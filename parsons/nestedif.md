---
layout: default
---

<!-- Function for hiding code!  -->
<script>
    function myFunction(name) {
      var x = document.getElementById(name);
      if (x.style.display === "none") {
        x.style.display = "block";
      } 
      else if(x.style.display ==="first"){
          x.style.display="none";         
      }
      else {
        x.style.display = "none";
      }
    }    
</script>
<style>
.ui-sortable {
    width: 700px;
}    
</style>
<!-- End of scripting functions! -->
    


# Nested If Statements

if/else if/else chains are just like any other code. Which means that you could put an if/else if/else chain INSIDE the code blocks for another if/else if/else chain. For example, look at the following code: <br>

<code>
let isSunny = false;<br>
let haveRaincoat = true;<br>
let haveUmbrella = true;<br>
let haveHikingboots = true;<br>
if(isSunny){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“Sure, go for a hike! It’s really nice out!”);<br>
}<br>
else{<br>
<b>&nbsp;&nbsp;&nbsp;&nbsp;if(haveRaincoat){<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;console.log(“Go for a hike, but don’t forget your raincoat!);<br>
&nbsp;&nbsp;&nbsp;&nbsp;}<br>
&nbsp;&nbsp;&nbsp;&nbsp;else{<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;console.log(“Best not go today. Try again tomorrow!”);<br>
&nbsp;&nbsp;&nbsp;&nbsp;}<br></b>
}<br>    
</code>

This code has a main if/else chain, but there is a <b>nested</b> if/else chain (which is bolded above) inside the code block of the main chain's else statement. 

[Previous](./moreelseif.html)
[Next](./nestedif.html)
