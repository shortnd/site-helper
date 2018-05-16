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
    $('INSERT TARGET HERE').css('padding-right', -pixelValue);
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
.sticky {
    position: fixed;
    width: 100%;
    top: 0 /* Or offset if there is a topbar */
}
```

```js
$(function() {
    $(window).scroll(function() {
        if($(this).scrollTop() > ENTER_DESIRED_HEIGHT_HERE) {
            $('TARGET TO ADD STICKY CLASS TO').addClass('sticky');
            // Add a padding to the rest of the document to offset the results
            // of the nav bar becoming fixed and not covering any elements
            $('.main-wrap').css({'padding-top': 'ENTER AMOUNT TO OFFSET HERE'});
        } else {
            $('TARGET TO REMOVE STICKY CLASS FROM').removeClass('sticky');
            // Remove the added padding
            $('.main-wrap').css({'padding-top': ''});
        }

        });
    });
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

