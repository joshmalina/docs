## Goal

To get some practical use with with the skills we've learned so far, lets program a page to be responsive to the time of day.

__Exercise: 
If the time is between 6am and 8pm, make the background of your page a light blue (i.e. day).
Otherwise, make the background of your page black (i.e. night).__

### Tip: Getting the time of day
For this, the `date()` function will come in handy.
What parameter would work best for the problem you're trying to solve?


### Tip: Timezones
You may encounter the time value you get as different from our timezone, based on how your server is configured. If that happens, check out `date_default_timezone_set()` ([ref](http://us2.php.net/date_default_timezone_set))


### Tip: Getting your PHP to talk to CSS:
Remember how we used this syntax to output PHP variables straight into our HTML?	
	
	<?=$background_color?>
	
You can do the same thing in internal CSS.

	<style type='text/css'>
	       body {
	           background-color:<?=$background_color?>
	        }
	</style>
