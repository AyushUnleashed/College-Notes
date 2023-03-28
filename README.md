# College-Notes

Technologies for Web Applications: HTML and DHTML
HTML stands for HyperText Markup Language. It is the standard language for creating web pages and web applications. HTML describes the structure and content of a web page using tags and attributes. HTML tags are keywords enclosed in angle brackets (< and >) that define how the content should be displayed by the browser. HTML attributes are additional information that modify the behavior or appearance of a tag.
For example, the following HTML code creates a simple web page with a title and a paragraph:
<!DOCTYPE html>
<html>
<head>
  <title>My First Web Page</title>
</head>
<body>
  <h1>Hello World!</h1>
  <p>This is a paragraph.</p>
</body>
</html>

DHTML stands for Dynamic HTML. It is not a separate language, but a term that refers to the combination of HTML, CSS, JavaScript, and the Document Object Model (DOM) to create dynamic and interactive web pages. DHTML allows web pages to respond to user actions, such as clicking, hovering, scrolling, resizing, etc., without reloading the page.
For example, the following DHTML code creates a web page with a button that changes its color when clicked:
<!DOCTYPE html>
<html>
<head>
  <style>
    #myButton {
      width: 100px;
      height: 50px;
      background-color: green;
      color: white;
      font-size: 20px;
    }
  </style>
  <script>
    function changeColor() {
      var button = document.getElementById("myButton");
      if (button.style.backgroundColor == "green") {
        button.style.backgroundColor = "red";
      } else {
        button.style.backgroundColor = "green";
      }
    }
  </script>
</head>
<body>
  <button id="myButton" onclick="changeColor()">Click Me</button>
</body>
</html>

HTML Basic Concepts
Some of the basic concepts of HTML are:
HTML documents have a hierarchical structure that consists of a root element (<html>), a head element (<head>), and a body element (<body>).
The head element contains metadata about the document, such as the title, character encoding, style sheets, scripts, etc.
The body element contains the visible content of the document, such as headings, paragraphs, images, links, forms, etc.
HTML elements can have child elements (nested inside them) or sibling elements (at the same level as them).
HTML elements can have attributes that provide additional information or modify their behavior or appearance. Attributes are specified as name-value pairs inside the start tag of an element.
HTML elements can be either block-level or inline-level. Block-level elements occupy the entire width of their parent element and start on a new line. Inline-level elements occupy only the space needed by their content and do not start on a new line.
HTML elements can be either empty or non-empty. Empty elements do not have any content or end tag. Non-empty elements have content and an end tag that matches their start tag.







Static and Dynamic HTML
Static HTML refers to web pages that are fixed and do not change in response to user actions or server-side events. Static HTML pages are created once and delivered to the browser as they are. Static HTML pages are easy to create and maintain, but they can be boring and limited in functionality.
Dynamic HTML refers to web pages that are generated or modified on the fly in response to user actions or server-side events. Dynamic HTML pages can use DHTML technologies such as CSS, JavaScript, and DOM to manipulate the content and appearance of the web page without reloading it. Dynamic HTML pages can also use server-side technologies such as PHP, ASP.NET, Ruby on Rails, etc., to generate or fetch data from databases or other sources and insert it into the web page. Dynamic HTML pages are more interactive and engaging, but they can be more complex and difficult to maintain.

Structure of HTML Documents
The structure of an HTML document is defined by its tags and attributes. A typical HTML document has the following structure:
<!DOCTYPE html> <!-- specifies the document type -->
<html lang="en"> <!-- specifies the root element and its language attribute -->
<head> <!-- specifies the head element -->
  <meta charset="UTF-8"> <!-- specifies the character encoding of the document -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- specifies the viewport settings for responsive design -->
  <meta http-equiv="X-UA-Compatible" content="ie=edge"> <!-- specifies the compatibility mode for Internet Explorer -->
  <link rel="stylesheet" href="./styles.css"> <!-- links an external style sheet -->
  <title>Document</title> <!-- specifies the title of the document -->
</head>
<body> <!-- specifies the body element -->
  <!-- here goes the visible content of the document -->
</body>
</html>

