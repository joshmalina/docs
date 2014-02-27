Challenge: Create a simple addition calculator
<img src='http://making-the-internet.s3.amazonaws.com/js-calculator.png'>

[Final example](/examples/_js/calculator/calculator.html)

[The guts (css, js, html)](/examples/_js/calculator/)


### Hints

The JavaScript [eval()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/eval) method can be used to calculate values. For example, in the following statement, `total` would be set to 2.

	var total = eval(1+1);
	
Knowing this, you can calculate the value the user has entered in by running eval on what is in the display box:
	
	var total = eval( $('#display').html() );

<small>
Security FYI: Because our input is coming from a controlled source (buttons we program), using eval() is okay. Note though, that you never want to use eval() when prcessing input a user enters (such as in a text field) because the user could enter malicious code that your JS would then process. ([Read more here...](http://stackoverflow.com/questions/6479236/calculate-string-value-in-javascript-not-using-eval))
</small>



