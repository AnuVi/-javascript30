The purpose of these posts is to reflect my troubles and moments of ahhaa.

<strong>Lessons from Day 1</strong>:
<ol>
	<li><strong>const</strong>&ndash; so far I've used only <em>var</em> to define variables. <a href="https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Statements/const" target="_blank" title="MDN source" rel="external">Their values cannot be changed or redeclared</a>.</li>
	<li><strong>` back-ticks and template literals:</strong>
<pre>
const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);
</pre>
 This is the part I struggled the most. If I copied it, it worked, if wrote it on my own&ndash; it didn't. And I couldn't understand why? And no ideas what to google for. Fortunately there is always Twitter. 

Yes I know there are different types of quotes - ",',´. But turns out there are also <em>backticks</em> - on Win you can type them ALT + (num keyboard on right)9+  (num keyboard on right)6  or you have to Google for which key to press. 

<em>`${variable}`</em> as <a href="https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Template_literals" target="_blank" title="MDN source" rel="external">templating literals allowing embedded variables</a>.
</li>
	<li><a href="http://keycode.info/" target="_blank" rel="external" title="Keycode"><strong>http://keycode.info/</strong></a> to find quickly keyboard's key code.</li>
	<li><strong>if(!Obj) return;</strong> &ndash; stop the function if the Obj is null (there is no such object). I think I'm familiar with the concept but why I haven't it used before?</li>
	<li><strong>arrow-function</strong> So this function:
<pre>
 allAs.forEach(function(element) {
             element.classList.add('playing');
        });  

</pre>
can be written as an arrow-function:
<pre>
 allAs.forEach(element => element.classList.add('playing'));
</pre>

</li>
<li><strong>&lt;kbd&gt;</strong> is html&mdash;tag for <em>keyboard input</em></li>
	<li> Adding audio files I had to add .mp3 to the end
```html
	<audio data-key="65" src="drumkit/cowbell1.aif.mp3"></audio>
```

 </li>
	<li><strong>As I changed the word to "javascript"</strong> I had two "A"s. It got me some time to figure out that I can't detect if it is the first A or the second A by keypress. So I had to modify my code: 
<em>a) check if it is A </em>
<em>b) if it is get all the A-s (document.querySelectorAll)</em>
<em> c) and each of them add class "playing"</em>
<pre>
 if(e.keyCode =="65"){
         // get all letter A                 
         allAs = document.querySelectorAll(`div[data-key="${e.keyCode}"]`);
         allAs.forEach(element => element.classList.add('playing'));
         
    } else {
       key.classList.add('playing');
    }

</pre>

</li>






</ol>


