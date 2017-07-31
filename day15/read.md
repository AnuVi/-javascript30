
The purpose of these posts is to reflect my troubles and moments of ahhaa.

<a href="http://www.anuvi.me/javascript30/day15.html" target="_blank" title="Day 15" rel="external">Demo</a>

<strong>Lessons from Day 15 &mdash; LocalStorage and EventDelegation</strong>:
<ol>
		<li><strong>Form and submit: </strong> if it is form you should listen to <em>submit</em>&mdash;event and not click.</li>
	<li><strong>this.querySelector('[name=item]')</strong> So if we have form like this:<pre>
<form name="frm" id="js-frm">
<input class="js-it" name="i">
</form>
</pre>
We can grab input value like this:
<pre>
var input = document.querySelector('.js-it');
var inputValue = input.value;
</pre>
or using <em>this</em> and p<em>arthensis</em>:
<pre>
var input = (this.querySelector['name=it']).value;
</pre>

</li>
	<li><strong>plates=[]</strong>: We have function<pre>
function populateList(plates=[], plateList){
 //code here
    
  }

</pre>
<em>plates=[]</em> is an <em>empty object</em> and if we forget to pass something in, it won't broke our JavaScript
</li>
	<li><strong>.map()</strong>: <em>creates</em> from one array <em>another arra</em>y.</li>
	<li><strong>.join('')</strong>: returns <em>.map() </em>array<em> as a string</em>.</li>
	<li><strong><input type="checkbox" checked="false"></strong> will still be <em>checked</em>&mdash; <em>any existence of attribute checked</em> will check it.</li>
	<li><strong>localStorage</strong> accepts only <em>strings.</em> If it's something else in<em> Console->Application-> Local Storage</em> you'll see <em>[object Object]</em>. It can be stringified:<pre>
localStorage.setItem('items', JSON.stringify(items));
</pre>
</li>
	<li><strong>JSON. parse()</strong> is opposite to <em>JSON.stringify()</em>, itparses string to origin value or object.</li>
	<li><strong>setting value as condition:</strong> <pre>
const items = JSON.parse(localStorage.getItem('items')) || [];
</pre>
</li>







</ol>

