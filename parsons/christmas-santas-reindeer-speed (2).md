---
layout: default
title: "Christmas: Santa’s Reindeer Speed"
---

<p class="task-description">
Santa wants to calculate how fast his sleigh is travelling.
Each reindeer adds <strong>150 mph</strong> to the sleigh’s speed.
You must use a <strong>function</strong> to calculate the speed and then output the result.
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
"def calculate_speed(reindeer)\n" +
"    speed = reindeer * 150\n" +
"    return speed\n" +
"\n" +
"count = int(input('How many reindeer are pulling the sleigh? '))\n" +
"mph = calculate_speed(count)\n" +
"print('Your sleigh speed is', mph, 'mph')\n";

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
      parsonsPuzzle.getFeedback();
  });
})();
</script>
