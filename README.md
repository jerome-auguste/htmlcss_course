# HTML and CSS course to create my first website

Generic website based on [OpenClassrooms course](https://openclassrooms.com/fr/courses/1603881-creez-votre-site-web-avec-html5-et-css3) labs.

## Structure of the course

- [x] Introduction to HTML
  - [x] My first HTML webpage
  - [x] Text structure
  - [x] Hyperlinks
  - [x] Insert pictures
- [ ] Introduction to CSS
  - [x] Include CSS in the HTML page
  - [x] Change text style
  - [x] Add a background color
  - [ ] Add some borders and shadows
  - [ ] Use dynamic styles
- [ ] Structure your webpage
  - [ ] Webpage strucure
  - [ ] Discover boxes
  - [ ] Page layout with Flexbox
  - [ ] Discover CSS Grids
  - [ ] Other page layout methods
- [ ] Advanced features
  - [ ] Add tables
  - [ ] Add forms
  - [ ] Finalize forms and add a submit button
  - [ ] Use responsive design with Media Queries
  - [ ] Go further

## Introduction to HTML

```html
<!DOCTYPE html>
<html lang="fr"> <!-- Webpage language -->

<head>
    <meta charset="utf-8"> <!-- Page encoding -->
    <title>Page title</title> <!-- Shown on your browser tab -->
</head>

<body>
    <!-- Insert the content here  -->
    <h1>Level 1 Header</h1>
    <h2>Level 2 Header</h2>
    <h3 id="my_anchor">Level 3 Header</h3> <!-- Good practice: no space or special characters in the anchor id, used in href and CSS styling -->
    <!-- Until <h6> -->
    <!-- Good practice: never skip a level h1 -> h2 -> h3...-->
    <p>Paragraph content, <br>with mutliple lines</p> <!-- Good practice: only one <br> and choose the size of the line break in CSS -->
    <ul> <!-- Unordered list -->
      <li>1st list item</li>
      <li>2nd list item</li>
    </ul>
    <ol> <!-- Ordered list -->
      <li>1st list item</li>
      <li>2nd list item</li>
    </ol>
    <mark>Highlighted text</mark> <!-- Good practice: use CSS for custom mark behaviour -->
    <em>Italic text</em> <!-- Good practice: use CSS for custom em behaviour -->
    <strong>Bold text</strong> <!-- Good practice: use CSS for custom strong behaviour -->
    <a href="link_to_content">Displayed text to click on</a> <!-- Link can be URL, relative path to other file (HTML file will be displayed, other file extensions will be downloaded), anchor using "#my_anchor" which you can combine with a link to another HTML file "relative/path/to/page.html#anchor_id, <target="_blank"> opens a new tab, "mailto:em@iladdress.com" opens e-mail app -->
    <img src="link_to_picture" alt="Alternative text for accessibility and references" title="Text to display on hover"> <!-- src has the same behaviour as href -->
    <!-- Good practice: use snake case for picture and folder names -->
    <!-- You can make clickable images putting the img tag inside the <a></a> tags -->

</body>

</html>
```

## Intruduction to CSS

```html
<!DOCTYPE html>
<html lang="fr"> <!-- Webpage language -->

<head>
    <meta charset="utf-8"> <!-- Page encoding -->
    <title>Page title</title> <!-- Shown on your browser tab -->
    <link href="style.css" rel="stylesheet"> <!-- Link to the CSS file -->
</head>

<body>
  <!-- Content of your page -->
  <p class="my_class_1 my_class_2">
    Content of your paragraph
  </p>
  <p class="my_class_1">
    Content of your paragraph
  </p>
  <div> <!-- Div is a generic container to structure the webpage construction, can be used to group elements -->
    <p id="my_id">
      Content of your <span class="special_word">paragraph</span> <!-- Span is a generic inline container, to reach a single element in a list of them (a word in a paragraph for example) -->
    </p>
  </div>
  
</body>
</html>
```

```css
selector1, selector2 {
  color: red; /* Color can be in hexa, rgb or rgba, rgba is rgb with alpha channel for transparency, set of color examples at https://coolors.co/ */
  property_1: value_1;
  property_2: value_2;
}

.class { /* Class referenced in HTML code (<p class="my_class">), class has a thiner description of elements and can be applied to multiple elements */
  property_1: value_1;
  property_2: value_2;
}

#id { /* Id referenced in HTML code (<p id="my_id">), id is unique and can only be applied to one element */
  property_1: value_1;
  property_2: value_2;
}

text_or_block_selector {
  font-size: 1em; /* Either in px or em, em is relative size to the parent element and is prefered for responsiveness */
  font-family: "Arial Black", sans-serif; /* Standard font family (supported by all browsers): Arial Black, Futura, Helvetica, Impact, Trebuchet MS, Verdana. You can import your own font family using Google Fonts (https://fonts.google.com/) or by using local custom fonts */
  font-style: italic; /* italic or oblique, normal */
  font-weight: bold; /* bold, normal, thin, 100 - 900, ensure to import all weights and styles of the custom font you are using */
  text-decoration: underline; /* underline, line-through, overline, none */
  text-align: center; /* left, right, center, justify, only on block tags <p>, <div>, <h1>... */
}

block_selector {
  background-color: black; /* Color can be in hexa, rgb or rgba, rgba is rgb with alpha channel for transparency */
  background-image: url("link_to_picture"); /* url can be a relative path to a picture or a http(s) link to a picture */
  /* Background image properties */
  background-repeat: no-repeat; /* repeat, repeat-x, repeat-y, no-repeat */
  background-position: center; /* left, right, center, top, bottom, top left, top right, bottom left, bottom right, x% y% */
  background-size: cover; /* cover, contain, x% y%, x px y px */
  background-attachment: fixed; /* fixed, scroll */
  /* Combine background properties */
  background: url("link_to_picture") no-repeat center center/cover fixed;
  /* Linear gradient */
  background: linear-gradient(to right, red, blue); /* to top, to bottom, to left, to right, to top left, to top right, to bottom left, to bottom right, angle, x% y%, color1, color2, gradient examples at https://uigradients.com/, build your own gradients at https://cssgradient.io/ */
  opacity: 0.5; /* 0 - 1 */
}
```

## Structure your webpage

## Advanced features
