The purpose of these posts is to reflect my troubles and moments of ahhaa.

<a href="http://www.anuvi.me/javascript30/day7.html" target="_blank" title="Day 7" rel="external">Demo</a>

<strong>Lessons from Day 7</strong>:
<ol>
	<li><strong>Array.prototype.some();</strong> is there at least one match? Returns <em>true</em> or <em>false</em>.

</li>
	<li><strong>Array.prototype.every(); </strong>every single item in array matches to the condition or not?  Returns <em>true</em> or <em>false</em>.</li>
	<li><strong>console.log({variable});</strong> - in console can be seen like
<pre>

isAdult:true
</pre>
</li>
	<li><strong>Array.prototype.find();</strong> Find is like filter, but instead returns just the one you are looking for</li>
	<li><strong>With all these methods we can use array method without <em>if-statment</em></strong>&mdash; because method returns <em>true</em> or <em>false</em>.
So, instead this:
<pre>
const comment = comments.find(function(comment){
      if (comment.id === 823423){
         return true;
      }

    });
</pre>
we can write:
<pre>
const comment = comments.find(comment => comment.id ===823423);
</pre>

</li>
	<li><strong>Deleting from array:</strong> First use <em>Array.prototype.findIndex() and then use <em></em>splice()</em><pre>
 const commentB = comments.findIndex(comment=>comment.id ===823423);
 //returns 1
comments.splice(0, 1);
</pre>

or creating<em> new array</em>, <em>spread</em> and slice(), 
<pre>
const index = comments.findIndex(comment=>comment.id ===542328);
    const newComments = [
      ...comments.slice(0,index),
      ...comments.slice(index + 1)
    ];
    console.table(newComments);
</pre>

</li>


</ol>
