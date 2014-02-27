## Server side capabilities
* Manipulate (create, read, update, delete) information from a database
* Maintain users / logins; remember information across sessions.
* Execute standard programming paradigms: __If...else statements__, __For loops__, __While loops__
* Send email
* Upload and manipulate files on a server
* Communicate with other sites
* Etc.

## Writing PHP

[php.net PHP Tags](http://us1.php.net/manual/en/language.basic-syntax.phptags.php)

To write PHP code in your files, start naming your files with the `.php` extension.
`.php` files are like super-powered `.html` files. They can run both html and PHP code.

PHP code is nested within `<?php` and `?>` tags or the shorthand `<?` and `?>` tags.

<small>Note: to use shorthand tags, the `short_open_tag` must be toggled on in your php.ini file which controls your PHP settings.</small>

Let's try out some code. Create a file called `logic.php` with this code:

	<?php
	$square = 4 * 4;
	?>

Here we created a variable called $sqare and set it to be 4 x 4. 
The semi-colon indicates the end of a command; this is called [instruction separation](http://us1.php.net/manual/en/language.basic-syntax.instruction-separation.php).

And create another file called `demo.php` with this code:

	<!DOCTYPE html>
	<html>
	<head>
		<?php require_once('logic.php'); ?>
	</head>
	
	<body>
	        The square of 4 is <?=$square?>
	</body>
	</html>

This file includes logic.php at the top, similarly to how you'd include in an external CSS or JS file.
Then, it prints the $square variable in the body.
Without worrying too much more about how this code works just yet, run it in your browser and do a <em>View Source</em>; what do you see?

## Separation of logic vs. display
PHP is going to serve two different roles on your pages. 

1. The __logic__, or brains, of  your site. Communicates with the database, run tests, crunch numbers, etc.
2. The __display__; this is the output that results from your logic.

If you wrote a complex script to calculate your company's profits for the month, that'd be the logic.
When you displayed the resulting profit number on the page, that'd be the display.

When working, we want to keep our logic and display as separate as possible which is why we separated the processing part of the PHP into it's own `logic.php` file which is then included in `demo.php`.

## PHP Error Reporting

[php.net error_reporting](http://php.net/manual/en/function.error-reporting.php)

Unlike HTML or CSS, PHP gives you feedback if your code has problems.

The feedback comes in the forms of Errors, Warnings and Notices.

Error reporting is set at a system level but can be overridden on the code level via the [error_reporting()](http://php.net/manual/en/function.error-reporting.php) function.

Example:

	<?php
	// Turn off all error reporting
	error_reporting(0);
	?>

Note, this command as the be placed at the very top of your file in order to work.

General rule:

* Project in development mode: all errors and warnings <em>on</em>.
* Project in production mode: all errors and warnings </em>off</em>.

## Commenting
[php.net Comments](http://us1.php.net/manual/en/language.basic-syntax.comments.php)

	// This is a single line comment
	
	/* This is a multi-line comment
	It can span
	Multiple lines
	*/
	
	// Coments can be used to leave notes to yourself, or disable lines of code
	// echo $results;
