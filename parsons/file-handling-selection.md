---
layout: default
title: "Word Counter (Count Controlled)"
---

<p class="task-description">
A program:

asks the user to enter 3 numbers

writes each number to a file called numbers.txt

if the number is greater than 10, it writes "High" after the number

otherwise, it writes "Low"</p> 
<p class="task-instructions">
Drag or shuffle the blocks of code in the practice problems below.
Remember to indent where appropriate by dragging blocks to the right.
To check your work, press the "Get Feedback" button.
To start over, press the "Reset Problem" button.
</p> 
<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
var initial = "file = open(\"numbers.txt\", \"w\")\n" +
"for i in range(3):\n" +
"    number = int(input(\"Enter a number: \"))\n" +
"    if number > 10:\n" +
"        file.write(str(number) + \" High\")\n" +
"    else:\n" +
"        file.write(str(number) + \" Low\")\n" +
"file.close()\n";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>