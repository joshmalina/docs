## Targeting an element on the page by its id
	
Vanilla JS:

	document.getElementById("lucy")
	
jQuery:

	$('#lucy')
	
## Targeting an element on the page by its class

Vanilla JS:

	document.getElementByClassName("ricardo")
	
jQuery:

	$('.ricardos')

## Targeting an element by its tag name

Vanilla JS:

	document.getElementByTagName("div")

JS with jQuery:

	$('div')

## Figure out what the src attribute

	<img src='western-hemisphere.jpg' id='map'>

Vanilla JS:

	var src = document.getElementById('map').src;
	
JS with jQuery:

	var src = $('#map').attr('src');

## Prepend text

	<div id='canvas'>
	     February 2012
	     March 2012
	     April 2012
	</div>
	
Vanilla JS:

	var existing_content = document.getElementById('canvas').innerHTML;

	document.getElementById('canvas').innerHTML = "March 2012<br>" + existing_content;
	
JS with jQuery:

	$('#canvas').prepend("March 2012");
