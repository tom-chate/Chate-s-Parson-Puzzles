---
layout: default
title: "Password Checker: Conditional Controlled"
---
<p class="task-description">
 Ask the user to input how many GCSE’s they have. They should then be allowed to enter a result for each GCSE grade.  The computer should work out how many
points they have got (9=9, 8=8, 7=7 etc). If their total score is 40 or over it should output ‘You can go to the sixth form’. If they their score between 35 and 39 it should
output ‘A discussion is needed.  Otherwise, it should say ‘Sorry not enough points.’

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
var initial = "length = 0\n" +
    "count = 0\n" +
    "while length &lt; 7:\n" +
    "  password = input(&quot;What is the password? &quot;)\n" +
    "  length = len(password)\n" +
    "  count = count + 1\n" +
    "print(&quot;It took &quot; + str(count) + &quot; attempts&quot;)";
    
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
</script>