HTML Elements
HTML elements are the building blocks of an HTML document. They consist of a start tag, an end tag, and optionally some content and attributes. The start tag and end tag are enclosed in angle brackets (< and >) and have the same name, except that the end tag has a slash (/) before the name. The content is anything that goes between the start tag and end tag. The attributes are name-value pairs that provide additional information or modify the behavior or appearance of an element. The attributes are specified inside the start tag, separated by spaces.
For example, the following HTML code creates a paragraph element with some content and an attribute:
<p class="intro">This is a paragraph.</p>

Some HTML elements are empty, meaning they do not have any content or end tag. They only have a start tag with some attributes. For example, the following HTML code creates an image element with some attributes:
<img src="./logo.png" alt="Logo" width="100" height="50">

Linking in HTML
Linking in HTML is the process of creating hyperlinks that allow users to navigate from one web page or resource to another. Linking in HTML is done using the anchor element (<a>). The anchor element has an attribute called href that specifies the destination of the link. The content of the anchor element is what appears as the clickable text or image on the web page.
For example, the following HTML code creates a link to another web page:
<a href="./about.html">About Us</a>

The following HTML code creates a link to an email address:
<a href="mailto:info@example.com">Contact Us</a>

The following HTML code creates a link to an image:
<a href="./logo.png"><img src="./logo.png" alt="Logo"></a>

Anchor Attributes
Anchor attributes are additional information that modify the behavior or appearance of a link. Some of the common anchor attributes are:
target: specifies where to open the linked document. It can have values such as _blank (opens in a new tab or window), _self (opens in the same tab or window), _parent (opens in the parent frame), _top (opens in the full body of the window), or a name of a frame.
title: specifies extra information about the link. It appears as a tooltip when the user hovers over the link.
download: specifies that the linked resource should be downloaded instead of opened in the browser. It can have an optional value that suggests a filename for the downloaded file.
rel: specifies the relationship between the current document and the linked document. It can have values such as alternate (provides an alternative version of the document), author (provides information about the author of the document), bookmark (provides a permanent URL for the document), help (provides help information for the document), next (indicates that the linked document is the next part of a series), prev (indicates that the linked document is the previous part of a series), etc.
For example, the following HTML code creates a link that opens in a new tab and has a tooltip:
<a href="./about.html" target="_blank" title="Learn more about us">About Us</a>

Image Maps
Image maps are images that have clickable areas that link to different destinations. Image maps are created using two elements: <img> and <map>. The <img> element displays the image and has an attribute called usemap that specifies the name of the map element. The <map> element defines the map and has an attribute called name that matches the usemap value. The <map> element contains one or more <area> elements that define the shape, coordinates, and destination of each clickable area.
For example, the following HTML code creates an image map with three clickable areas:
<img src="./worldmap.png" alt="World Map" usemap="#worldmap">
<map name="worldmap">
  <area shape="rect" coords="0,0,300,200" href="./asia.html" alt="Asia">
  <area shape="circle" coords="400,150,50" href="./africa.html" alt="Africa">
  <area shape="poly" coords="300,200,400,250,500,200" href="./europe.html" alt="Europe">
</map>

Meta Information: Meta information is data that describes other data. It summarizes basic information about a web page, such as its title, description, keywords, author, etc. Meta information is usually expressed in the form of meta tags, which are HTML elements that are placed inside the <head> section of a web page. Meta tags help search engines and browsers to understand and display the web page’s content. For example, this is a meta tag that specifies the character encoding of a web page:
<meta charset="UTF-8">

This is a meta tag that specifies the description of a web page:
<meta name="description" content="This is a web page about meta information.">

This is a meta tag that specifies the keywords of a web page:
<meta name="keywords" content="meta, information, web, technology">

