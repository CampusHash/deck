title: Slide Title
subtitle: Subtitle
class: image

![CampusHash](images/campushash_icon_128.png)

---

title: Special Slide
subtitle: Subtitle
class: segue dark nobackground

---

title: Elements
class: big
build_lists: false

This is an unordered list:

- Bullet1
- Bullet2
- Bullet3

This is __bold__. This is _italic_.

---

title: No Background
class: nobackground fill

![CampusHash](images/campushash_icon_128.png)

<footer class="source">source: place source info here</footer>

---

title: Big Title Slide
class: title-slide

This is a title with the event branding.

---

title: Code Example

Media Queries are sweet:

<pre class="prettyprint" data-lang="css">
@media screen and (max-width: 640px) {
  #sidebar { display: none; }
}
</pre>

---

title: Once more, with JavaScript

<pre class="prettyprint" data-lang="javascript">
function isSmall() {
  return window.matchMedia("(min-device-width: ???)").matches;
}

function hasTouch() {
  return Modernizr.touch;
}

function detectFormFactor() {
  var device = DESKTOP;
  if (hasTouch()) {
    device = isSmall() ? PHONE : TABLET;
  }
  return device;
}
</pre>

---

title: Centered content
content_class: flexbox vcenter

This content should be centered!
