Flip-jQuery v0.9.9++
====================

What is Flip?
-------------

Flip is a jQuery plugin that will flip easily your elements in four directions.


How to use?
-----------

Like every jquery plugin, just chain it:

    $("#flipbox").flip({
    	direction:'tb'
    })


How to change content?
----------------------

Add content params in this way:

    $("#flipbox").flip({
    	direction:'tb',
    	content:'this is my new content'
    })


How to add callbacks?
---------------------

There are three available callbacks: onBefore, onAnimation, onEnd

    $("#flipbox").flip({
    	direction:'tb',
    	onBefore: function(){
    			console.log('before starting the animation');
    	},
    	onAnimation: function(){
    			console.log('in the middle of the animation');
    	},
    	onEnd: function(){
    			console.log('when the animation has already ended');
    	}
    })


How to revert a flip?
---------------------

There's an "hidden" method called revertFlip: as it says, revert a flip to the previous state

    $("#flipbox").revertFlip()


Some options
------------

Here are all options available:

* content       - define the new content of the flipped box. It works with: html, text or a jQuery object ex:$("selector")
* direction     - the direction where to flip. Possible values: 'tb', 'bt', 'lr', 'rl' (default: 'tb')
* color         - Flip element ending background color (default: '#999')
* speed         - Speed of the two parts of the animation (default: 500)
* onBefore      - Synchronous function excuted before the animation starts
* onAnimation   - Synchronous function excuted at half animation
* onEnd         - Synchronous function excuted after animation's end


Other options
-------------

* bgColor           - the inital (pre-flip) background color (default: the targets 'background-color' OR '#999')
* dontChangeColor   - does not apply the 'color' option to the finished result (default: false)


Methods
-------

* revertFlip()
* flip()
