# WCAG Skip Links

**Translated Web Content Accessibility Guidelines (WCAG) conformant, accessible yet invisible skip links.**

---

## Table of contents

<!-- vim-markdown-toc GFM -->

* [About](#about)
* [Usage](#usage)
  * [HTML](#html)
  * [CSS](#css)
  * [Link text](#link-text)
* [Example](#example)
* [Documentation](#documentation)
  * [Introduction to WCAG](#introduction-to-wcag)
  * [Official documentation](#official-documentation)
* [Mirrors](#mirrors)
* [Warranty and Liability](#warranty-and-liability)
* [Licenses](#licenses)
* [Contribute](#contribute)

<!-- vim-markdown-toc -->

---

## About

The [Web Content Accessibility Guidelines (WCAG)]() are part of a series of web accessibility guidelines published by the [Web Accessibility Initiative (WAI)](https://www.w3.org/WAI/) of the [World Wide Web Consortium (W3C)](https://www.w3.org/), the main international standards organization for the Internet. The official recommendation for [WCAG 2.1](https://www.w3.org/TR/WCAG21/) was published in 2018 and was adopted by the [European Union (EU)](https://europa.eu/) as the digital accessibility standard the same year.

Skip links are a mechanism to bypass blocks of content that are repeated on multiple Web pages ([WCAG Success Criterion 2.4.1 Bypass Blocks](https://www.w3.org/WAI/WCAG21/Understanding/bypass-blocks.html)).

Skip links help people, who navigate sequentially through content, to access the primary content of a Web page more directly. Skip links help to skip repeated blocks of content like logos and navigation links.


## Usage

Create Skip links by following the instructions below. 

### HTML

1. Place a HTML skip link on all of your Web pages, ideally before any other content. E.g.:

```html
<body>
  <a href="#main-content" class="visually-hidden focusable skip-link">Skip to main content</a>
  …
```

2. Add `id="main-content"` attribute to an HTML element, that marks the beginning of the main content. E.g.:

```html
…
<main id="main-content">
…
```


### CSS

Add the following to your Cascading Style Sheets (CSS):

```CSS
/* Hide visually but not from screen readers */

.visually-hidden {
  border: 0;
  clip: rect(0 0 0 0);
  height: 1px;
  margin: -1px;
  overflow: hidden;
  padding: 0;
  position: absolute;
  white-space: nowrap;
  width: 1px;
  }

/* Allow the Skip link to be focusable when navigated to via the keyboard */

.visually-hidden.focusable:active,
.visually-hidden.focusable:focus {
  clip: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  position: static;
  white-space: inherit;
  width: auto;
  }

.skip-link.visually-hidden.focusable:focus {
  background: #ffffff;
  color: #000000;
  left: .2em;
  padding: .1em 2em;
  top: 0;
  width: auto;
  z-index: 99999;
  }
```


### Link text 

Set up translations. The translation table, `international-skip-link_link-texts.csv`, uses the **ISO 639-1** and **ISO 639-2/B** language codes to identify ~28 languages. Help with translations is appreciated.


## Example

You can inspect the example implementation by using the `Tab` key to navigate the [rendered version](https://htmlpreview.github.io/?https://github.com/jonasjacek/wcag-skip-links/blob/master/skip-link-example.html) of the example `skip-link-example.html`. 

You can find the file itself on [GitLab](https://gitlab.com/jonasjacek/wcag-skip-links/-/blob/master/skip-link-example.html) and [GitHub](https://github.com/jonasjacek/wcag-skip-links/blob/master/skip-link-example.html).


## Documentation

### Introduction to WCAG

* https://www.w3.org/WAI/standards-guidelines/wcag/
* https://developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG
* https://www.jonas.me/talks/introduction-to-the-web-content-accessibility-guidelines/ (HTML slide show, 6.5 MB)

### Official documentation
* https://www.w3.org/TR/WCAG21/
* https://www.w3.org/TR/UNDERSTANDING-WCAG20/navigation-mechanisms-skip.html
* https://www.w3.org/TR/WCAG20-TECHS/G1


---

## Mirrors

You can find this repository at:
* GitLab  
  [https://gitlab.com/jonasjacek/wcag-skip-links](https://gitlab.com/jonasjacek/wcag-skip-links)
* GitHub  
  [https://github.com/jonasjacek/wcag-skip-links](https://github.com/jonasjacek/wcag-skip-links)


## Warranty and Liability
[Responsive Images](https://gitlab.com/jonasjacek/wcag-skip-links) is a small, private project. The author makes absolutely no claims and representations to warranties regarding the accuracy or completeness of the information provided. However, you can use the information in this repository AT YOUR OWN RISK.


## Licenses

<p xmlns:dct="http://purl.org/dc/terms/"><a rel="license" href="http://creativecommons.org/publicdomain/mark/1.0/"><img src="http://i.creativecommons.org/p/mark/1.0/88x31.png" style="border-style: none;" alt="Public Domain Mark"></a><br>This work (<span property="dct:title">WCAG skip links</span>, by <a href="https://gitlab.com/jonasjacek/wcag-skip-links" rel="dct:creator"><span property="dct:title" title="Jonas Jared Jacek">Jonas Jacek</span></a>), identified by <a href="https://www.jonas.me/" rel="dct:publisher"><span property="dct:title" title="Jonas Jared Jacek">Jonas Jacek</span></a>, is free of known copyright restrictions.</p>

## Contribute

Found a mistake? [Open an issue](https://gitlab.com/jonasjacek/wcag-skip-links/-/issues) or [send a merge request](https://gitlab.com/jonasjacek/wcag-skip-links/-/merge_requests). Want to help in another way? [Contact me](https://www.jonas.me/contact).
