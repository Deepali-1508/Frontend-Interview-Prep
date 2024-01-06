# Frequently Asked HTML Questions 

## 1. What is HTML?

HTML, or HyperText Markup Language, is the standard markup language for creating web pages. It provides a structure for content on the web, using a system of tags to define different elements such as headings, paragraphs, links, and images.

## 2. What are Tags, Elements, and Attributes?

In HTML, the terms "tags," "elements," and "attributes" are fundamental concepts:

- **Tags:** Tags are the building blocks of HTML. They define the structure and hierarchy of content on a web page. Tags are represented by opening (`<tag>`) and closing (`</tag>`) elements, surrounding the content they affect.

- **Elements:** An element is a complete set of tags, along with the content they enclose. It consists of the opening tag, the content, and the closing tag. For example, in `<p>This is a paragraph.</p>`, `<p>` is the opening tag, `This is a paragraph.` is the content, and `</p>` is the closing tag.

- **Attributes:** Attributes are used along with the HTML tags to define the characteristics of the element. Attributes provide additional information about HTML elements. They are always included in the opening tag and are used to modify the behavior or appearance of the element. Attributes consist of a name and a value, separated by an equal sign. For example, in `<a href="https://example.com">Visit Example</a>`, `href` is the attribute name, and `https://example.com` is the attribute value.

- **Void Elements:** HTML elements which do not have closing tags or do not need to be closed are Void elements. For Example `<br />, <img />, <hr />,` etc.
Understanding these concepts is crucial for creating well-structured and semantically meaningful HTML documents.

## 3. What are HTML entities?

# HTML Entities

HTML entities are special codes used to represent reserved characters, as well as characters that might not easily be typed or displayed using the standard keyboard. These entities are particularly useful in HTML documents where certain characters have special meanings, such as `<` and `>` in tags or characters with reserved meanings like `&`.

HTML entities are written as a combination of the `&` (ampersand) symbol, followed by a specific code, and ending with a semicolon (`;`). Here are some common HTML entities:

**Character Entity References:**

- `&lt;`: Represents the less-than symbol `<`.
- `&gt;`: Represents the greater-than symbol `>`.
- `&amp;`: Represents the ampersand symbol `&`.
- `&quot;`: Represents the double quotation mark `"`.

For apostrophe or single quotation mark, you can use either `&apos;` or the actual character `'`.

## 4. What is Class and ID in HTML, and What's the Difference?

In HTML, both class and ID are attributes used to apply styles or scripts to specific elements.

- **class:**
  - A class is a way to apply a style or script to multiple elements on a page.
  - Multiple elements can share the same class.
  - Defined using the class attribute: `<div class="example">`.
  - Styled in CSS with a period: .example { /* styles */ }.

- **id:**
  - An ID is used to uniquely identify a single element on a page.
  - Each ID must be unique within a page.
  - Defined using the id attribute: `<div id="uniqueElement">`.
  - Styled in CSS with a hash: #uniqueElement { /* styles */ }.
  
 
