---
sidebar: auto
---
# Main / Home Page

## Over All Layout For Main

```html
<header>
  <!-- TOP BAR IF NEEDED -->
  <!-- TOGGLES FOR MOBILE -->
  <!-- ROW FOR NAVBAR AND LOGO -->
</header>
<section id="slider">
<!-- AND OTHER ELEMENTS TO INCLUDE WITHIN OR OVER THE SLIDER -->
</section><!--/.slider-->
<main>
<!-- QLINKS -->
<!-- OTHER OPTIONAL SECTIONS -->
<!-- WELCOME OR FREEFORM SECTION with CONTROLS -->
<!-- SIGNUP SECTION -->
</main>
<footer>
<!-- COPY RIGHT INFO AND REVIZE INFO/LOGIN -->
</footer>
```

## Header and Navbar

```html
<!-- IN HEADER TAG -->

<div class="container">
  <div class="row">
    <div class="col-md-2 logo">
      <a href="#" id="logo">
        <img src="_assets_/images/logo.png" alt="navigation logo">
      </a><!--/#logo-->
    </div><!--/.col-md-2-->
    <nav class="col-md-8 text-right">
      <ul id="nav">
        <li>
          <a href="#">home</a>
        </li>
        <li>
          <a href="#">departments</a>
          <ul>
            <li>
              <a href="#">First-level dropdown</a>
            </li>
            <li>
              <a href="#">First-level dropdown</a>
              <ul>
                <li>
                  <span>Second-level dropdown</span>
                </li>
                <li>
                  <a href="#">Second-level dropdown</a>
                </li>
                <li>
                  <span>Second-level dropdown</span>
                </li>
                <li>
                  <a href="#">Second-level dropdown</a>
                </li>
                <li>
                  <span>Second-level dropdown</span>
                </li>
                <li>
                  <a href="#">Second-level dropdown</a>
                </li>
              </ul>
            </li>
            <li>
              <span>First-level dropdown</span>
            </li>
            <li>
              <a href="#">First-level dropdown</a>
            </li>
            <li>
              <span>First-level dropdown</span>
            </li>
            <li>
              <a href="#">First-level dropdown</a>
            </li>
          </ul>
        </li>
        <li>
          <a href="#">staff directory</a>
        </li>
        <li>
          <a href="#">FAQ</a>
        </li>
        <li>
          <a href="#">how do i?...</a>
        </li>
      </ul><!--/#nav-->
    </nav><!--/.col-md-8.text-right-->
  </div><!--/.row-->
</div><!--/.container-->

<!-- IN HEADER TAG -->
```

### Logo

```html

<div class="col-md-2">
  <a href="#" id="logo">
    <img src="_assets_/images/logo.png" alt="navigations logo">
  </a><!--/#logo-->
</div><!--/.col-md-2-->

```

Make sure to position the Logo absolute example to start off with

```scss

#logo img {width: 144px; position: absolute; max-width: inital; left: 10px; top: 55px}

```

### Top Bar

```html
<section id="top-bar">
  <div class="container">
    <div class="row">
      <!-- INSERT WHAT IS NEEDED HERE -->
    </div><!--/.row-->
  </div><!--/.container-->
</section><!--/#top-bar-->
```


### Mobil Search and Nav

```html
<div class="hidden-lg hidden-md">
  <div id="nav-toggle" class="fa fa-bars mobile-nav"></div>
  <div id="search-toggle" class="fa fa-search"></div>
</div>
```

## Controls

```html
<section class="controls">
  <div class="controls-search">
    <!-- SEARCH SECTION -->
  </div>
  <div class="controls-translate">
    <!-- TRANSLATE GOES HERE -->
  </div>
  <div class="controls-social">
    <!-- SOCIAL GOES HERE -->
  </div>
</section>
<!-- /.controls -->
```

### Search