Meta information can also be used for other purposes, such as specifying the viewport size for mobile devices, defining the canonical URL of a web page, or adding social media metadata for sharing123
Image Preliminaries: Image preliminaries are the basic aspects of using images on web pages, such as choosing the right image format, size, quality, and resolution. Image format refers to the way an image is encoded and compressed. Different image formats have different advantages and disadvantages in terms of file size, quality, and compatibility. Some common image formats for web pages are JPEG, PNG, GIF, SVG, and WebP. Image size refers to the dimensions of an image in pixels (width and height). Image quality refers to the level of detail and clarity of an image. Image resolution refers to the number of pixels per inch (PPI) or dots per inch (DPI) of an image. Image preliminaries are important for web pages because they affect the loading speed, appearance, and user experience of the web page. For example, using a large image with high resolution and quality may result in a slow loading time and waste bandwidth. Using a small image with low resolution and quality may result in a blurry and pixelated appearance. Therefore, it is recommended to use an appropriate image format, size, quality, and resolution for each web page according to its purpose and design4
Layouts: Layouts are the ways of arranging and organizing the elements of a web page, such as text, images, links, buttons, etc. Layouts help to create a structure and hierarchy for the web page’s content and improve its readability and usability. Layouts can be created using various techniques and tools in web technology, such as HTML tables, CSS properties (such as display, position, float, flexbox, grid), frameworks (such as Bootstrap), or templates (such as WordPress themes). For example, this is a simple layout using HTML tables:
<table>
  <tr>
    <td colspan="2">Header</td>
  </tr>
  <tr>
    <td>Navigation</td>
    <td>Content</td>
  </tr>
  <tr>
    <td colspan="2">Footer</td>
  </tr>
</table>

This is a simple layout using CSS flexbox:
<style>
  .container {
    display: flex;
    flex-direction: column;
  }

  .header {
    flex: 1;
  }

  .main {
    display: flex;
    flex: 10;
  }

  .nav {
    flex: 1;
  }

  .content {
    flex: 4;
  }

  .footer {
    flex: 1;
  }
</style>

<div class="container">
  <div class="header">Header</div>
  <div class="main">
    <div class="nav">Navigation</div>
    <div class="content">Content</div>
  </div>
  <div class="footer">Footer</div>
</div>

Layouts can also be responsive or adaptive to different screen sizes and devices using media queries or breakpoints4

Colors and Text: Colors and text are the visual aspects of a web page that affect its appearance and readability. Colors and text can be specified using various methods and units in web technology, such as HTML attributes, CSS properties, hexadecimal codes, RGB values, HSL values, color names, etc. For example, this is how to set the color and text of a paragraph using HTML attributes:
<p style="color: blue; font-family: Arial; font-size: 16px; font-weight: bold;">This is a paragraph.</p>

This is how to set the color and text of a paragraph using CSS properties:
p {
  color: #0000FF;
  font-family: Arial;
  font-size: 16px;
  font-weight: bold;
}

Colors and text can also be used to create contrast, harmony, emphasis, or mood for the web page’s content and design. For example, using dark colors on a light background or light colors on a dark background can create contrast and improve readability. Using complementary colors or analogous colors can create harmony and balance. Using different font sizes or styles can create emphasis or hierarchy. Using warm colors or cool colors can create mood or atmosphere.

Fonts: Fonts are the styles of text that are used on a web page. Fonts can affect the appearance and readability of the web page’s content and design. Fonts can be specified using various methods and units in web technology, such as HTML attributes, CSS properties, font names, font families, font stacks, etc. For example, this is how to set the font of a paragraph using HTML attributes:
<p style="font-family: Arial;">This is a paragraph.</p>

This is how to set the font of a paragraph using CSS properties:
p {
  font-family: Arial;
}

Fonts can also be imported from external sources or embedded in the web page using methods such as @font-face rule, Google Fonts API, Font Awesome icons, etc. For example, this is how to import and use a Google Font on a web page:
<head>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lobster">
</head>
<body>
  <p style="font-family: Lobster;">This is a paragraph.</p>
</body>

Fonts can also be adjusted or manipulated using properties such as font-size, font-weight, font-style, text-align, text-transform, text-decoration, etc. For example, this is how to adjust and manipulate the font of a paragraph using CSS properties:
p {
  font-size: 20px;
  font-weight: bold;
  font-style: italic;
  text-align: center;
  text-transform: uppercase;
  text-decoration: underline;
}

Fonts can also be used to create contrast, harmony, emphasis, or mood for the web page’s content and design. For example, using serif fonts or sans-serif fonts can create contrast and improve readability. Using similar fonts or different fonts can create harmony or variety. Using different font sizes or styles can create emphasis or hierarchy. Using decorative fonts or script fonts can create mood or personality.
Backgrounds: Backgrounds are the parts of a web page that are behind the foreground elements, such as text or images. Backgrounds can be used to add color, texture, pattern, image, or gradient to the web page’s design and appearance. Backgrounds can be specified using various methods and units in web technology, such as HTML attributes, CSS properties, hexadecimal codes, RGB values, HSL values, color names, etc. For example, this is how to set the background color of a web page using HTML attributes:
<body style="background-color: yellow;">
  <p>This is a web page with a yellow background.</p>
