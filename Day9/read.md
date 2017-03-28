<a href="http://www.anuvi.me/javascript30/day9.html" target="_blank" title="Demo-Day 9" rel="external">Demo - Day 9</a>

<strong>Lessons from Day 9</strong>:

Some console tricks (on Win Ctrl+Shift+I)
<ol>
<li>
<strong>Interpolated strings in console.log()</strong>
<pre>
    console.log('Hello');
    console.log('I am a %s string', 'awesome' );
    var string = "awesome";
    console.log(`I am ${string} string`);

</pre>
<a href="http://www.anuvi.me/blog/wp-content/uploads/2017/03/interpolated_string.jpg" rel="attachment wp-att-421"><img src="http://www.anuvi.me/blog/wp-content/uploads/2017/03/interpolated_string.jpg" alt="Interpolated string" width="938" height="91" class="aligncenter size-full wp-image-421" /></a>
</li>

<li>
<strong>Styling console.log()</strong>
<pre>
    console.log('%c I am awesome string', 'color:#BADA55; font-size:20px;');
</pre>
<a href="http://www.anuvi.me/blog/wp-content/uploads/2017/03/styled.jpg" rel="attachment wp-att-423"><img src="http://www.anuvi.me/blog/wp-content/uploads/2017/03/styled.jpg" alt="Styled console.log()" width="1128" height="34" class="aligncenter size-full wp-image-423" /></a>
</li>
	<li><strong>Warning&mdash;console.warn()</strong><pre>
    console.warn("No!");
</pre>
<a href="http://www.anuvi.me/blog/wp-content/uploads/2017/03/warning.jpg" rel="attachment wp-att-424"><img src="http://www.anuvi.me/blog/wp-content/uploads/2017/03/warning.jpg" alt="consol. warn()" width="604" height="29" class="aligncenter size-full wp-image-424" /></a>
</li>
	<li><strong>Error&mdash;console.error()</strong>
<pre>
    console.error("Smth went wrong!");
</pre>
<a href="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_error.jpg" rel="attachment wp-att-425"><img src="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_error.jpg" alt="console_error" width="353" height="30" class="aligncenter size-full wp-image-425" /></a>
</li>
<li><strong>Info&mdash;console.info()</strong>
<pre>
 console.info("console.info() is for providing info!");
</pre>
<a href="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_info.jpg" rel="attachment wp-att-426"><img src="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_info.jpg" alt="console_info" width="360" height="24" class="aligncenter size-full wp-image-426" /></a>
</li>
<li><strong>Clearing console&mdash;console.clear()</strong>&mdash; simpliest way to clear console.
</li>
<li><strong>Testing&mdash;console.assert()</strong> - <em>returns only if the statemeny is false</em><pre>
   console.assert (1===1, 'That is true'); // won't show anything
   console.assert (1===2, 'That is wrong'); //shows text

    const p = document.querySelector('p');
    console.assert (p.classList.contains('whatever'), 'No such class!');
</pre>
<a href="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_assert.jpg" rel="attachment wp-att-427"><img src="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_assert.jpg" alt="console_assert" width="360" height="46" class="aligncenter size-full wp-image-427" /></a>
</li>
<li><strong>Viewing DOM elements&mdash;console.dir</strong><pre>
 console.log(p); //shows actual element itself
 console.dir(p); // shows all the element's attributes and methods
</pre>
Image shows only a fragment of<em> console.dir()</em>:
<a href="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console.dir_.jpg" rel="attachment wp-att-428"><img src="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console.dir_.jpg" alt="console.dir()" width="937" height="421" class="aligncenter size-full wp-image-428" /></a>
</li>
<li><strong>Grouping together&mdash;console.group()&mdash;uncollapsed version</strong><pre>
dogs.forEach(dog => {
      console.group(`${dog.name}`); // uncollapsed
      console.log(`This dog is ${dog.age} years old`);
      console.groupEnd(`${dog.name}`); // important to put otherwise inside each other

    });
</pre>
<a href="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_group_uncollapsed.jpg" rel="attachment wp-att-429"><img src="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_group_uncollapsed.jpg" alt="console_group_uncollapsed" width="474" height="104" class="aligncenter size-full wp-image-429" /></a>
</li>
<li><strong>Grouping together&mdash;console.group()&mdash;collapsed version</strong><pre>
dogs.forEach(dog => {
      console.groupCollapsed(`${dog.name}`); // collapsed
       console.log(`This dog is ${dog.age} years old`);
      console.groupEnd(`${dog.name}`); // important to put otherwise inside eacother

    });
</pre>
Hugo is clicked open to show provided information:
<a href="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_group_collapsed.jpg" rel="attachment wp-att-430"><img src="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_group_collapsed.jpg" alt="console_group_collapsed" width="403" height="76" class="aligncenter size-full wp-image-430" /></a>
</li>
<li><strong>Counting&mdash;console.count()</strong><pre>
    console.count('S');
    console.count('S');
    console.count('R');
    console.count('S');
    console.count('S');
    console.count('T');
    console.count('T');
    console.count('S');
    console.count('L');
</pre>
<a href="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_count.jpg" rel="attachment wp-att-431"><img src="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_count.jpg" alt="console_count" width="360" height="226" class="aligncenter size-full wp-image-431" /></a>
</li>
<li><strong>Timing&mdash;console.time()</strong>&mdash; how long operation takes time<pre>
console.time('fetching data');
    fetch('https://api.github.com/users/wesbos')
    .then(data => data.json())
    .then(data =>{
      console.timeEnd('fetcing data');
      console.log(data);
    });
</pre>
<a href="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_time.jpg" rel="attachment wp-att-433"><img src="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_time.jpg" alt="console_time" width="1082" height="97" class="aligncenter size-full wp-image-433" /></a>
</li>
<li><strong>console.table()&mdash;displays tabular data as table</strong><pre>
console.log(dogs);
console.table(dogs);//same size of objects
</pre>
<a href="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_table.jpg" rel="attachment wp-att-432"><img src="http://www.anuvi.me/blog/wp-content/uploads/2017/03/console_table.jpg" alt="console_table" width="1182" height="134" class="aligncenter size-full wp-image-432" /></a>
</li>










    	


	






</ol>