```html
<div id="search">
  <form class="search-form" method="get" action="search.php">
    <input name="q" class="form-control search-input" placeholder="Search..." type="search" id="search-input">
    <button>Search</button>
  </form><!--/.search-form-->
</div><!--/#search-->
```

### Translate

```html
<div id="google-translate" class="control hidden-sm hidden-xs">
  <script type="text/javascript">
    function googleTranslateElementInit() {
      new google.translate.TranslateElement({pagelanguage: 'en',
        layout: google.translate.TranslateElement.InlineLayout.SIMPLE},
        'google-translate');
    }
  </script>
  <script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>
</div><!--/#google-translate.control.hidden-sm.hidden-xs-->
```

### Social

```html
<a href="#">
  <i class="fa fa-facebook controls-social-facebook"></i>
</a>
<a href="#">
  <i class="fa fa-twitter controls-social-twitter"></i>
</a>
<a href="#">
  <i class="fa fa-youtube-play controls-social-youtube"></i>
</a>
```

### Weather

```html
<div id="weather" class="weather">
</div><!--/#weather.weather-->
```


## Bxslider or Slider

```html
<!-- IN SLIDER SECTION -->
<ul class="bxslider">
  <li style="background: url('<!--INSERT LOCATION OF SLIDE HERE-->') center no-repeat; background-size: cover;">
    <div class="container slider-caption">
      <h2>Some Text</h2>
      <span>Some descriptive text</span>
    </div><!--/.container-slider-caption-->
  </li>
</ul><!--/.bxslider-->
<!-- IN SLIDER SECTION -->
```

## Quicklinks and Owl Slider

Depends on website if its an owl slider of not.

```html
<!-- USUALLY IN THE MAIN SECTION -->
<div id="quick-links-wrap">
  <div class="container">
    <section id="quick-links">
      <a href="#" class="quick-links-item">
        <img src="_assets_/images/quick-links-image-1.png" alt="">
        <span>employment</span>
      </a><!--/.quick-links-item-->
      <a href="#" class="quick-links-item">
        <img src="_assets_/images/quick-links-image-2.png" alt="">
      </a><!--/.quick-links-item-->
    </section><!--/#quick-links-->
  </div><!--/.container-->
</div><!--/#quick-links-wrap-->
<!-- USUALLY IN THE MAIN SECTION -->
```

If its not a owlsider use css grid

```scss
#qlinks-wrap {
  -moz-column-count: 3;
  -webkit-column-count: 3;
  -ms-column-count: 3;
  -o-column-count: 3;
  column-count: 3;
  -moz-column-gap: 10px;
  -webkit-column-count: 10px;
  -ms-column-count: 10px;
  -o-column-count: 10px;
  column-gap: 10px;
}
/*------------------------------
Then adjust the qlinks how you need
------------------------------*/
```

## Main section

```html
<main id="main">
  <div class="news-events-wrap">
    <div class="news">
    <!-- NEWS GOES HERE -->
    </div>
    <!-- /.news -->
    <div class="events">
    <!-- EVENTS GOES HERE -->
    </div>
    <!-- /.events -->
  </div>
  <!-- /.news-events-wrap -->
</main>
<!-- /#main -->
```

## News section

```html
<div class="news-header-wrap">
  <h2 class="news-header-title">Latest News</h2>
  <span class="news-header-caption">Stay up to date</span>
</div>
<!-- /.news-header-wrap -->
<div class="news-list">
  <div class="news-list-item">
    <div class="news-list-item-date">
      March 23, 2018
    </div>
    <!-- /.news__list-item-date -->
    <h3 class="news-list-item-title">Post Title Magna Purus Condimentum Justo Tortor</h3>
    <!-- /.news__list-item-title -->
    <div class="news-list-item-caption">
    Duis mollis, est non commodo luctus, nisi erat porttitor ligula, eget lacinia odio sem nec elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit... <a href="#" class="news-list-item-link">Read more</a>
    </div>
    <!-- /.news-list-item-caption -->
  </div>
  <!-- /.news-list-item -->
</div>
<!-- /.news-list -->
```