</body>

This is how to set the background color of a web page using CSS properties:
body {
  background-color: yellow;
}

Backgrounds can also be set to an image or a gradient using the background-image property. For example, this is how to set the background image of a web page using CSS properties:
body {
  background-image: url("background.jpg");
}

This is how to set the background gradient of a web page using CSS properties:
body {
  background-image: linear-gradient(to right, red, orange, yellow, green, blue);
}

Backgrounds can also be adjusted or manipulated using properties such as background-repeat, background-position, background-size, background-attachment, etc. For example, this is how to adjust and manipulate the background image of a web page using CSS properties:
body {
  background-image: url("background.jpg");
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-attachment: fixed;
}

Backgrounds can also be used to create contrast, harmony, emphasis, or mood for the web page’s content and design. For example, using dark colors on a light background or light colors on a dark background can create contrast and improve readability. Using complementary colors or analogous colors can create harmony and balance. Using different textures or patterns can create emphasis or variety. Using images or gradients can create mood or atmosphere123

Tables: Tables are HTML elements that allow web developers to arrange data into rows and columns. Tables consist of table cells inside table rows, which are defined by <td> and </td> tags. Table cells can contain text, images, lists, links, other tables, etc. Table rows start with a <tr> and end with a </tr> tag. Tables can also have table headers, which are defined by <th> and </th> tags. Table headers are usually bold and centered by default. Tables can also have captions, which are defined by <caption> and </caption> tags. Captions are usually displayed above or below the table. Tables can also be styled with CSS to change their appearance and layout1.
Example of a simple HTML table:
<table>
  <caption>A simple HTML table</caption>
  <tr>
    <th>Company</th>
    <th>Contact</th>
    <th>Country</th>
  </tr>
  <tr>
    <td>Alfreds Futterkiste</td>
    <td>Maria Anders</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centro comercial Moctezuma</td>
    <td>Francisco Chang</td>
    <td>Mexico</td>
  </tr>
</table>

Frames: Frames are HTML elements that allow web developers to divide a browser window into multiple sections, each displaying a different web page. Frames are defined by <frame> and </frame> tags inside a <frameset> and </frameset> tag. Frames can have attributes such as src, name, scrolling, noresize, etc. Frames can also be nested inside other framesets to create more complex layouts. Frames can also be targeted by links to change the content of a specific frame.
Example of a simple HTML frameset:
<frameset cols="25%,75%">
  <frame src="menu.html" name="menu">
  <frame src="content.html" name="content">
</frameset>

Layers: Layers are HTML elements that allow web developers to create overlapping sections of content on a web page. Layers are defined by <div> and </div> tags with a style attribute that specifies the position, z-index, top, left, width, and height properties. Layers can be positioned relative to their normal flow position (position: relative), relative to their parent element (position: absolute), or relative to the browser window (position: fixed). Layers can also have different stacking orders based on their z-index values, which determine which layer is on top of which23.
Example of a simple HTML layer:
<div style="position: absolute; z-index: 1; top: 50px; left: 50px; width: 200px; height: 200px; background: red;">
  This is a red layer
</div>

<div style="position: absolute; z-index: 2; top: 100px; left: 100px; width: 200px; height: 200px; background: green;">
  This is a green layer
</div>

<div style="position: absolute; z-index: 3; top: 150px; left: 150px; width: 200px; height: 200px; background: blue;">
  This is a blue layer
</div>

Database integration: Database integration is the process of connecting a web application to a database server, which stores and manages data for the application. Database integration allows web developers to create dynamic web pages that can display, insert, update, delete, and query data from the database. Database integration requires a server-side scripting language (such as PHP, ASP.NET, Python, etc.) and a database management system (such as MySQL, SQL Server, Oracle, etc.). Database integration also requires a connection string that specifies the location, name, username, password, and driver of the database .

CSS: CSS stands for Cascading Style Sheets. CSS is a language that allows web developers to style and format HTML elements. CSS can control the appearance, layout, and behavior of web pages. CSS can be applied to HTML elements using selectors, properties, and values. CSS can also use variables, functions, media queries, animations, transitions, and other features to create dynamic and responsive web pages1.
Example of a simple CSS rule:
/* Select the element with the id of "title" */
#title {
  /* Set its font size to 24 pixels */
  font-size: 24px;
  /* Set its color to blue */
  color: blue;
  /* Set its text alignment to center */
  text-align: center;
}

