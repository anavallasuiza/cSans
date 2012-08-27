cSans CSS framework
===================

Created by Oscar Otero <http://oscarotero.com> <http://anavallasuiza.com> <oom@oscarotero.com>

GNU Affero GPL version 3. http://www.gnu.org/licenses/agpl-3.0.html

cSans is a css framework focused to work with css3 and html5. Supported only by modern browsers and IE8+.

Features:

* Support for all modern browsers, mobiles and IE8+
* Support for HTML5
* Solid CSS reset
* Some universal CSS helpers

What cSans is
-------------

* Provides a CSS reset for unify all default styles across all modern browsers
* Provides some universal helpers (image replacement, show/hidden, etc) for generic needs.
* Provides a universal style (inspired in http://stuffandnonsense.co.uk/blog/about/universal_internet_explorer_6_css/) for old browsers. 

What cSans is not
-----------------

* Not predefined look and feel. Just only reset basic styles
* Not a grid system. It's not good idea for responsive web
* Not predefined widgets (buttons, forms, etc).


CSS reset
---------

The file "csans.css" contains a solid reset for all html5 elements and brings a strong base to build. So if you only need a simple css reset you can include just this file

Helpers
-------

In the file "csans.helpers.css" there are some helpers for generical purposes:

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

* Change the display property using .inline, .block or .inline-block
* Apply the clearfix using .clear
* Hide elements using .hidden, .hidden-a11y (maintaining the accesibility) or .invisible (keep the space)
* In ul elements, you can change the list-style-type using .square, .disc, .decimal, .lower-alpha, .upper-alpha, .lower-roman, .upper-roman

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
