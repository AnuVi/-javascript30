<strong>Lessons from Day 17 &mdash; a/an/the</strong>:
<ol>
<li><strong>Regex to replace a/an/the with ' '</strong>
<pre>
function strip(bandName){

  return bandName.replace(/^(a |the |an )/i,'').trim();

}
</pre>
</li>
	<li><strong>Ternary operator</strong> - ?: is called <a href="https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Operators/Conditional_Operator" target="_blank" title="Ternary operator -MDN">ternary operator</a>
<pre>
return strip(a) > strip(b) ? 1 : -1
</pre>

</li>
	<li><strong>How to write a function</strong>in three ways:<pre>
//first
const sortedBands = bands.sort(function(a,b){
 return strip(a) > strip(b) ? 1 : -1
});

//as arrow-function
const sortedBands = bands.sort ((a,b) =>{
 return strip(a) > strip(b) ? 1 : -1
});

// if the only thing you are doing in function is returning - you can do implicit return
const sortedBands = bands.sort((a,b) => strip(a) > strip(b) ? 1 : -1);
</pre>
</li>
	<li><strong>Output with/without commas</strong>
<pre>
sortedBands.map(band => `<li>${band}</li>`);
</pre>
//will give you commas after the names:
["<li>Anywhere But Here</li>", "<li>The Bled</li>", "<li>Counterparts</li>", "<li>The Devil Wears Prada</li>", "<li>The Midway State</li>", "<li>Norma Jean</li>", "<li>Oh, Sleeper</li>", "<li>An Old Dog</li>", "<li>Pierce the Veil</li>", "<li>The Plot in You</li>", "<li>Say Anything</li>", "<li>A Skylit Drive</li>", "<li>We Came as Romans</li>"]
<pre>
sortedBands.map(band => `<li>${band}</li>`).join('');
</pre>
//will give
<li>Anywhere But Here</li><li>The Bled</li><li>Counterparts</li><li>The Devil Wears Prada</li><li>The Midway State</li><li>Norma Jean</li><li>Oh, Sleeper</li><li>An Old Dog</li><li>Pierce the Veil</li><li>The Plot in You</li><li>Say Anything</li><li>A Skylit Drive</li><li>We Came as Romans</li>




</li>





    	


	






</ol>
