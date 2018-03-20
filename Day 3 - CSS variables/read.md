<a href="https://javascript30.com/" target="_blank" title="JavaScript30" rel="external">JavaScript30</a> is 30-day vanilla javaScript coding challenge by <a href="http://wesbos.com/" target="_blank" title="Wes Bos's website" rel="external">Wes Bos</a> (<a href="https://twitter.com/wesbos?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor" target="_blank" title="Wes Bos on Twitter">@wesbos</a>). 

The purpose of these posts is to reflect my troubles and moments of ahhaa.<br>
<strong>Lessons from Day 3 &mdash; CSS Variables + JS</strong>: <br>
<a href="http://www.anuvi.me/javascript30/day3.html" target="_blank" title="Demo-Day 3" rel="external">Demo - Day 3</a><br>
<ol>
	<li><strong>- -</strong> declares variables in CSS as $ in php or var in javaScript.
You declare:
<pre>
:root{
--basecolor:#ffc600;
}

</pre>

and call it out like this:

<pre>
p {
 backround-color: var(--basecolor);
}
</pre>

</li>
	<li><strong>:root</strong> is the deepest level you can go.</li>

	<li>
If you want update your e.g. style attribute according to input via javaScript <strong>variable and name should have the same name, otherwise it wont work:</strong>
<pre>
<input id="base" type="color" name="basecolor" value="#ffc600">
</pre>

<em>- -basecolor:#ffc600;</em>
</li>
	<li><strong>NodeList vs array</strong>
<em>document.querySelectorAll</em> gives <em>NodeList</em>. The difference between <em>NodeList</em> and <em>array</em> is that <em>array</em> gives you all kinds and longer <em>list of methods</em> like map,reduce.

<strong>List of methods for array:</strong><br><a href="http://www.anuvi.me/blog/wp-content/uploads/2018/03/array.jpg" rel="attachment wp-att-513"><img src="http://www.anuvi.me/blog/wp-content/uploads/2018/03/array.jpg" alt="methods list for array" width="259" height="293" class="aligncenter size-full wp-image-513" /></a><br>
<strong>List of methods for NodeList:</strong><br>
<a href="http://www.anuvi.me/blog/wp-content/uploads/2018/03/NodeList.jpg" rel="attachment wp-att-514"><img src="http://www.anuvi.me/blog/wp-content/uploads/2018/03/NodeList.jpg" alt="methods for NodeList" width="407" height="310" class="aligncenter size-full wp-image-514" /></a>
</li>


</ol>
