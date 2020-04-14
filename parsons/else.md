---
layout: default
<!-- title: Ms. Hackman's If/else if/else Notes & Problems -->
<!-- description: Read through the following notes on if, else if , and else statements. Embeded in the notes are examples to try. Some of them are interactive on this site, requiring you to drag and code blocks into the right order to solve a problem. Others require you to write some code in the <a href="https://editor.p5js.org/">p5js editor</a> and then click the <i>See Answer</i> buttons to see a solution. After you've completed this, return to google classroom to do this week's assignment. -->
description:  
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
<!-- End of scripting functions! -->
    
    
<style>
.ui-sortable {
    width: 1000px;
}    
</style>


# Else Statements
The Else block is If’s partner is crime! An else block is code that the computer should run <b>ONLY</b>
when the If block code didn’t run. That is, the else block code only happens when the if block’s boolean statement was false. <b>Only  one</b>  of the <i>if</i> block or <i>else</i> block can happen.  <b>Either the if block code is run OR the else block code is run. Both CANNOT run.</b><br>

So in this code:
<code>
let x = 4;<br>
if(x > 5){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“Bigger than 5!”);<br>
} else{<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“Smaller or equal to 5!”); }<br>
</code>

The output would be "Smaller or equal to 5!", because 4 > 5 returns <i> false</i> and so we do NOT run our if block code. The else block gets run whenever its if statement is false.

What would happen if x was 10 instead?

<button onClick="myFunction('ex1')"> Show Answer </button>

<div id='ex1' style="display:none;" >
<code>
The output would be "Bigger than 5!" since 10 > 5 returns true. When the if statement is true, we skip the else statement.
</code>
</div>


## Exercise 1

Drag these lines of code into the solution box and put them in the correct order. This code should determine whether or not someone should pay for their cake based on if it is their birthday. The variable isBirthday is a boolean variable that is true when it is someone's birthday. 
<b> Remember to properly indent your code (code that is INSIDE an if block or an else block is indented). </b> 

<div id="ex1-sortableTrash" class="sortable-code"></div> 
<div id="ex1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="ex1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="ex1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "if(isBirthday){\n" +
    "    console.log(\"This birthday cake is free!\");\n" +
    "}\n" +
    "else{\n" +
    "	console.log(\"This cake will be $7.99 please\");\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "ex1-sortable",
    "max_wrong_lines": 2,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "ex1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#ex1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#ex1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


[Previous](https://ms-hackman.github.io/ParsonsProblems/)
[Next](./elseif.html)
