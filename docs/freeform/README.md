---
sidebar: auto
---
# Freeform

## Overall layout for Freeform

Target all styles with #freeform

```html
<!-- BRING HEADER FROM HOMEPAGE -->
<section id="slider">
  <ul class="bxslider">
    <li style="background: url('<!--INSERT SLIDER URL HERE-->')center no-repeat; background-size: cover"></li>
  </ul>
</section>
<main id="main">
  <!-- FLYOUT -->
  <!-- ENTRY and POST SECTION -->
</main>
<!-- BRING FOOTER FROM HOMEPAGE -->
```

## Flyout

```html
<aside id="flyout-wrap">
  <span class="flyout-header">Related Pages</span>
  <ul id="flyout">
    <li><a href="#">Mattis Venenatis Tortor</a></li>
    <ul>
      <li><a href="#">Mattis Venenatis Tortor</a></li>
      <li><a href="#">Dolor Consectetur Amet</a></li>
      <li><a href="#">Nullam Cras Ultricies Etiam</a></li>
    </ul>
  </ul>
</aside>
```

## Entry, Breadcrumbs and Post

### Entry

```html
<article class="entry">
  <div class="entry-header-wrap">
    <h2 class="entry-header-title">Interior Page Title Lorem Ipsum</h2>
    <!-- BREADCRUMBS WERE THEY NEED TO BE -->
  </div>
  <!-- /.entry-header-wrap -->
</article>
<!-- /.entry -->
```

### Breadcrumbs

```html
<div class="breadcrumbs">
  <a class="breadcrumbs-link" href="#">Home</a><a class="breadcrumbs-link" href="#">Parent Category</a><span class="breadcrumbs-current-page">Current Page</span>
</div>
<!-- /.breadcrumbs -->
```

### Post

```html
<div class="post">
  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta.</p>
  <img class="post-image" src="'<!-- INSERT URL TO IMAGE HERE -->'" alt="interior image">
  <span class="post-subheader">Header Two (H2)</span>
  <p>Sed posuere consectetur est at lobortis. Donec id elit non mi porta gravida at eget metus. Cras mattis consectetur purus sit amet fermentum. Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Maecenas sed diam eget risus varius blandit sit amet non magna. Nulla vitae elit libero, a pharetra augue. Morbi leo risus, porta ac consectetur ac, vestibulum at eros.Duis mollis, est non commodo luctus, nisi erat porttitor ligula, eget lacinia odio sem nec elit. Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Aenean lacinia bibendum nulla sed consectetur. Nullam quis risus eget urna mollis ornare vel eu leo. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec id elit non mi porta gravida at eget metus. Cras mattis consectetur purus sit amet fermentum. Integer posuere erat a ante venenatis dapibus posuere velit aliquet. Integer posuere erat a ante venenatis dapibus posuere velit aliquet. Donec ullamcorper nulla non metus auctor fringilla. Praesent commodo cursus magna, vel scelerisque nisl consectetur et.</p>
</div>
<!-- /.post -->
```