- **Difference:** 

  Classes are for multiple elements; IDs are for a single, unique element.
  Multiple elements can share the same class, but each ID must be unique.
  CSS rules for classes start with a period (.), and for IDs, they start with a hash (#).

## 5. What are List in HTML and Types of List?

In HTML, a list is a way to organize and structure content. There are three main types of lists: ordered lists, unordered lists, and description lists.
### Types of List:

1. **Ordered Lists (<ol>):** An ordered list is used to represent a list of items in a specific sequence or order. Each item in the list is marked with a number or another ordered marker. In HTML, you create an ordered list using the <ol> element and list items with the <li> element.
 ```html
<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ol>
```

2. **Unordered Lists (<ul>):** An unordered list is used to represent a list of items without a specific order or sequence. Each item in the list is typically marked with a bullet point or another unordered marker. In HTML, you create an unordered list using the <ul> element and list items with the <li> element.
  ```html
 <ul>
  <li>Apple</li>
  <li>Banana</li>
  <li>Orange</li>
</ul>
```

 3. **Description Lists (<dl>):** A description list is used to represent a list of terms and their corresponding descriptions. Each term is defined using the <dt> (definition term) element, and its description is provided using the <dd> (definition description) element.
  ```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>

  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>

  <dt>JavaScript</dt>
  <dd>A programming language for the web</dd>
</dl>
```  

## 6. What are Tables in HTML and Types of Tables?

In HTML, tables are used to organize and display data in a structured format. A table is created using the `<table>` element, and it consists of rows and columns. The basic structure includes `<tr>` for table rows, `<th>` for table headers, and `<td>` for table data.

## 7. What are Multipart form Data?

Multipart form data is a format used to encode and transmit binary data as part of an HTTP request. It is commonly used when submitting forms that include file uploads or other binary data. Unlike the traditional URL-encoded form data, which is suitable for simple text-based key-value pairs, multipart form data allows for the transmission of binary files, such as images, videos, or documents.

In a multipart form data request, the data is divided into multiple parts, each part represented by a separate section within the request body. Each section has its own set of headers, including a content-type header that specifies the type of data being transmitted (e.g., text, image, etc.). The sections are typically separated by a boundary string.

```POST /submit-form HTTP/1.1
Host: example.com
Content-Type: multipart/form-data; boundary=---------------------------1234567890

-----------------------------1234567890
Content-Disposition: form-data; name="text_field"

Some text data
-----------------------------1234567890
Content-Disposition: form-data; name="file_field"; filename="example.jpg"
Content-Type: image/jpeg

(Binary data for the image file)
-----------------------------1234567890--
```

In this example:

Content-Type: multipart/form-data; boundary=---------------------------1234567890 specifies the use of multipart form data with the specified boundary.
Each part begins with -----------------------------1234567890.
The first part includes a text field with the name "text_field" and some text data.
The second part includes a file field with the name "file_field," a filename "example.jpg," and the binary data of an image file with the content type "image/jpeg."
The boundary string is crucial for distinguishing between different parts within the request body. It must be unique and not appear in the data itself. The server uses the boundary to parse and extract each part of the multipart form data.

## 8. What is the purpose of the <!DOCTYPE html> declaration?
It defines the document type and version of HTML being used. It helps browsers to render the web page correctly.

## 9.What is the difference between <div> and <span>?
- **<div> (Division Element):** The <div> element is a block-level container used to group and structure content.
It is typically used to create sections or divisions in a webpage, allowing you to apply styles or manipulate the content as a whole.
<div> elements automatically start on a new line and take up the full width of their container by default.

- **<span> (Inline Element):**
The <span> element is an inline container used to apply styles or manipulate specific portions of text within a larger block of content.
It is often used when you want to style a specific part of text, apply scripting, or apply CSS styles without affecting the entire block.
<span> elements do not start on a new line and only take up as much width as necessary.

## 10.What is the purpose of the <meta> tag?
The <meta> tag is used to provide metadata about the HTML document, such as character set, viewport settings, and description.

## 11.What is the purpose of the alt attribute in the <img> tag?
 The alt attribute provides alternative text for an image, which is displayed if the image cannot be loaded. It is also important for accessibility.

## 12. What is the purpose of the `<DOCTYPE>` declaration, and how does it differ from the `<meta>` tag?
   - The `<DOCTYPE>` declaration defines the document type and version of HTML, aiding in proper rendering. It is not an HTML tag but an instruction to the browser. `<meta>` tags, on the other hand, provide metadata within the HTML document.

## 13. Explain the concept of HTML semantics.
   - HTML semantics involves using tags to convey the meaning of the content rather than just its presentation. Semantically correct HTML helps search engines and assistive technologies better understand the structure and context of the content.

## 14. What are some new semantic elements introduced in HTML5?
   - HTML5 introduced semantic elements like `<article>`, `<section>`, `<nav>`, `<header>`, `<footer>`, `<aside>`, `<figure>`, and `<figcaption>`. These elements provide more meaningful structure to web documents.

## 15. How does the `<canvas>` element work in HTML5?
   - The `<canvas>` element provides a drawing space for graphics using JavaScript. Developers can draw shapes, images, and other graphical elements on the canvas dynamically.

## 16. Explain the purpose of the `data-*` attributes in HTML.
   - `data-*` attributes are custom attributes that allow developers to store extra information in HTML elements. They are often used for scripting or styling purposes and don't affect the rendering or default behavior of the elements.

## 17. What is the importance of the `role` attribute in HTML, especially in terms of accessibility?
   - The `role` attribute is used to define the purpose or role of an element, particularly in the context of accessibility. It helps assistive technologies understand the intended function of an element on the page.

## 18. How can you embed audio and video in HTML5?
   - You can use the `<audio>` and `<video>` elements to embed audio and video, respectively. Example:
     ```html
     <audio controls>
       <source src="audio.mp3" type="audio/mp3">
       Your browser does not support the audio element.
     </audio>

     <video width="320" height="240" controls>
       <source src="movie.mp4" type="video/mp4">
       Your browser does not support the video tag.
     </video>
     ```

## 19. Explain the difference between the `<script>`, `<script async>`, and `<script defer>` elements.
   - The `<script>` element is used to embed or reference JavaScript. Adding `async` makes the script execute asynchronously, while `defer` delays script execution until the HTML parsing is complete.

## 20. How does the HTML5 geolocation API work?
   - The Geolocation API allows obtaining the user's geographical location. It can be accessed using JavaScript through the `navigator.geolocation` object.

## 21. What is the purpose of the `<details>` and `<summary>` elements in HTML5?
    - The `<details>` element represents a disclosure widget from which the user can obtain additional information. The `<summary>` element provides a summary or label for the content within the `<details>` element.

## 21. Explain the purpose of the `<iframe>` element.
   - The `<iframe>` (Inline Frame) element is used to embed another HTML document within the current document. It is often used to display content from external sources like maps or videos.

## 22. What is the difference between `<span>` and `<div>`? When would you use one over the other?
   - Both `<span>` and `<div>` are container elements, but `<span>` is an inline element, and `<div>` is a block-level element. Use `<span>` when you want to apply styles or scripting to a specific piece of inline content, and `<div>` when you want to group and style block-level content.

## 23. How does the `lang` attribute contribute to web accessibility?
   - The `lang` attribute is used to declare the language of the content. It aids accessibility by informing screen readers and other assistive technologies about the language used, ensuring proper pronunciation and comprehension.

## 24. Explain the concept of responsive web design and how it can be achieved using HTML and CSS.
   - Responsive web design aims to make web pages render well on various devices and window sizes. It is achieved by using flexible grid layouts, media queries, and fluid images. Media queries in CSS allow styles to be applied based on device characteristics like screen width and height.

## 25. What is the HTML `<template>` element used for?
   - The `<template>` element is used to hold client-side content that you don't want to be rendered when the page loads. It can be cloned and used dynamically with JavaScript.

## 26. Explain the purpose of the `<figcaption>` element when used with `<figure>`.
   - The `<figcaption>` element is used to provide a caption or description for the content within the `<figure>` element. This is commonly used with images or multimedia content.

## 27. How can you create a hyperlink that opens an email client with a pre-filled subject and body?
   - Use the `mailto:` scheme in the `href` attribute of an `<a>` tag. Example:
     ```html
     <a href="mailto:example@email.com?subject=Subject%20Text&body=Body%20Text">Send Email</a>
     ```

## 28. What is the purpose of the `<ruby>` and `<rt>` elements in HTML?
   - The `<ruby>` element is used to define annotations for characters, typically used in East Asian typography. The `<rt>` element provides the pronunciation of characters within the `<ruby>` element.

## 29. Explain the concept of HTML microdata and its use.
   - HTML microdata is used to embed machine-readable data within HTML documents. It is often used for providing additional information about the content, such as defining product details, person information, or event details.

## 30. How can you embed custom fonts in a web page using HTML and CSS?
   - Use the `@font-face` rule in CSS to embed custom fonts. Example:
     ```css
     @font-face {
       font-family: 'CustomFont';
       src: url('custom-font.woff2') format('woff2');
     }

     body {
       font-family: 'CustomFont', sans-serif;
     }
     ```

### 31. How to handle events in HTML?

- HTML handles events using attributes like `onclick`, `onchange`, etc. For example:
  ```html
  <button onclick="myFunction()">Click me</button>
  ```

### 32. Explain the difference between padding and margin in CSS.

- **Padding:**
  - Space between the content and the inner border of an element.
  - Set using `padding` property.
  - Example: `padding: 10px;`

- **Margin:**
  - Space outside the outer border of an element.
  - Set using `margin` property.
  - Example: `margin: 10px;`

### 33. What is the box model in CSS, and how does it work?

- **Box Model:**
  - Describes the layout of elements in HTML.
  - Consists of content, padding, border, and margin.

- **Components:**
  - **Content:** Actual content of the box.
  - **Padding:** Space between content and border.
  - **Border:** Surrounds the padding.
  - **Margin:** Space outside the border.

### 34. How can you make a hyperlink open in a new tab or window?

- Use the `target` attribute with the value `_blank`.
  ```html
  <a href="https://www.example.com" target="_blank">Visit Example.com</a>
  ```

### 35. Explain the concept of responsive web design and how media queries are used.

- **Responsive Web Design:**
  - Design approach to make web pages render well on various devices and window sizes.
  - Achieved using fluid grids, flexible images, and media queries.

- **Media Queries:**
  - Used to apply styles based on device characteristics.
  - Example:
    ```css
    @media screen and (max-width: 600px) {
      /* Styles for screens up to 600px width */
    }
    ```

### 36. What is the purpose of the HTML `<meta>` tag?

- `<meta>` tag is used to provide metadata about the HTML document.
- Common uses include setting the character set, viewport settings, and specifying keywords for search engines.
  ```html
  <meta charset="UTF-8">
  ```

### 37. How to create an ordered list (`<ol>`) and an unordered list (`<ul>`) in HTML?

- **Ordered List:**
  ```html
  <ol>
    <li>Item 1</li>
    <li>Item 2</li>
  </ol>
  ```

- **Unordered List:**
  ```html
  <ul>
    <li>Item A</li>
    <li>Item B</li>
  </ul>
  ```

### 38. Explain the role of the `<head>` section in an HTML document.

- `<head>` section contains metadata and links to external resources.
- Includes elements like `<title>`, `<meta>`, `<link>`, and `<style>`.

### 39. What is the purpose of the HTML `<nav>` element?

- `<nav>` is used to define a set of navigation links.
- Typically includes menus, lists of links, or other navigation elements.

### 40. How to create a dropdown list (`<select>`) in HTML?

- Use the `<select>` element to create a dropdown list.
- Inside, use `<option>` elements for each item in the list.
  ```html
  <select>
    <option value="option1">Option 1</option>
    <option value="option2">Option 2</option>
  </select>
  ```

## 41. Describe HTML layout structure.
Every web page has different components to display the intended content and a specific UI. But still, there are few things which are templated and are globally accepted way to structure the web page, such as:

<header>: Stores the starting information about the web page.
<footer>: Represents the last section of the page.
<nav>: The navigation menu of the HTML page.
<article>: It is a set of information.
<section>: It is used inside the article block to define the basic structure of a page.
<aside>: Sidebar content of the page

## 42. How is Cell Padding different from Cell Spacing?
Cell Padding:

cellpadding is an attribute used in HTML tables to define the space between the content of a cell and its border.
Applied to individual <td> or <th> elements within a table.
Example: <td cellpadding="5">
Cell Spacing:

cellspacing is an attribute used in HTML tables to define the space between cells within the table.
Applies to the entire table, affecting the spacing between all cells.
Example: <table cellspacing="10">

## 43. How can we club two or more rows or columns into a single row or column in an HTML table?
To span multiple rows: Use the rowspan attribute in a `<td> or <th>` element.

```
<td rowspan="2">Spanning Two Rows</td>
To span multiple columns: Use the colspan attribute in a <td> or <th> element.
<td colspan="3">Spanning Three Columns</td>
```

## 44. Is it possible to change an inline element into a block-level element?
Yes, you can change an inline element into a block-level element using the CSS display property.
css

```
inline-element {
  display: block;
}
```

## 45. In how many ways can we position an HTML element? Or what are the permissible values of the position attribute?
Permissible values of the position attribute are:
-static: Default positioning.
-relative: Relative to its normal position.
-absolute: Relative to its nearest positioned ancestor.
-fixed: Relative to the browser window.
-sticky: Based on user's scroll position.


## 46. In how many ways can we display HTML elements?
Permissible values of the display property include:
-block: Displays an element as a block-level element.
-inline: Displays an element as an inline element.
-inline-block: Displays an element as an inline-level block container.
-flex: Displays an element as a block-level flex container.
-grid: Displays an element as a block-level grid container and more.

## 47. What is the difference between “display: none” and “visibility: hidden”, when used as attributes to the HTML element.
display: none: Completely removes the element from the document flow, and it won't take up space.
visibility: hidden: Hides the element, but it still occupies space in the document flow.

## 48. How to specify the link in HTML and explain the target attribute?
To specify a link, use the <a> (anchor) tag.

```
<a href="https://www.example.com" target="_blank">Visit Example.com</a>
```
target attribute:

_blank: Opens the link in a new tab or window.
_self: Opens the link in the same frame or tab.


## 49. In how many ways can we specify the CSS styles for the HTML element?
Styles can be specified in multiple ways:
Inline styles within the HTML element.
Internal styles using the <style> tag within the <head> section.
External styles using an external CSS file linked with the <link> tag.

## 50. Difference between link tag <link> and anchor tag <a>?
<link>: Used in the <head> to link external resources, such as stylesheets.

```
<link rel="stylesheet" type="text/css" href="styles.css">
```
<a>: Used to create hyperlinks.
```
<a href="https://www.example.com">Visit Example.com</a>
```

## 51. How to include JavaScript code in HTML?
Use the <script> tag to include JavaScript code.

<script>
  // JavaScript code goes here
</script>

## 51. When to use scripts in the head and when to use scripts in the body?
Scripts in the <head>: Use for scripts that need to run before the content is displayed, like loading external resources.
Scripts in the <body>: Use for scripts that manipulate or interact with the document content.


## 52. What are forms and how to create forms in HTML?
Forms are used to collect user input. Create forms using the <form> tag and include various form elements like ` <input>, <select>, <textarea>`.
```
<form action="/submit" method="post">
  <!-- Form elements go here -->
</form>
```

## 53.What are formatting tags in HTML?
Various Formatting Tags in HTML:
HTML provides several formatting tags to structure and style content. Here are some common formatting tags:

- **`<strong>`**: Represents strong importance or emphasis. It typically renders as bold text.

- **`<b>`**: Represents bold text. It doesn't imply strong importance and is often used for presentational purposes.

- **`<em>`**: Represents emphasized text. It typically renders as italicized text.

- **`<i>`**: Represents italicized text. Like <b>, it is often used for presentational purposes.

## 54.What is the difference between `<strong>`,` <b>`,` <em>`,` <i>` tags?

- **`<strong>`** is a semantic tag indicating strong importance, affecting both style and structure.
- **`<b>`** is a presentational tag, used for bold formatting without indicating strong importance.
- **`<em>` vs. `<i>`:**

`<em>` is a semantic tag indicating emphasis, affecting both style and structure.

`<i>` is a presentational tag, used for italic formatting without indicating emphasis.

## 55.Web Page Inside a Web Page (Nesting of Web Pages)?
Web pages are typically structured using HTML, and it's common to nest elements within each other to create a hierarchy.
However, a web page inside a web page in the sense of one HTML document fully encapsulated within another is not a standard practice.
Each HTML document is expected to have a single root element (e.g., `<html>`), and embedding a full HTML document within another breaks the structure and is not a valid HTML construct.

## 56.What are some ways to optimize asset loading in web page?
Optimizing asset loading is crucial for improving website performance. Here are some strategies to optimize the loading of assets such as images, stylesheets, and scripts:

1. **Minify and Compress Assets:**
   - Minify CSS, JavaScript, and HTML files to remove unnecessary characters, whitespace, and comments.
   - Use tools like UglifyJS for JavaScript and CSSNano for CSS.
   - Enable server-side compression (gzip or Brotli) to reduce the size of assets during transmission.

2. **Optimize Images:**
   - Use image optimization tools to compress images without compromising quality, such as ImageOptim, TinyPNG, or Squoosh.
   - Consider using responsive images with the `<picture>` element or the `srcset` attribute to deliver different image sizes based on the user's device.

3. **Leverage Browser Caching:**
   - Set appropriate caching headers to instruct browsers to cache assets locally.
   - Use a unique filename or versioning (e.g., appending a hash) for updated assets to ensure that changes are recognized by the browser.

4. **Combine and Minify CSS and JavaScript:**
   - Reduce the number of HTTP requests by combining multiple CSS or JavaScript files into one.
   - Minify the combined file to reduce its size.
   - Consider using tools like Webpack or Gulp to automate this process.

5. **Asynchronous and Deferred Loading:**
   - Use the `async` or `defer` attributes for script tags to control when scripts are executed.
     - `async`: Downloads the script asynchronously and executes it as soon as it's available.
     - `defer`: Downloads the script asynchronously and executes it after the HTML document is fully parsed.
   - Be cautious with third-party scripts, as they may not support these attributes.

6. **Lazy Loading:**
   - Implement lazy loading for images, especially those below the fold.
   - Use the `loading="lazy"` attribute on `<img>` tags to defer the loading of images until they are near the user's viewport.

7. **Critical CSS:**
   - Identify and inline critical CSS to render above-the-fold content quickly.
   - Load non-critical CSS asynchronously or defer its loading to enhance page load speed.

8. **CDN (Content Delivery Network):**
   - Use a CDN to distribute static assets across multiple servers geographically closer to the user, reducing latency.
   - Utilize a reliable CDN service to cache and serve assets efficiently.

9. **Preconnect and Prefetch:**
   - Use `<link rel="preconnect">` to establish early connections to domains hosting third-party assets or resources.
   - Use `<link rel="prefetch">` to download and cache assets that will be needed in the future, reducing load times for subsequent requests.

10. **Reduce HTTP Requests:**
    - Combine small images into sprites to reduce the number of image requests.
    - Minimize the use of external scripts and stylesheets.

11. **Critical Path Rendering:**
    - Prioritize loading critical resources required for rendering above-the-fold content.
    - Use tools like Google PageSpeed Insights or Lighthouse to identify critical rendering path issues.

## 57.Difference between HTML and HTML5 ?
# HTML

HTML (Hypertext Markup Language) is the standard markup language for creating web pages and web applications. It was initially introduced in 1991 and has undergone various versions and updates. The latest version of HTML before HTML5 was HTML 4.01, which was released in 1999.

## Key Features of HTML:

- Limited support for multimedia elements.
- Reliance on plugins like Flash for rich media content.
- Lack of native support for audio and video.
- Absence of semantic tags for structuring content.
- Limited form types and attributes.

# HTML5

HTML5 is the latest version of HTML and was officially released in October 2014. It brings a significant evolution to web development by introducing new features, elements, and APIs. HTML5 aims to enhance the capabilities of web browsers, improve multimedia support, and provide a more structured and semantic approach to content.

## Key Features of HTML5:

- Native support for audio and video elements (`<audio>` and `<video>`).
- Introduction of semantic elements like `<article>`, `<section>`, `<nav>`, `<header>`, and `<footer>`.
- Support for offline web applications using the Application Cache.
- Improved form elements and attributes, including new input types like email, tel, and date.
- Introduction of the `<canvas>` element for drawing graphics using JavaScript.
- Native support for geolocation with the Geolocation API.
- Enhanced support for local storage with the Web Storage API.

HTML5 has become the standard for modern web development, offering a more feature-rich and semantic approach to building web applications compared to its predecessors. It has played a crucial role in shaping the contemporary web landscape.


## 58. **What is HTML5, and how is it different from HTML?**
   - **Answer:** HTML5 is the latest version of HTML, introducing new features, elements, and APIs to enhance web development. It provides better multimedia support, introduces semantic elements, and improves the overall structure of web documents.

## 59. **Can you mention some new semantic elements introduced in HTML5?**
   - **Answer:** HTML5 introduced semantic elements like `<article>`, `<section>`, `<nav>`, `<header>`, `<footer>`, `<aside>`, `<figure>`, and `<figcaption`. These elements enhance the meaning and structure of web content.

## 60. **What is the purpose of the `<canvas>` element in HTML5?**
   - **Answer:** The `<canvas>` element provides a drawing space for graphics using JavaScript. It allows developers to draw shapes, images, and other graphical elements dynamically on the web page.

## 61. **Explain the significance of the `<video>` and `<audio>` elements in HTML5.**
   - **Answer:** `<video>` and `<audio>` elements provide native support for embedding video and audio content without the need for plugins like Flash. They offer a standardized way to include multimedia content in web pages.

## 62. **How does the Geolocation API in HTML5 work?**
   - **Answer:** The Geolocation API allows obtaining the user's geographical location using JavaScript. It provides information such as latitude, longitude, and altitude, enabling location-based functionality in web applications.

## 63. **What is local storage in HTML5, and how does it differ from session storage?**
   - **Answer:** Local storage is a part of the Web Storage API in HTML5, providing a way to store key/value pairs in the user's browser. It persists even after the browser is closed. Session storage, on the other hand, is temporary and lasts only for the duration of a page session.

## 64. **Explain the difference between the `<article>` and `<section>` elements in HTML5.**
   - **Answer:** `<article>` is used to represent a self-contained piece of content that can be distributed and reused independently, while `<section>` is a generic sectioning element that defines a thematic grouping of content.

## 65. **How can you implement responsive design in HTML5?**
   - **Answer:** Responsive design in HTML5 involves using media queries in CSS to adapt the layout based on the user's device characteristics, such as screen size. It allows the web page to display properly on various devices.

## 66. **What is the purpose of the `<details>` and `<summary>` elements in HTML5?**
   - **Answer:** The `<details>` element represents a disclosure widget from which the user can obtain additional information. The `<summary>` element provides a summary or label for the content within the `<details>` element.

## 67. **How can you embed custom fonts in a web page using HTML5 and CSS3?**
    - **Answer:** Use the `@font-face` rule in CSS3 to embed custom fonts. Example:
      ```css
      @font-face {
        font-family: 'CustomFont';
        src: url('custom-font.woff2') format('woff2');
      }
      body {
        font-family: 'CustomFont', sans-serif;
      }
      ```

