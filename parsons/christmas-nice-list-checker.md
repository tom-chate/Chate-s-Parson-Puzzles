---
layout: default
title: "Christmas: Nice List Checker"
---

<p class="task-description">
Santa has stored his Nice List in a text file called <strong>nice_list.txt</strong>.
Write a program that reads the file and checks if the user is on the Nice List.
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
"file = open('nice_list.txt', 'r')\n" +
"names = file.read().splitlines()\n" +
"file.close()\n" +
"\n" +
"name = input('Enter your name: ')\n" +
"\n" +
"if name in names\n" +
"    print('You are on the Nice List!')\n" +
"else\n" +
"    print('You are not on the Nice List yet.')\n";

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