Positioning with Style sheets: Positioning with style sheets is a technique that allows web developers to change the position and layout of HTML elements using CSS. Positioning with style sheets can override the normal document flow and make elements overlap, float, or stick to a fixed position. Positioning with style sheets requires the use of the position property, which can have values such as static, relative, absolute, fixed, or sticky. Positioning with style sheets also requires the use of the top, bottom, left, and right properties, which specify the offset of the positioned element from its reference point. Positioning with style sheets also depends on the stacking context, which determines the order of overlapping elements based on their z-index values12.
Example of a simple positioning with style sheets:
/* Select the element with the class of "box" */
.box {
  /* Set its width and height to 100 pixels */
  width: 100px;
  height: 100px;
}

/* Select the first box */
.box:nth-of-type(1) {
  /* Set its position to relative */
  position: relative;
  /* Set its background color to red */
  background: red;
}

/* Select the second box */
.box:nth-of-type(2) {
  /* Set its position to absolute */
  position: absolute;
  /* Set its top and left offset to 50 pixels */
  top: 50px;
  left: 50px;
  /* Set its background color to green */
  background: green;
}

/* Select the third box */
.box:nth-of-type(3) {
  /* Set its position to fixed */
  position: fixed;
  /* Set its bottom and right offset to 10 pixels */
  bottom: 10px;
  right: 10px;
  /* Set its background color to blue */
  background: blue;
}

Introduction to JavaScript: JavaScript is a scripting language that allows web developers to add interactivity and functionality to web pages. JavaScript can manipulate HTML elements, access and modify browser data, communicate with servers, create animations, handle user events, and more. JavaScript can be embedded in HTML using <script> and </script> tags or linked from external files using <script src="..."> tags. JavaScript can also use libraries and frameworks such as jQuery, React, Angular, etc. to simplify and enhance web development3.
Example of a simple JavaScript script:
// Get the element with the id of "title"
let title = document.getElementById("title");
// Change its text content to "Hello World"
title.textContent = "Hello World";
// Add a click event listener to it
title.addEventListener("click", function() {
    // Alert a message when it is clicked
    alert("You clicked the title");
});

Cookies: Cookies are small pieces of data that are stored in the browser by web servers. Cookies can store user information such as preferences, settings, login status, etc. Cookies can be created, read, modified, and deleted by JavaScript using the document.cookie property. Cookies have attributes such as name, value, expiry date, path, domain, secure flag, etc. Cookies are sent along with every request to the same domain by the browser1.

Example of creating a cookie using JavaScript:

// This function creates a cookie using the field-name, field-value, and expiry date
function createCookie(fieldname, fieldvalue, expiry) {
  // Create a date object
  var date = new Date();
  // Set the expiry time in milliseconds
  date.setTime(date.getTime() + (expiry * 24 * 60 * 60 * 1000));
  // Convert the date to UTC string
  var expires = "expires=" + date.toUTCString();
  // Write the cookie as a name-value pair with attributes
  document.cookie = fieldname + "=" + fieldvalue + ";" + expires + ";path=/";
}

// Call the function to create a cookie named "username" with a value of "John Doe" that expires in one day
createCookie("username", "John Doe", 1);
Example of reading a cookie using JavaScript:

// This function reads a cookie by its name and returns its value
function readCookie(fieldname) {
  // Get the cookie string
  var cookieString = document.cookie;
  // Split the cookie string by semicolons into an array of name-value pairs
  var cookieArray = cookieString.split(";");
  // Loop through the array
  for (var i = 0; i < cookieArray.length; i++) {
    // Trim any leading or trailing spaces from each pair
    var pair = cookieArray[i].trim();
    // Check if the pair starts with the given field name followed by an equal sign
    if (pair.indexOf(fieldname + "=") == 0) {
      // Return the value part of the pair by slicing it from the equal sign to the end
      return pair.slice(fieldname.length + 1);
    }
  }
  // Return null if no matching pair is found
  return null;
}

// Call the function to read the value of the cookie named "username"
var username = readCookie("username");
// Display the value in an alert box
alert("The value of username cookie is: " + username);

