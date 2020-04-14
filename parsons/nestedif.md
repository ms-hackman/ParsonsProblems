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

This code determines if someone should go for a hike based on whether or not it is raining and whether or not they have a rain coat. We want this code to tell someone to go for a hike if it is sunny. If it isn't sunny, it should check that they have a raincoat to determine if they should go for a hike. Naturally we only want to ask the user if they have a raincoat if it's not sunny out. So we only want our if chain that checks if the user has a raincoat (bolded above) to run if we've already determined it is not sunny. 

To achieve this effect, we use a <b> nested</b> if statement. This code has a main if/else chain to check if it is sunny, and there is a <b>nested</b> if/else chain inside our original else block, which checks if the user has a raincoat. This code will ONLY get run if we enter that else block. 

### Exercise 5
What would this code print out if <code>isSunny</code> is false and <code>haveRaincoat</code> is false?

<button onClick="myFunction('rainanswer1')"> Show Answer </button>

<div id='rainanswer1' style="display:none;" >
<i> Answer: Best not go today. Try again tomorrow!  </i><br>
</div>

 Note that the nested if/else block is indented, and its code blocks are doubly indented to help us read our code more easily. This indentation makes it easier to see that the bolded text is INSIDE the else block. It also helps us see that the bolded console.log lines belong to the code blocks of these nested if/else statements. <br>
 
 It's also important to note that we can tell which if statement an else statement belongs to  by checking which if block it is touching. Each else statement is immediately after the closing parenthesis of the if statement (or else if statement) it belongs to. <br>

### Exercise6
Rearrange the code blocks below to modify the hiking example so it will first check to see if the user has hiking boots. it will only bother checking if the user can go hiking if they already have hiking boots. Use the boolean variable <code>haveHikingBoots</code> to represent if the user has hiking boots. <br>


<div id="ex6_Rain-sortableTrash" class="sortable-code"></div> 
<div id="ex6_Rain-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="ex6_Rain-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="ex6_Rain-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "if(haveHikingBoots){\n" +
    "	if(isSunny)({\n" +
    "		console.log(\"Sure, go for a hike! It's really nice out!\");\n" +
    "	}\n" +
    "	else{\n" +
    "		if(haveRaincoat){\n" +
    "    		console.log(\"Go for a hike, but don't forget your raincoat!\");\n" +
    "		}\n" +
    "    	else{\n" +
    "    		console.log(\"Beast not go today. Try again tomorrow!\");\n" +
    "    	}\n" +
    "	}\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "ex6_Rain-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#ex6_Rain-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#ex6_Rain-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

[Previous](./moreelseif.html)
<!-- [Next](./nestedif.html) -->
