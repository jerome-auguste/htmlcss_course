# HTML and CSS course to create my first website

Generic website based on [OpenClassrooms course](https://openclassrooms.com/fr/courses/1603881-creez-votre-site-web-avec-html5-et-css3) labs.

## Structure of the course

- [ ] Introduction to HTML
  - [x] My first HTML webpage
  - [x] Text structure
  - [x] Hyperlinks
  - [x] Insert pictures
- [ ] Introduction to CSS
  - [ ] Include CSS in the HTML page
  - [ ] Change text style
  - [ ] Add a background color
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
    <!-- You can make clickable images putting the img tag inside the <a></a> tags>

</body>

</html>
```

## Intruduction to CSS

## Structure your webpage

## Advanced features