## Events / Calendar

```html
<div class="col-md-6">
  <div class="events">
    <div class="events-header-wrap">
      <h2 class="events-header-title">Upcoming Events</h2>
      <span class="events-heading-caption">Whats happening</span>
    </div>
    <!-- /.events-header-wrap -->
    <div class="events-calendar-wrap">
      INSERT CALENDAR HERE
      <!-- INSERT CALENDAR HERE -->
    </div>
    <!-- /.events-calendar-wrap -->
  </div>
  <!-- /.events -->
</div>
<!-- /.col-md-6 -->
```

## Footer

```html
<footer>
  <div class="container">
    <div class="row">
      <div class="col-md-6 copyright">
        <p>&copy;&nbsp;&nbsp; CITY NAME HERE</p>
      </div>
      <!-- /.col-md-6.copyright -->
      <div class="col-md-6 revize text-right">
        <span class="powered-by-revize">Powered by <a href="http://www.revize.com" target="_blank" id="powered-by-revize-link">Revize</a></span> <a id="revize-login-link" href="#">Login</a>
      </div>
      <!-- /.col-md-6.revize.text-right -->
    </div>
    <!-- /.row -->
  </div>
  <!-- /.container -->
</footer>
```

Footer with a background image

```html
<footer style="background: url('<!-- INSERT URL HERE -->') center no-repeat; background-size: cover;">
  <div class="container">
    <div class="row">
      <div class="col-md-6 copyright">
        <p>&copy;&nbsp;&nbsp; CITY NAME HERE</p>
      </div>
      <!-- /.col-md-6.copyright -->
      <div class="col-md-6 revize text-right">
        <span class="powered-by-revize">Powered by <a href="https://revize.com" target="_blank" id="powered-by-revize">Revize</a></span> <a href="#" id="revize-login-link">Login</a>
      </div>
      <!-- /col-md-6.revize.text-right -->
    </div>
    <!-- /.row -->
  </div>
  <!-- /.container -->
</footer>
```

### Footer Mega Menu

```html
<div class="col-md-9 footer-mega-links">
  <div class="footer-mega-links-header">
    <span class="footer-mega-links-header-title">Links</span>
  </div>
  <!-- /.footer-mega-links-header -->
  <div class="footer-mega-links-wrap">
    <ul id="footer-mega">
      <li>
        <a href="#">Link</a>
      </li>
      <li>
        <a href="#">Link</a>
      </li>
      <li>
        <a href="#">Link</a>
      </li>
      <li>
        <a href="#">Links</a>
      </li>
      <li>
        <a href="#">Links</a>
      </li>
      <li>
        <a href="#">Link</a>
      </li>
      <li>
        <a href="#">Link</a>
      </li>
      <li>
        <a href="#">Link</a>
      </li>
      <li>
        <a href="#">Links</a>
      </li>
      <li>
        <a href="#">Links</a>
      </li>
      <li>
        <a href="#">Link</a>
      </li>
      <li>
        <a href="#">Link</a>
      </li>
      <li>
        <a href="#">Link</a>
      </li>
      <li>
        <a href="#">Links</a>
      </li>
      <li>
        <a href="#">Links</a>
      </li>
      <li>
        <a href="#">Link</a>
      </li>
      <li>
        <a href="#">Link</a>
      </li>
      <li>
        <a href="#">Link</a>
      </li>
      <li>
        <a href="#">Links</a>
      </li>
      <li>
        <a href="#">Links</a>
      </li>
    </ul>
  </div>
  <!-- /.footer-mega-links-wrap -->
</div>
<!-- /.col-md-9.footer-mega-links -->
```

CSS for Mega Footer

```css
#footer-mega {
  margin: 0;
  -moz-column-count: 4;
  -webkit-column-count: 4;
  column-count: 4;
  -webkit-column-gap: 50px;
  -moz-column-gap: 50px;
  column-gap: 50px;
  padding: 20px 0 0 0;
}
```
