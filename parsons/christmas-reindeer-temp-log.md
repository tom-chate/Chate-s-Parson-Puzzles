---
layout: default
title: "Christmas: Reindeer Temperature Log"
---

<p class="task-description">
Santa checks the temperature for his reindeer several times.
For each temperature, the program should decide if it is <strong>Safe</strong> or <strong>Too cold</strong>
and write the results to a file called <strong>temp_log.txt</strong>.
</p>

<p class="task-instructions">
Drag or shuffle the blocks of code below into the correct order.
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
  var initial =
"file = open('temp_log.txt', 'w')\n" +
"for i in range(5):\n" +
"    temp = int(input('Enter temperature: '))\n" +
"    if temp <= -10:\n" +
"        status = 'Too cold'\n" +
"    else:\n" +
"        status = 'Safe'\n" +
"    print(temp, 'is', status)\n" +
"    file.write(str(temp) + ',' + status + \"\\n\")\n" +
"file.close()";

  var parsonsPuzzle = new ParsonsWidget({
      sortableId: "sortable",
      grader: ParsonsWidget._graders.LineBasedGrader,
      max_wrong_lines: 0,
      exec_limit: 2500,
      can_indent: true,
      x_indent: 50,
      lang: "en"
  });

  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();

  $("#newInstanceLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.shuffleLines();
  });

  $("#feedbackLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.getFeedback(); // visual feedback only
  });
})();
</script>
