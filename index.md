# Web Development Quick Notes

## Day 1: The Basics

### 1. `<script>` vs. `<noscript>`

* **`<script>`:** This is where you put your JavaScript code. The browser runs whatever is inside this tag. It's what makes websites interactive.
* **`<noscript>`:** This is a fallback. If a user has JavaScript disabled in their browser, or if their browser doesn't support it, the content inside the `<noscript>` tag will be displayed instead. It's a way to provide a basic experience for everyone.

### 2. `<link>` and `<meta>`

* **`<link>`:** Think of this as a bridge to other files. Its most common use is to link your HTML to a CSS stylesheet, which is what makes your website look good. You can also use it for things like favicons (the little icon in the browser tab).
* **`<meta>`:** This tag provides "meta-information" about your HTML document that isn't displayed on the page itself. It's for the browser and search engines. You use it to set the character set (`UTF-8`), provide a description for search results, and specify keywords.

## Day 2: Images and Movement

### 1. `<img>` and `<marquee>`

* **`<img>`:** This is how you put images on your webpage. It's a self-closing tag.
* **`<marquee>`:** This creates a scrolling text or image. It's an older tag and not really used in modern web design because it can be distracting and is considered bad for user experience. CSS animations are the modern way to create movement.

### 2. Attributes for `<img>` and `<marquee>`

* **`<img>` Attributes:**
    * `src`: This is the most important one. It specifies the path to the image file.
    * `alt`: This provides alternative text for the image if it can't be displayed. It's crucial for accessibility (screen readers) and SEO.
    * `width` & `height`:  Sets the dimensions of the image. It's good practice to include these to prevent the page layout from shifting as images load.
    * `title`:  A tooltip that appears when you hover over the image.

* **`<marquee>` Attributes:**
    * `behavior`:  Can be `scroll` (default), `slide` (stops at the end), or `alternate` (bounces back and forth).
    * `direction`:  `left`, `right`, `up`, or `down`.
    * `scrollamount`:  Controls the speed of the scroll.

## Day 3: Forms and User Input

### 1. `<form>`, `<fieldset>`, and `<label>`

* **`<form>`:** This is the container for all your input elements like text boxes, buttons, etc. It's what groups them together to be submitted.
* **`<fieldset>`:** Used to group related elements within a form. It draws a box around the elements, making the form easier to read and understand.
* **`<label>`:** This provides a descriptive label for an input field. Clicking on the label will focus on the associated input, which is great for usability.

### 2. `required` and `placeholder`

* **`required`:** An attribute you can add to an input field to make it mandatory. The user won't be able to submit the form until they fill out that field.
* **`placeholder`:** This is the light grey text you see inside an input field that gives a hint about what to enter (e.g., "Enter your name"). It disappears as soon as you start typing.

### 3. `method` and `action`

* **`method`:** Specifies how the form data should be sent to the server. The two most common values are:
    * `GET`:  Appends the form data to the URL. Good for search forms, but not for sensitive data.
    * `POST`:  Sends the form data in the body of the HTTP request. More secure and used for submitting personal information.
* **`action`:** This attribute specifies the URL where the form data should be sent for processing when the user hits "submit."

## Day 4: Layout and Styling

### 1. The `<div>`

* **Purpose of `<div>`:** It's a generic container. By itself, it does nothing. Its real power comes when you use it with CSS. You can group sections of your content within `<div>`s and then style those entire sections at once. It's the fundamental building block for modern web layouts.

### 2. CSS: `border`, `height`, `width`

* **`border`:** Lets you add a line around an element. You can control its `width`, `style` (solid, dashed, etc.), and `color`.
* **`height` & `width`:** These properties do exactly what they say: they set the height and width of an element. You can use pixels (`px`), percentages (`%`), or other units.

### 3. `float: left` vs. `float: right`

* **`float`:** This CSS property was originally used to wrap text around images.
    * `float: left;`:  Pushes the element to the left, and allows other content to flow around it on the right.
    * `float: right;`: Pushes the element to the right, and allows other content to flow around it on the left.
* **Note:** While `float` is still used, modern layouts are more commonly built with Flexbox or CSS Grid because they offer more control and flexibility.

## Day 5: Spacing, Style, and Backgrounds

### 1. `padding` vs. `margin`

* **`padding`:** This is the space *inside* an element, between the content and the border. Think of it as adding "breathing room" around your text or image within its box.
* **`margin`:** This is the space *outside* an element, between its border and other elements on the page. It's used to push elements away from each other.

### 2. CSS Box Shadows

* **`box-shadow`:** A CSS property that lets you add a shadow effect around an element's frame. You can specify the horizontal and vertical offset, the blur radius, the spread radius, and the color of the shadow. It's a great way to add depth and make elements pop.

### 3. HTML Entities

* **What are they?** Sometimes you need to display characters that have a special meaning in HTML, like `<` or `>`. HTML entities are codes you can use to display these characters correctly.
* **Common Examples:**
    * `&lt;` for `<` (less than)
    * `&gt;` for `>` (greater than)
    * `&amp;` for `&` (ampersand)
    * `&copy;` for the copyright symbol ©

### 4. `background-image` vs. `background-color`

* **`background-color`:** Sets a solid color for the background of an element.
* **`background-image`:** Sets an image as the background. You can control how it repeats, its position, and its size. If you set both, the background image will appear on top of the background color.

## Day 6: Modern Layouts and Positioning

### 1. Flexbox Layout

* **Flexbox:** A modern and powerful CSS layout model that makes it easy to arrange, align, and distribute space among items in a container, even when their size is unknown or dynamic. It's a one-dimensional layout system (either a row or a column).

### 2. Header/Sidebar/Footer with Flexbox

* Flexbox is perfect for creating the common header, sidebar, and footer layout. You can easily make the main content area flexible to fill the available space while the header and footer have fixed heights, and the sidebar has a fixed width.

### 3. `flex-direction`, `justify-content`, `align-items`

* These are key Flexbox properties:
    * **`flex-direction`:** Defines the main axis of the flex container. `row` (default, left-to-right), `row-reverse`, `column` (top-to-bottom), or `column-reverse`.
    * **`justify-content`:** Aligns items along the main axis. You can space them out (`space-between`, `space-around`), center them (`center`), or push them to the start or end.
    * **`align-items`:** Aligns items along the cross axis (the axis perpendicular to `flex-direction`). You can center them, stretch them to fill the space, or align them to the start or end.

### 4. Responsive Layout

* A responsive layout is one that adapts to different screen sizes, from large desktop monitors to small mobile phones. Flexbox is a key tool for creating responsive designs because it allows elements to grow, shrink, and wrap onto new lines as the screen size changes. Media queries in CSS are used to apply different styles at different screen widths.

### 5. CSS `position`

* The `position` property in CSS determines how an element is positioned in the document.
    * **`static`:** The default. The element is in the normal flow of the page.
    * **`relative`:** The element is positioned relative to its normal position. You can then use `top`, `right`, `bottom`, and `left` to move it around.
    * **`absolute`:** The element is removed from the normal flow and positioned relative to its nearest positioned ancestor (an ancestor that isn't `static`). If there's no positioned ancestor, it's positioned relative to the `<body>`.
    * **`fixed`:** The element is removed from the normal flow and positioned relative to the browser window. It will stay in the same place even when you scroll. Great for "sticky" navigation bars.