---
layout: default
title: "Christmas: Advent Calendar Grid"
---

<p class="task-description">
Santa has a 4x4 advent calendar stored as a 2D list.
Write a program that prints the grid and lets the user open one door.
If there is an <strong>'X'</strong>, they get chocolate, otherwise they do not.
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
"calendar = [\n" +
"    ['X', '.', 'X', '.'],\n" +
"    ['.', 'X', '.', 'X'],\n" +
"    ['X', 'X', '.', '.'],\n" +
"    ['.', '.', 'X', 'X']\n" +
"]\n" +
"\n" +
"for row in calendar\n" +
"    print(' '.join(row))\n" +
"\n" +
"r = int(input('Row (0-3): '))\n" +
"c = int(input('Column (0-3): '))\n" +
"\n" +
"if calendar[r][c] == 'X'\n" +
"    print('You got chocolate!')\n" +
"else\n" +
"    print('Sorry, no chocolate today.')\n";

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
