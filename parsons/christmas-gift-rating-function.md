---
layout: default
title: "Christmas: Gift Rating Function"
---

<p class="task-description">
Santa wants to rate gifts based on their price.
Write a function that returns <strong>'Budget gift'</strong>, <strong>'Standard gift'</strong> or <strong>'Luxury gift'</strong>
depending on the price, then use it to rate three gifts.
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
"def rate_gift(price)\n" +
"    if price < 10\n" +
"        return 'Budget gift'\n" +
"    elif price <= 50\n" +
"        return 'Standard gift'\n" +
"    else\n" +
"        return 'Luxury gift'\n" +
"\n" +
"for i in range(3)\n" +
"    value = float(input('Enter gift price: '))\n" +
"    rating = rate_gift(value)\n" +
"    print('£' + str(value), '→', rating)\n";

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
