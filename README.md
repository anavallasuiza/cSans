cSans CSS framework
===================

Created by Oscar Otero <http://oscarotero.com> <http://anavallasuiza.com> <oom@oscarotero.com>

cSans is a css framework focused to work with css3 and html5. Supported only by modern browsers and IE8+.

Features:

* Support for all HTML5 modern browsers, mobiles and IE8+
* Provides a CSS normalizer to unify all default styles across all browsers
* Provides some universal helpers (image replacement, show/hidden, etc) for generic needs.
* Provides some universal css styles for ui widgets (buttons, links)


CSS normalizer
--------------

The file "csans.css" contains a solid reset and normalize for all html elements bringing a strong base to build. So if you only need a css reset you can include just this file

Helpers
-------

The file "csans.helpers.css" contains some helpers for generical purposes:

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

The main purpose of the ui classes is to provide some basic css rules to build your own ui widgets. It's not a framework with predefined styles (like bootstrap, jquery.ui, etc), but it's a collection of some css classes that you can extend and customize. In tests/ui.html you can see some examples.

* .button Generic class to build a button using any html element (button, span, link, input, etc). Using .button-select, you can create a simple dropdown with a select element with pure css.
* .link It's a generic class to build link-style elements. It's like .button, but for links. You can create links also with selects and there is the .link-select class to create a dropdown element with link appearance.
