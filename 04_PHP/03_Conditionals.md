## Control structures

[php.net if](http://us1.php.net/manual/en/control-structures.if.php)
[php.net else](http://us1.php.net/manual/en/control-structures.else.php)
[php.net elseif](http://us1.php.net/manual/en/control-structures.elseif.php)

HTML code is fairly static and "brainless"; what you type is what you get. With PHP, however, we're going to write code that allows our program to "think".





## If statements
With If...Else statements we can build code that makes decisions.

logic.php:

	<?php
	$age = 10;
	
	if($age <= 18) {
	   $person_type = "kiddo";
	}
	else {
	   $person_type = "adult";
	}
	?>

In the `<body>` of demo.php:

	You're a <?=$person_type?>
	
In this example, our code first asks the question... is age less than or equal to 18? 
If yes, execute the next line of code which sets the `$person_type` to be "kiddo"
If no, execute what follows the else statement, which sets the `$person_type` to be "adult"

Note the use of parentheses ( ) and curly brackets { } in writing If...Else statements:

* The parentheses ( ) surrounds the test or question we're asking.
* The curly brackets { }  surrounds the code that will be executed If that test is passed.

Lets take this a step further: Our If...Else statement can ask multiple questions:

logic.php:

	<?php
	$age = 100;
	
	if($age < 12) {
	   $person_type = "kiddo";
	}
	elseif($age > 12 AND $age <= 19) {
	   $person_type = "teenager";
	}
	elseif($age > 19 AND $age <= 80) {
		$person_type = "adult";
	}
	else {
		$person_type = "super wise person";
	}
	?>

In the `<body>` of demo.php

	You're a <?=$person_type?>
	
Play around with this code changing the value of the `$age` variable to see if you can get it to hit every case.


Note how we use the `AND` to say that <em>both</em> conditions must be true in order to pass. Sometimes you might want to use an `OR` for a test if only one condition needs to pass.

For example:

	<?php
	if($age >= 21 OR $parents == NULL) {
	   $person_type = "adult";
	}
	?>
	
`AND`/`OR` are examples of [logical operators](http://php.net/manual/en/language.operators.logical.php).

