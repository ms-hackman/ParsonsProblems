---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Ms. Hackman's If/else if/else Notes & Problems
description: Read through the following notes on if, else if , and else statements. Embeded in the notes are examples to try. Some of them require dragging and droppin code into the right order, the others require you to write some code on the <a href="https://editor.p5js.org/">p5js editor</a>. Click the <i>See Answer</i> buttons to see the solutions. 
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
    
We’ve already seen simple uses of if statements in class but let’s review and get a bit more complex!
# If Statements
If statements allow us to run parts of our code only run when certain conditions are met. These “conditions” must be written as  <b>true or false</b>  statements. True or false statements are called  <b>boolean expressions .</b>

<code>
if(<i>boolean expression</i>){<br >
    <i>code to run</i><br >
}  <br >
</code>


We refer to the if statement + boolean expression + code to run as an <b> if block.</b>

<button onClick="myFunction('code1')"> Hide Code 1 </button>

<div id='code1'>
<code>
console.log("Hello World");
</code>
</div>

    
Boolean expressions can be made up of any code that evaluates to <b> true or false </b>. Examples of boolean expressions include:

<code>
  X > 7 //is true if x is greater than 7, otherwise is false<br >
  Y <= 10 //is true if y is less than OR EQUAL TO 10, otherwise it is false<br>
  Z === 30 // checks if z is equal to 30. Note in p5js we use three equal signs to check if things are equal <br>
</code>

<b>Note a boolean variable is ALREADY a boolean expression.</b> So the following code would actually display “Yes, Ms. Hackman is very very very cool.” (regardless of how true you think that statement actually is.

<code>
let isCool = true;<br >
if(isCool){<br >
console.log(“Yes, Ms. Hackman is very very very cool.”);<br>
}<br>
</code>

The code we want to run if our if statement is true must live between two curly brackets {}. It is a common bug to forget one of your curly brackets, or to accidentally put code inside the brackets, you meant to be outside (or put code outside the brackets you meant to put inside), so be careful!

## Question 1:





### Implementation Notes

When you host multiple Parson's problems on a single markdown page, you need to add a unique prefix. You can easily do this in the Codio generator by typing a unique prefix into the "Prefix" textbox and pressing Enter/Return. Then you can simply copy-paste like normal.

If want each problem to be it's own page, you can use relative path links at the bottom of each of your markdown pages as seen below. If you want students to be able to return to previous problems in this format, consider adding previous links or link to a table of contents like page.

### Example Next Link
[Next](./parsons/example1.html)
