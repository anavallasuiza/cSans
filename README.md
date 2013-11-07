cSans CSS framework
===================

Created by Oscar Otero <http://oscarotero.com> <http://anavallasuiza.com> <oom@oscarotero.com>

GNU Affero GPL version 3. http://www.gnu.org/licenses/agpl-3.0.html

cSans is a css framework focused to work with css3 and html5. Supported only by modern browsers and IE8+.

Features:

* Support for all modern browsers, mobiles and IE8+
* Support for HTML5
* Provides a CSS reset for unify all default styles across all modern browsers
* Provides some universal helpers (image replacement, show/hidden, etc) for generic needs.
* Provides some universal css styles for ui widgets (buttons, etc)
* Provides a universal style (inspired in http://stuffandnonsense.co.uk/blog/about/universal_internet_explorer_6_css/) for old browsers.


CSS reset
---------

The file "csans.css" contains a solid reset and normalize for all html elements bringing a strong base to build. So if you only need a css reset you can include just this file

Helpers
-------

The file "csans.helpers.css" contains some helpers for generical purposes:

* Float the elements using .left, .right or .right-right (Floats the element and align its contain to right)
* .image: Image replacement. You must specify the width, height and background-image:

```CSS
.logo {
	background-image: url('my-logo.png');
	width: 300px;
	height: 300px;
}
```

```HTML
<span class="image logo">My logo</span>

<span class="image logo"><a href="#">My logo with link</a></span>
```

* Apply the clearfix using .clear
* Hide elements using .hidden, .visually-hidden (visible only for screen readers) or .invisible (keep the space)
* .no-appearance Displays the input[type="search"] in webkit like the rest of the browsers
* .aspect-ratio Keeps the aspect ratio of iframes or flash elements while make them elastic:

```HTML
<div class="aspect-ratio aspect-ratio-16-9">
	<iframe src="youtube-content.html">
</div>

<!-- By default is applied only to iframe, object and embed, but you can apply to other elements (divs, imgs, videos, etc) using the class .aspect-ratio-target -->
<div class="aspect-ratio aspect-ratio-4-3">
	<div class="aspect-ratio-target">This div has an aspect ratio of 4/3</div>
</div>
```

UI
--

The main purpose of the ui classes is to provide some basic css rules to build your own ui widgets. It's not a framework with predefined styles (like bootstrap, jquery.ui, etc), but it's a collection of some css clases that you can extend and customize. In tests/ui.html you can see some examples.

* .button Generic class to build a button using any html element (button, span, link, input, etc). Using .button-select, you can create a simple dropdown with a select element with pure css.
* .link It's a generic class to build link-style elements. It's like .button, but for links. You can create links also with selects and there is the .link-select class to create a dropdown element with link appearance.

Universal styles
----------------

People with old browsers (ie7, ie6 or even ie5) should access to web content but it's difficult to create a great interface that works in these browsers. It's better create a simple universal style for these browsers that provides a more confortable way to access to de content:

```html
<!--[if gte IE 8]><!-->
<link href="csans.css" type="text/css" rel="stylesheet" />
<link href="csans.helpers.css" type="text/css" rel="stylesheet" />
<!-- <![endif]-->

<!--[if lte IE 7]>
<link href="csans.universal-styles.css" type="text/css" rel="stylesheet" />
<![endif]-->
```
