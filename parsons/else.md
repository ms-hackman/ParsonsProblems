---
layout: default
title: Ms. Hackman's If/else if/else Notes & Problems
description: Read through the following notes on if, else if , and else statements. Embeded in the notes are examples to try. Some of them are interactive on this site, requiring you to drag and code blocks into the right order to solve a problem. Others require you to write some code in the <a href="https://editor.p5js.org/">p5js editor</a> and then click the <i>See Answer</i> buttons to see a solution. After you've completed this, return to google classroom to do this week's assignment.
---

<!-- Function for hiding code!  -->
<script>
    function myFunction(name) {
      var x = document.getElementById(name);
      if (x.style.display === "none") {
        x.style.display = "block";
      } else {
        x.style.display = "none";
      }
    }    
</script>
<!-- End of scripting functions! -->
    


# Else Statements
The Else block is If’s partner is crime! An else block is code that the computer should run <b>ONLY</b>
when the If block code didn’t run. That is, the else block code only happens when the if block’s boolean statement was false. <b>Only  one</b>  of the <i>if</i> block or <i>else</i> block can happen.  <b>Either the if block code is run OR the else block code is run. Both CANNOT run.</b><br>

So in this code:
<code>
let x = 4;<br>
if(x > 5){<br>
&emsp console.log(“Bigger than 5!”);<br>
} else{<br>
&emspconsole.log(“Smaller or equal to 5!”); }<br>
</code>


[Previous](../)
[Next](./example2.html)
