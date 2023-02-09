# HTML and CSS course to create my first website

Generic website based on [OpenClassrooms course](https://openclassrooms.com/fr/courses/1603881-creez-votre-site-web-avec-html5-et-css3) labs.

## Structure of the course

- [x] Introduction to HTML
  - [x] My first HTML webpage
  - [x] Text structure
  - [x] Hyperlinks
  - [x] Insert pictures
- [x] Introduction to CSS
  - [x] Include CSS in the HTML page
  - [x] Change text style
  - [x] Add a background color
  - [x] Add some borders and shadows
  - [x] Use dynamic styles
- [ ] Webpage layouts
  - [x] Structure your webpage
  - [x] Hands on box models
  - [x] Hands on Flexbox
  - [x] CSS Grids
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
  text-shadow: 1px 1px 1px black; /* x-offset y-offset blur-radius color, can be multiple */
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
  border: 1px solid black; /* thickness style color, style can be solid, dashed, dotted, double, none, you can also change proporties of each border using border-top, border-bottom, border-right, border-left keys */
  border-radius: 10px; /* absolute value in px or 0 - 100%, you can also change proporties of each border radius by giving 4 different values, it is possible to create more custom elliptic shapes using complex parameters with "/", you can easilly visualize them using https://9elements.github.io/fancy-border-radius/ */
  box-shadow: 10px 10px 5px rgba(0,0,0,0.75); /* x-offset y-offset blur-radius color, can be multiple visualize shadows at https://shadows.brumm.af/ */
}

/* Dynamic styling with pseudo-classes */
selector:state { /* state can be :hover, :active (on click), :focus (selection using tab for instance), :visited */
  property_1: value_1;
  property_2: value_2;
}

/* Sibling selectors */
selector1 + selector2 { /* Selects the first selector2 that is directly after selector1 */
  property_1: value_1;
  property_2: value_2;
}

* { /* Selects all elements */
  property_1: value_1;
  property_2: value_2;
}

/* Nested selectors */
selector1 selector2 { /* Selects all selector2 that are nested in selector1 */
  property_1: value_1;
  property_2: value_2;
}

/* Attribute selectors */
selector[attribute] { /* Selects all selector that have the attribute */
  property_1: value_1;
  property_2: value_2;
}

selector[attribute="value"] { /* Selects all selector that have the attribute with the value */
  property_1: value_1;
  property_2: value_2;
}

selector[attribute*="value"] { /* Selects all selector that have the attribute with the value in it */
  property_1: value_1;
  property_2: value_2;
}
/* ... Other refined selections are possible, see https://www.w3.org/Style/css3-selectors-updates/WD-css3-selectors-20010126.fr.html#selectors */
```

## Webpage layout

```html
<!DOCTYPE html>
<html lang="fr"> <!-- Webpage language -->

<head>
    <meta charset="utf-8"> <!-- Page encoding -->
    <title>Page title</title> <!-- Shown on your browser tab -->
    <link href="style.css" rel="stylesheet"> <!-- Link to the CSS file -->
</head>

<body>
    <header> <!-- Header of the page, often light and readable with logo, search bar, CTA...  -->
        <nav> <!-- Navigation bar to switch to different sections or pages -->
            <ul>
                <li><a href="link_to_page">Link 1</a></li>
                <li><a href="link_to_page">Link 2</a></li>
                <li><a href="link_to_page">Link 3</a></li>
            </ul>
        </nav>
    </header>
    <main> <!-- Main content of the page -->
      <h1>Page title</h1>
        <section> <!-- Section of the page, structures the main block -->
          <h2>Section title</h2>
          <p>Content of your paragraph</p>
        </section>
        <section>
          <article> <!-- Autonomous part of your page, usually structured so it can be copied to another website -->
            <h2>Article title</h2>
            <p>Content of your paragraph</p>
          </article>
        </section>
    </main>
    <aside> <!-- Separated from the main content, can be put aside from the main content for instance, but it can be put anywhere on the page depending on your needs -->
        <h3>Aside title</h3>
        <p>Content of your paragraph</p>
    </aside>
    
    <footer> <!-- Footer of the page -->
        <p>Contact information, useful informations, legal terms, privacy policy...</p>
    </footer>
</body>
```

```html
<div></div> <!-- block tag -->
<span></span> <!-- inline tag -->
```

```css
block_selector {
  width: 100%; /* absolute value in px or % */
  height: 100%; /* absolute value in px or % */
  margin: 10px; /* external spacing with other blocks, absolute value in px or % or auto for horizontal centering, you can also change proporties of each margin by giving 4 different values (top right bottom left) */
  padding: 10px; /* internal spacing with nested content, absolute value in px or %, you can also change proporties of each padding by giving 4 different values */
}

container_selector {
  display: flex; /* block, inline, inline-block, flex, grid, none */
  flex-direction: row; /* row, row-reverse, column, column-reverse, direction of the flexbox */
  flex-wrap: wrap; /* nowrap, wrap, wrap-reverse, depending on the screen size, some elements might go to a new line or reverse when a new line is created */
  justify-content: center; /* flex-start, flex-end, center, space-between, space-around, space-evenly, aligns the elements in the flexbox on the principal direction (defined in the flex-direction property) */
  align-items: center; /* flex-start, flex-end, center, baseline, stretch, aligns the elements in the flexbox on the secondary direction (defined in the flex-direction property) */
  align-content: center; /* flex-start, flex-end, center, space-between, space-around, stretch, aligns the lines of the flexbox on the secondary direction (defined in the flex-direction property) when flex-warp is enabled (no effect with only 1 line) */

  /* To center a flexbox, you can use the following properties */
  display: flex;
  margin: auto;
}

container_selector {
  display: grid;
  grid-template-columns: 200px 200px 200px; /* Absolute value in px, em, rem and fr (fraction unit) give the number of columns by giving the width of each column, ensure that each grid cell width is not set otherwise you would have an unexpected result */
  grid-template-rows: 200px 200px 200px; /* Absolute value in px, give the number of rows by giving the height of each row, ensure that each grid cell height is not set otherwise you would have an unexpected result */
  gap: 10px; /* Absolute value in px, defines the spacing between the grid cells */
}

grid_cell_selector {
  grid-column: 1 / 3; /* Defines the column of the grid cell, equivalent to grid-column-start: 1; grid-column-end: 3; */
  grid-row: 1 / 3; /* Defines the row of the grid cell, equivalent to grid-row-start: 1; grid-row-end: 3; */
}
```

## Advanced features
