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
<style>
.ui-sortable {
    width: 1000px;
}    
</style>
<!-- End of scripting functions! -->
    


# Else If Statements

Now what if we have more than two possible situations? We can add “else if” blocks between our if and else statement to create multiple possibilities. For example:<br>
<code>
let grade = 4;<br>
if(grade <=6){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in elementary school”);<br>
else if(grade <= 9 ){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in junior high!”);<br>
} else{<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in high school!”);<br>
}<br>
</code>

This code will determine what school a student attends based on their current grade. Just like with if and else blocks,  <b>only ONE</b>  of our if, else if, and else statements will happen. <b>Whenever we find our first true if/else if statement, we skip the rest.<b> If no true if (or else if) statement is found, then the else block is done.<br>
<br>


<b>NOTE:</b>The order of our if statements are important. Your code checks each if statement in order, from top to bottom.  Consider the following example:<br>
<code>
let grade = 4;<br>
if(grade <=9){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in junior high school”);<br>
}<br>
else if(grade <= 6 ){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in elementary!”); }<br>
else{<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in high school!”);<br>
}<br>
</code>

## Exercise 2
What will this code currently print out? 
<button onClick="myFunction('schoolanswer')"> Show Answer </button>

<div id='schoolanswer' style="display:none;" >
<i> This Code will print out <code>This student is in junior high</code> because the code is run in order from top to bottom. The first if statement is true, because grade 4 is less than 9, and so it prints out the student is in junior high. Since only one of our if/else if/else statements can be run, skip the else if and else statement.   </i><br>
</div>

Rewrite the grade checking code above to only use greater than signs (>) to correctly identify the student's school level. 
<b> Note there are EXTRA lines of code here that are not necessary for the solution. Do not expect you need to use all the lines of code </b><br>
<div id="school1-sortableTrash" class="sortable-code"></div> 
<div id="school1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="school1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="school1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "if(grade >9){\n" +
    "	console.log(“This student is in high school!”);\n" +
    "}\n" +
    "else if(grade > 6){\n" +
    "	console.log(“This student is in junior high!”);\n" +
    "}\n" +
    "else {\n" +
    "	console.log(“This student is in elementary school”);\n" +
    "}\n" +
    "if(grade > 6){ #distractor\n" +
    "if(grade > 0){ #distractor\n" +
    "else if(grade > 9){ #distractor\n" +
    "else if(grade > 0){ #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "school1-sortable",
    "max_wrong_lines": 4,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "school1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#school1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#school1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

<button onClick="myFunction('schoolhint')"> Show Hint </button>

<div id='schoolhint' style="display:none;" >
<i> Remember there are three cases!<br>
1) The student is in elementary:  grade >0<br>
2)  The student is in junior high: grade > 6 <br>
3) The student is in high school: Grade 9 <br>
What order do we need to check these three cases so that a grade 12 student is placed in high school?</i><br>
</div>


## If/Else if/Else Chains


I refer to a connected set of if/elseif/else statements as a  chain. An if statement is connected to any else if/else statements that immediately follow it. <b>If statements are not connected to other if statements.<b> For example:<br>
    
<code>
 Let grade = 4; <br>
 if(grade <=6){<br>
 &nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in elementary school”);<br>
 }<br>
 if(grade <=9){<br>
 &nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in junior high school”);<br>
 }   <br>
</code>

These if statements are  <b>not<b>  chained. Only <i>else if</i> or <i>else</i> blocks can attach to a chain.  In this case, when the first if statement is true, we don’t skip the second if statement since they’re not connected.  Both of them  are true so both of console.log statements will run. 
    
## Exercise 3
Consider the following scenario. You are looking at moving into one of two apartments. Both apartments have special monthly fees for owning pets and both charge $900 for monthly rent. <br>

<b>Apartment 1</b> charges you a fee of $20 for the first dog and $5 for each dog after that, and $10 dollars for your first cat and $3 for each cat after that. <br>
<b> Apartment 2 </b>charges you $60 if you have any number of dogs, but only $40 if you only have cats. <br>

Assuming you have variables numCats and numDogs which tell you how many cats and dogs you have, determine the code you would need to write to determine your total monthly costs for each Apartment. Store the total amount you have to pay in a variable named total.

<b> Note there are EXTRA lines of code here that are not necessary for the solution. Do not expect you need to use all the lines of code </b><br>

### Apartment 1
<div id="dogs1-sortableTrash" class="sortable-code"></div> 
<div id="dogs1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="dogs1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="dogs1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "let total = 900;\n" +
    "if(numDogs >=1){\n" +
    "	total +=  $20 + (numDogs -1)*5;\n" +
    "}\n" +
    "if(numCats >=1){\n" +
    "	total += $10 + (numCats - 1)*3;\n" +
    "} \n" +
    "else if(numCats >=1){ #distractor\n" +
    "else if(numDogs >=1){ #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "dogs1-sortable",
    "max_wrong_lines": 2,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "dogs1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#dogs1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#dogs1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

<button onClick="myFunction('doghint1')"> Show Hint </button>

<div id='doghint1' style="display:none;" >
<i> Hint: Remeber using an if and an else statement means one OR the other happens. In this situation, we pay per cat AND dog so we do not want to use an else statement. </i><br>
</div>

### Apartment 2
<div id="dogs2-sortableTrash" class="sortable-code"></div> 
<div id="dogs2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="dogs2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="dogs2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "let total = 900;\n" +
    "if(numDogs >=1){\n" +
    "   total += 60;\n" +
    "}\n" +
    "else if(numCats >=1){\n" +
    "	total += 40;\n" +
    "} \n" +
    "if(numCats >=1) #distractor\n" +
    "else{ #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "dogs2-sortable",
    "max_wrong_lines": 1,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "dogs2-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#dogs2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#dogs2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
<button onClick="myFunction('doghint2')"> Show Hint </button>

<div id='doghint2' style="display:none;" >
<i> Hint: Remeber using an if and an else statement means one OR the other happens. In this situation, we either pay the dog or the cat fee. So we only want to pay one fee or the other.  </i><br>
</div>

[Previous](./else.html)
[Next](./moreelseif.html)
