---
layout: default
title: "Exam Bonus Calculator"
---

<p class="task-description">
A function works out a student’s final score. <br>
The test mark is out of 100 <br>
The bonus score is out of 10 <br>
Final score = test_mark + (bonus * 5) <br>
Then:
<ul>
<li> If final score ≥ 90 → "Excellent" </li>
<li> Else if final score ≥ 60 → "Pass"" </li>
<li> Else → "Fail" </li>
</ul>
<p class="task-instructions">
Drag or shuffle the blocks of code in the practice problems below.
Remember to indent where appropriate by dragging blocks to the right.
To check your work, press the "Get Feedback" button.
To start over, press the "Reset Problem" button.
</p> 
<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def calculate_result(test_mark, bonus):\n" +
    "    final_score = test_mark + (bonus * 5)\n" +"\n" +
    "    if final_score &gt;= 90:\n" +
    "        return &quot;Excellent&quot;\n" +
    "    elif final_score &gt;= 60:\n" +
    "        return &quot;Pass&quot;\n" +
    "    else:\n" +
    "        return &quot;Fail&quot;";
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