## User defined

[php.net user-defined functions](http://us2.php.net/manual/en/functions.user-defined.php)

Functions are bits of reusable code we can use in our programs. If you have a common task you need to repeat 100 times throughout your application, it'd make sense to store that task in a function so you can call it whenever you need it.

	<?php
	function calculate_total($subtotal, $discount, $shipping_method) {
		
		if($shipping_method == 'priority') {
			$shipping_rate = 5;
		}
		elseif($shipping_method == 'express') {
			$shipping_rate = 15;
		}
		
		$tax = .09 * $subtotal;
		
		$total = $subtotal + $shipping_rate - $discount;
		
		return $total;
		
	}
	?>
	
We could then call this function like so:

	Your total is <?=calculate_total(10,3,'priority')?>

Functions accept __parameters__ which are extra bits of info a function may use to get its job done. In this case the parameters were *subtotal*, *discount* and *shipping method*. 

It is not required that functions accept parameters. If no parameters are needed, don't enter anything in between the quotes after the function name.

Example:

	<?php
	function pick_a_random_number() {
		return rand(1,100);
	}
	?>





## Built-in functions
[php.net built-in/internal functions](http://us2.php.net/manual/en/functions.internal.php)
In addition to creating your own functions, PHP has many useful built-in functions.

Here's an examples of the built in [date()](http://us2.php.net/manual/en/function.date.php) function:

logic.php:

	<?php 
	$day = date('g');
	?>

In the `<body>` of demo.php:

	Today is <?=$day?>
	
Based on the documentation for the `date()` function, what does the `g` parameter represent?