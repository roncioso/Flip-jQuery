Flip!
=========

An easy to use jQuery plugin that allows you to flip elements in four directions.

Installation
--------------

Add the minified.js version of Flip! to your project and insert the following script tag (edit to the correct path) into the head section of your HTML document.

```html
<script src="[path to the file]/jquery.flip.min.js"></script>
```


Flip! requires the latest versions of [jQuery](http://jquery.com/download/) and [jQuery UI](http://jqueryui.com/download/) ; link the jQuery and jQuery UI script tags before Flip!.


Example
--------------
Here's a basic example to show you how to Flip!
```html
<html>
	<head>
		<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
		<script src="jquery-ui-1.11.0.custom/jquery-ui.min.js"></script>
		<script src="jquery.flip.min.js"></script>

	</head>
	<body>
		<div style= "border: 2px solid red; width: 20%; height: 40%">
			"Let's Flip this!"
		</div>
	</body>
	<script type="text/javascript">
		$("div").on("click", flipDiv)
		
		function flipDiv(){
			$("div").flip({
				direction:"tb",
				content: "We've been flipped!"
			})
		}
	</script>
</html>
```


