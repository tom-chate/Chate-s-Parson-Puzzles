---
layout: default
title: "Christmas: Toy Stock Table"
---

<p class="task-description">
Santa has three workshops and three types of toys.
A 2D list stores the stock levels.
Write a program that asks for a workshop and toy, then outputs the stock level.
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
"stock = [\n" +
"    [10, 5, 3],\n" +
"    [4, 8, 2],\n" +
"    [7, 2, 9]\n" +
"]\n" +
"\n" +
"workshop = int(input('Workshop (0=NP,1=EU,2=UK): '))\n" +
"toy = int(input('Toy (0=Teddy,1=Bike,2=Game): '))\n" +
"\n" +
"amount = stock[workshop][toy]\n" +
"print('Stock level:', amount)\n";

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
