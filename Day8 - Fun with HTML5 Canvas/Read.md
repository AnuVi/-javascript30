<a href="http://www.anuvi.me/javascript30/day8.html" target="_blank" title="Demo-Day 8" rel="external">Demo</a>
<ol>

<li><strong>Organizing your variables and values as an array:</strong>
<pre>
[lastX, lastY] = [e.offsetX, e.offsetY];
</pre>
is the same as:
<pre>
lastX = e.offsetX;
lastY = e.offsetY;
</pre>

</li>
	<li><strong>hsl</strong>&mdash; h is for hue (between 0-360), s is for saturation and l is for lightness.</li>
	<li><strong>strokeStyle and lineWidth</strong> It's <em>ctx.strokeStyle</em> for color, but <em>ctx.lineWidth </em>for width.</li>
	<li><strong>direction != direction</strong> and <strong>direction = !direction</strong> - let's assume that direction is true:
<pre>
direction != direction // true isn't equal to true
direction = !direction  // change direction's value to opposite - if true, now be false

</pre>


</li>
	<li><strong>Debugging:</strong><ul>
	<li><strong>console.log(canvas)</strong>- as it didn't do nothing and no spelling mistakes so far - turned out I had accidentally deleted the '</script>' tag.</li>
	<li><strong>inside draw()</strong> - <em>console.log(e) </em>after the condition, if I console it before it gives me true and false, but I only want one of them.</li>
	<li><strong>calling out draw function</strong> - <em>addEventListener('mousemove')</em> worked but nothing else  didn't care if it was false or true. Possible ways to debug:<pre>
inside function draw(){
	console.log(isDrawing);
	if(isDrawing ="false") return;
}
</pre>
It turned out to be spelling mistake in <em>addEventListener('mousedown'),()=> is<strong>DAR</strong>wing = true);</em> and not <em>addEventListener('mousedown'),()=> i<strong>sDRA</strong>wing = true);</em>
</li>



</ul>


</li>




	






</ol>
