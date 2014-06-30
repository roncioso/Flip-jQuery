Flip!
=========

An easy to use jQuery plugin that allows the flipping of elements in one of four directions.

Installation
--------------

Add the minified.js version of Flip! to your project and insert the following script tag (edit to the correct path) into the head section of your HTML document.

```html
<script src="[path to the file]/jquery.flip.min.js"></script>
```


Flip! requires the latest versions of [jQuery](http://jquery.com/download/) and [jQuery UI](http://jqueryui.com/download/) ; link the jQuery and jQuery UI script tags before the minified Flip.js.


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
		<button class = "flip">Flip</button>
		<div style= "border: 2px solid red; width: 20%; height: 40%" class = "box">
			"Let's Flip this!"
		</div>
		<button class = "flipBack">Flip Back</button>
	</body>
	<script type="text/javascript">
		$(".flip").on("click", flipDiv)
		$(".flipBack").on("click", flipBack)

		function flipDiv(){
			$(".box").flip({
				direction:"tb",
				content: "We've been flipped!",
				color: "blue",
				speed: 100
			})
		}

		function flipBack(){
			$(".box").revertFlip()
		}
	</script>
</html>
```

Options
--------------
```js
$(".box").flip({
	direction:"tb",
	content: "We've been flipped!",
	color: "blue",
	speed: 100,
	onBefore: console.log("Have not flipped yet"),
	onAnimation: console.log("We are flipping"),
	onAfter: console.log("We finished flipping")
})


```


There are many ways to customize the flip effect. Within the "flip" function you can add various options to change the flip to your liking. Below are the listed options.

####content
Defines the new content of the flipped box. It works with: html, text or a jQuery object ex:$("selector"). In the example above, the div reads "Let's flip this!" however, after the click, the div reads "We've been flipped!"
####direction
The direction where to flip. Possible values: 'tb', 'bt', 'lr', 'rl'. The default direction is tb. 
####color
After the flip, the background will change to this color. In the example above the div is white however changes to blue after the flip.
####speed
Speed of the two parts of the animation. Accepts a range of numbers; the smaller the number, the faster the flip. The default speed is 500.
####onBefore
Synchronous function excuted before the animation starts.
####onAnimation
Synchronous function excuted at half animation.
####onEnd
Synchronous function excuted after animation's end.

revertFlip()
--------------
Included is a revertFlip function that allows you to revert a flip. In the example above, clicking the flipBack button will change the div back to its original content.

######note as of June 30th, 2014 you are unable to revert back to an original state after multiple successive flips.