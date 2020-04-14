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
    width: 1000px;
}    
</style>
<!-- End of scripting functions! -->
    


# Multiple Else If Statements
You can have multiple else if statements in a chain.  Looking back at our grade example, if we wanted to say any student after grade 12 is graduated, we could add more else/if statements:<br>

<code>
let grade = 14;<br>
if(grade <=6){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in elementary school”);<br>
}<br>
else if(grade <= 9 ){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in junior high!”); }<br>
else if(grade <= 12){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in high school!”);<br>
} else{<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This person has graduated!”); }<br>
</code>

We can just keep adding if statements to handle more and more cases. 

## Exercise 4
Rewrite the  code above so it prints out “This child is too young for school” if their grade is less than 0.<br>
<div id="school2-sortableTrash" class="sortable-code"></div> 
<div id="school2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="school2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="school2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "if(grade < 0){\n" +
    "	console.log(\"This child is too young for school\");\n" +
    "}\n" +
    "else if(grade <=6){\n" +
    "	console.log(“This student is in elementary school”);\n" +
    "}\n" +
    "else if(grade <= 9 ){\n" +
    "	console.log(“This student is in junior high!”); \n" +
    "}\n" +
    "else if(grade <= 12){\n" +
    "	console.log(“This student is in high school!”);\n" +
    "} \n" +
    "else{\n" +
    "	console.log(“This person has graduated!”); \n" +
    "}\n" +
    "if(grade <= 6){ #distractor\n" +
    "else if(grade < 0){ #distractor\n" +
    "if(grade <=9){ #distractor\n" +
    "if(grade <=12){ #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "school2-sortable",
    "max_wrong_lines": 4,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "school2-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#school2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#school2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

<button onClick="myFunction('schoolSolution1')"> Show Answer </button>

<div id='schoolSolution1' style="display:none;" >
<code>
if(grade <0){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log("This child is too young for school!");<br>
}<br>
else if(grade <=6){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in elementary school!”);<br>
}<br>
else if(grade <=9){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in junior high school!”);<br>
}<br>
else if(grade <=12){<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This student is in high= school!”);<br>
}<br>
else{<br>
&nbsp;&nbsp;&nbsp;&nbsp;console.log(“This person has graduated!”);<br>
}<br>
</code>
</div>

[Previous](./elseif.html)
[Next](./nestedif.html)
