<a href="https://javascript30.com/" target="_blank" title="JavaScript30" rel="external">JavaScript30</a> is 30-day vanilla javaScript coding challenge by <a href="http://wesbos.com/" target="_blank" title="Wes Bos's website" rel="external">Wes Bos</a> (<a href="https://twitter.com/wesbos?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor" target="_blank" title="Wes Bos on Twitter">@wesbos</a>). 

The purpose of these posts is to reflect my troubles and moments of ahhaa.

<strong>Lessons from Day 2 &mdash; CSS-JS clock</strong>:
<a href="http://www.anuvi.me/javascript30/day2.html" target="_blank" title="Demo-Day 2" rel="external">Demo - Day 2</a>

<ol>
	<li><strong>Date()</strong> gives a chance to get hours, minutes, seconds etc.
<pre>

const now = new Date();
seconds = now.getSeconds();
minutes = now.getMinutes();
hours = now.getHours()


</pre>




</li>
	<li><strong>transform-origin</strong> vs <strong>transform:rotate() </strong> </br> 
The first one sets the point around which the transformation takes place.<em> Rotate() </em>is driven by center of the element. More about <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/transform-origin" rel="noopener" target="_blank" rel="exeternal">MDN  transform-origin</a>
.</li>

</ol>
