# csans

Created by Oscar Otero <http://oscarotero.com> <oom@oscarotero.com>

License: MIT

This project contains a set of opinionated css classes that you can use in your web projects. Support for all HTML5 modern browsers, mobiles and IE9+


## Image replacement

Use the class `image` combinated with other class providing the image, with and height. Example:

```css
.logo {
	background-image: url('my-logo.png');
	width: 300px;
	height: 300px;
}
```

```html
<span class="image logo">My logo</span>

<span class="image logo"><a href="#">My logo with link</a></span>
```

## Aspect ratio

Keeps the aspect ratio of `<iframes>`, `<embed>` or any other element while make them elastic:

```html
<div class="aspect-ratio aspect-ratio-16-9">
	<iframe src="youtube-content.html">
</div>

<!-- By default is applied only to iframe, object and embed, but you can apply to other elements (divs, imgs, videos, etc) using the class .aspect-ratio-target -->
<div class="aspect-ratio aspect-ratio-4-3">
	<div class="aspect-ratio-target">This div has an aspect ratio of 4/3</div>
</div>
```

# Buttons

`.button` is a generic class that you can extend to build a button using any html element (button, span, link, input, etc). Using `.button-select`, you can create a simple dropdown with a select element with pure css.

# Links

`.link` is a generic class to build link-style elements. It's like .button, but for links. You can create links also with selects and there is the `.link-select` class to create a dropdown element with link appearance.


# Other classes:

* `.clear` To apply the clearfix
* `.hidden, .invisible, .visuallyhidden` Various ways to hide elements
