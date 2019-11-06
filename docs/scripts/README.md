---
sidebar: auto
---
# Helpful Scripts

## Pull Left or Right

### Left
```js
function fillLeft() {
    var bodyWidth = $('body').outerWidth();
    // Make sure this is targeting
    // the container the element is in
    var pixelValue = (bodyWidth - $('.container').width()) / 2;

    $('INSERT TARGET HERE').css('margin-left', -pixelValue);
    $('INSERT TARGET HERE').css('padding-left', pixelValue);
}
fillLeft();
$window.resize(fillLeft);
```

### Right

This is the same as above but just changed to the right instead of left...

```js
function fillRight() {
    var bodyWidth = $('body').outerWidth();
    // Make sure this is targeting
    // the container the element is in
    var pixelValue = (bodyWidth - $('.container').width() / 2 );

    $('INSERT TARGET HERE').css('margin-right', -pixelValue);
    $('INSERT TARGET HERE').css('padding-right', pixelValue);
}
fillRight();
$window.resize(fillRight);
```

### Both

Hopefully you should know how to make this by looking at the above... Ill give you the starter code...

```js
function fillBoth() {
    // Fill out the rest
}
fillBoth();
$window.resize(fillBoth);
```

## Sticky

Here is the basics of a better sticky script instead of the one in the framework

```c
.fixed-nav header {
    width:100%;
    top:0;
    right:0;
    position:fixed;
}
```

```js
var nav = document.querySelector('header');
var topOfNav = nav.offsetTop;

function fixNav() {
    if (window.pageOffsetY >= topOfNav) {
        document.body.style.paddingTop = nav.offsetHeight + 'px';
        document.body.classList.add('fixed-nav');
    } else {
        document.body.classList.remove('fixed-nav');
        document.body.style.paddingTop = 0;
    }
}

window.addEventListener('scroll', fixNav);
```

## Translate

```html
<div id="google-translate" class="control hidden-sm hidden-xs">
    <script type="text/javascript">
        function googleTranslateElementInit() {
            new google.translate.TranslateElement({pageLanguage: 'en', layout: google.translate.TranslateElement.InlineLayout.SIMPLE}, 'google-translate');
        }
    </script>
    <script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>
</div>
```
Base styles for translate
```css
/*! removes styling from the translate */
#google-translate .goog-te-gadget-simple{border:0}
#google-translate .goog-te-menu-value{margin:0}
#google-translate .goog-te-menu-value>*{display:none}
#google-translate .goog-te-menu-value>span:first-of-type{display:block;font-size:0}
/*! for adding an icon before the alternate text */
#google-translate .goog-te-menu-value>span:first-of-type:before{content:'\f0ac';font-size:14px;font-family:FontAwesome}
/*! for changing the text in the translate */
#google-translate .goog-te-menu-value>span:first-of-type:after{content:'Translate';font-size:14px}
#google-translate img{display:none}
```

## Owl Carousel

```js
if(typeof $.fn.owlCarousel !== 'undefined') {
    var quickLinksLength = $('YOUR TARGET HERE');
    $('OWL CAROUSEL CONTAINER HERE').owlCarousel({
        items: NUMBERS_OF_ITEMS_TO_BE_SHOWN_ON_SCREEN,
        // OPTIONAL DEPENDENT ON DESIGN
        // nav: true,
        // THESE WILL GIVE YOU THE RIGHT AND LEFT ARROWS
        // navText: ["<i class='fa fa-chevron-left'></i>", "<i class='fa fa-chevron-right></i>'"],
        responsive: {
            // EX: SET TO WHAT YOU WILL NEED
            992: {
                items: NUMBER
            },
            669: {
                items: NUMBER
            },
            430: {
                items: NUMBER
            },
            0: {
                items: NUMBER
            }
        }
    });
}
```

## Add Icons to Nav

If nav has images for each link

```js
$('#nav-icons>img').each(function() {
    $(this).clone().prependTo($('#nav>li').eq($(this).index()).children('a'));
});
```

```html
<div id="nav-icons" class="hidden">
    <img class="nav-img" src="_assets_/images/ICON YOU WANT HERE"  alt="ENTER ALT HERE"/>
    <img class="nav-img" src="_assets_/images/ICON YOU WANT HERE" alt="ENTER ALT HERE"/>
    <img class="nav-img" src="_assets_/images/ICON YOU WANT HERE" alt="ENTER ALT HERE" />
</div><!--/#nav-icons.hidden-->
```

## Google Translate Issue with qlinks

### Issue

Google translate will try to translate both the anchor tag, and the images/span tags inside of the link, causing duplication's and strange behavior.

### Solution

The solution is to give an attribute of `translate="no"` and a class of `notranslate` to the anchor tag. Then you need to add the attribute of `translate="yes"` and the class of `translate` to any span tag inside of the anchor tag.

### Example

```html
<a href="#" class="quick-links notranslate" translate="no">
    <img src="_assets_/images/image.png" alt="Quick Link Image" class="notranslate" translate="no">
    <span class="translate" translate="yes">This will be translated properly</span>
</a>
```

## Fixed Scroll
    with smooth scrolling
```js
 var y = $(window).scrollTop();
 $('html, body').animate({
     scrollTop: y + $(window).height();
 }, 1000);
```

## Responsive Calendar

finds the height of the miniBody and adds 5px padding to the bottom to allow better responsiveness

```js
// start calendar resize handler
	function resizeIframe(height) {
		var iFrameID = document.getElementById('calendar');
		if(iFrameID) {
				// here you can set the height, I delete it first, then I set it again
				iFrameID.height = "";
				iFrameID.height = height;
		}
		console.log("height to: " + height);
	}
	var eventMethod = window.addEventListener
	? "addEventListener"
	: "attachEvent";
	var eventHandler = window[eventMethod];
	var messageEvent = eventMethod === "attachEvent"
		? "onmessage"
		: "message";
	eventHandler(messageEvent, function (e) {

		if( e.data && e.data[0] === "setCalHeight" )
		{
			if(typeof resizeIframe === 'function'){
				resizeIframe(e.data[1]);
			}

		}

	});
	// end calendar resize handler
```

## Slider Height Responsive

responsive slider height to keep items "Above the Fold"

```js
    function heroHeight(){
        var windowHeight = $(window).outerHeight();
        $('.main-page #header-wrap').height(windowHeight)
    }
    heroHeight();
    $window.load(heroHeight);
    $window.resize(heroHeight);
```
