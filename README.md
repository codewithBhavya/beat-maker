# Beat Maker

This is a simple web application called "Beat Maker" that allows you to create music by tapping on different pads. It is built using HTML, CSS, and JavaScript.

## HTML

The HTML code defines the structure and content of the web page. Here's a breakdown of the elements used:

- `<!DOCTYPE html>`: Specifies the document type and version.
- `<html>`: The root element of the HTML page.
- `<head>`: Contains metadata and external resources used by the page.
  - `<meta>`: Meta tags that provide information about the page.
  - `<link>`: Links to external resources such as stylesheets and fonts.
  - `<script>`: Links to the JavaScript code file.
  - `<title>`: Sets the title of the page displayed in the browser tab.
- `<body>`: Represents the content of the web page.
  - `<div class="app">`: The main container for the application.
    - `<header>`: Contains the title and description of the app.
    - `<div class="visual">`: Container for visual effects.
    - `<div class="pads">`: Container for the sound pads.
      - `<div class="pad1">` to `<div class="pad6">`: Individual sound pads with associated audio files.

## CSS

The CSS code provides the styling and layout for the HTML elements. Here's an overview of the CSS styles applied:

- `*`: Applies the specified styles to all elements.
- `body`: Sets the font family for the entire page.
- `.app`: Styles the main container with a fixed height and vertical flex layout.
- `header h1`: Styles the heading element within the header.
- `header p`: Styles the paragraph element within the header.
- `.pads`: Styles the container for the sound pads with a background color.
- `.pads > div`: Styles each pad within the pads container with equal width and height.
- `.pad1` to `.pad6`: Styles each pad with a specific background color.
- `.visual > div`: Styles the visual effect elements with absolute positioning and animation properties.
- `@keyframes jump`: Defines the animation keyframes for the visual effect.

## JavaScript

The JavaScript code adds interactivity and functionality to the web application. Here's a summary of what it does:

- The `window` event listener waits for the page to load before executing the code.
- The `sounds` variable stores references to all audio elements with the class "sound".
- The `pads` variable stores references to all div elements within the "pads" container.
- The `visual` variable stores a reference to the div element with the class "visual".
- The `colors` array contains different colors used for the visual effect.
- A click event listener is added to each pad element. When clicked:
  - The corresponding sound is played from the beginning.
  - The `createBubbles` function is called with the index of the clicked pad.
- The `createBubbles` function dynamically creates a new div element as a visual effect.
  - The new div is appended to the "visual" container.
  - The background color is set based on the index passed.
  - An animation is applied to the new div using the "jump" keyframes.
  - An animationend event listener is added to remove the div from the DOM when the animation ends.

This README provides an overview of the HTML structure, CSS styles, and JavaScript functionality of the Beat Maker web application.