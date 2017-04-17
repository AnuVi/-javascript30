
<strong>Lessons from Day 13</strong>:
<ol>
	<li><strong>wrapping function to function</strong><pre>

 window.addEventListener('scroll', debounce(checkSlide));
</pre>
</li>
	<li><strong> calling function after every 5 seconds</strong>
<pre>
 window.addEventListener('scroll', debounce(checkSlide, 5000));
</pre>

</li>
	<li>  <strong>window.scrollY</strong>&mdash; <a href="https://developer.mozilla.org/en-US/docs/Web/API/Window/scrollY" target="_blank"  rel="external"  title="MDN link">Returns the number of pixels that the document has already been scrolled vertically.</a>
</li>


	<li> <strong>window.innerHeight</strong>&mdash;h<a href="https://developer.mozilla.org/en-US/docs/Web/API/Window/innerHeight" target="_blank" rel="external"  title="MDN link">eight (in pixels) of the browser window viewport including, if rendered, the horizontal scrollbar</a></li>

	<li><strong>slideImage.offsetTop</strong>&mdash; how far image top is from the actual window
</li>
	<li><strong>perfomance issues! - look at debounce function</strong></li>



    	


	






</ol>
