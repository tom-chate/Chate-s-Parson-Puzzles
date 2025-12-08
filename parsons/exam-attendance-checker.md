---
layout: default
title: "Exam Attendance Checker"
---

<p class="task-description">
A function decides if a student passes the course.
A student passes if:

their exam mark is 50 or more, AND

their attendance is 80 or more.

The function should return "Pass" or "Fail".

The function should take in two parameters and return the correct output

</p> 
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
  var initial = "def check_pass(exam_mark, attendance):\n" +
    "    if exam_mark &gt;= 50 and attendance &gt;= 80:\n" +
    "        return &quot;Pass&quot;\n" +
    "    else:\n" +
    "        return &quot;Fail&quot;\n" +"\n" +
    "";
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