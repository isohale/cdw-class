# Introduction to building a website
## HTML, CSS and JavaScript

Welcome to the world of web development! This tutorial will teach you the fundamentals of building websites using the three core technologies: HTML, CSS, and JavaScript. We'll learn how these languages work together to create modern, interactive websites.

---

### 1  The Role of HTML, CSS and JavaScript

#### **HTML (HyperText Markup Language) - The Structure**
HTML provides the **foundation and framework** for your website. It defines the basic structure and content.

**What HTML does:**
- Defines the structure of your webpage
- Contains all the text content
- Creates headings, paragraphs, lists, and links
- Adds images, forms, and other elements
- Provides meaning and organization to your content

**Key HTML Elements from our website:**
```html
<!-- Basic HTML structure -->
<!DOCTYPE html>                    <!-- Declares this is an HTML5 document -->
<html lang="en">                   <!-- Root element, lang="en" specifies English language -->
<head>                             <!-- Contains metadata about the page (not visible) -->
  <meta charset="UTF-8">           <!-- Sets character encoding for special characters -->
  <title>Module 1</title>          <!-- Title that appears in browser tab -->
  <link rel="stylesheet" href="style.css">  <!-- Links to our CSS file for styling -->
</head>
<body>                             <!-- Contains all visible content on the page -->
  <!-- Content goes here -->       <!-- Placeholder comment for where content would be -->
  <script src="script.js"></script>  <!-- Links to our JavaScript file for interactivity -->
</body>
</html>

<!-- Interactive elements with IDs for JavaScript -->
<button id="demoButton">Click Me!</button>  <!-- Clickable button with unique ID for JavaScript -->
<div id="messageDisplay"></div>            <!-- Empty container div with ID for JavaScript to fill -->
```

#### **CSS (Cascading Style Sheets) - The Design**
CSS handles the **styling and visual presentation** of your website. It controls how everything looks and is arranged.

**What CSS does:**
- Controls colors, fonts, and text styling
- Arranges elements on the page (layout)
- Adds spacing, borders, and backgrounds
- Makes websites responsive (work on different screen sizes)
- Creates animations and visual effects

**Key CSS Properties from our website:**
```css
/* Basic styling for the page */
body {
  font-family: 'Roboto', sans-serif;  /* Set the font */
  background-color: #ffffff;          /* White background */
  color: #111;                        /* Dark text color */
  margin: 0;                          /* Remove default spacing */
}

/* Interactive button styling */
button {
  background-color: #111;             /* Dark background */
  color: white;                       /* White text */
  padding: 12px 24px;                 /* Internal spacing */
  cursor: pointer;                    /* Hand cursor on hover */
  transition: background-color 0.3s;  /* Smooth color change */
}

/* Hover effect for buttons */
button:hover {
  background-color: #333;             /* Lighter background on hover */
}
```

#### **JavaScript - The Interactivity**
JavaScript adds **interactivity and dynamic behavior** to your website. It makes things happen when users interact with your page.

**What JavaScript does:**
- Responds to user actions (clicks, typing, etc.)
- Changes content on the page without reloading
- Validates forms and user input
- Creates animations and effects
- Connects to databases and external services
- Makes websites dynamic and interactive

**Key JavaScript Concepts from our website:**
```javascript
// Wait for the page to load before running JavaScript
document.addEventListener('DOMContentLoaded', function() {
    
    // Find HTML elements using their IDs
    const button = document.getElementById('demoButton');
    const messageArea = document.getElementById('messageDisplay');
    
    // Add click event listener to the button
    button.addEventListener('click', function() {
        // Get current time and create a message
        const currentTime = new Date().toLocaleTimeString();
        const message = 'Hello! You clicked the button at ' + currentTime;
        
        // Display the message in our HTML
        messageArea.textContent = message;
        
        // Change button text temporarily
        button.textContent = 'Thanks for clicking!';
    });
});
```

#### **How They Work Together**
1. **HTML** provides the structure and content (buttons, text areas)
2. **CSS** makes it look good and organized (colors, spacing, hover effects)
3. **JavaScript** makes it interactive and dynamic (responds to clicks, changes content)

---

### 2  Boilerplate code (using separate files)

While it's possible to put HTML, CSS, and JavaScript all in one file, we'll use **separate files** for better organization and learning. This approach helps you understand the role of each language clearly.

#### **Why Separate Files?**
- **Clearer organization**: Each file has one specific purpose
- **Easier to maintain**: Changes to styling don't affect structure
- **Better collaboration**: Different people can work on different files
- **Professional practice**: This is how real websites are built
- **Easier debugging**: Problems are easier to find and fix

#### **File Structure**
```
Building a Website/
├── index.html      (HTML structure and content)
├── style.css       (CSS styling and layout)
├── script.js       (JavaScript functionality)
└── README.md       (This tutorial)
```

#### **HTML File Structure (index.html)**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Module 1</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <div class="left">Columbia GSAPP</div>
    <div class="center">
      Computational Design Practices<br>
      <span>Project Archive</span>
    </div>
    <div class="right"><a href="#">About</a></div>
  </header>

  <main>
    <div class="project-meta">2025</div>
    <div class="project-title">Project Title</div>
    <div class="project-subtitle">Student Name</div>
    
    <!-- Content sections -->
    <div class="section-title">Interactive Demo</div>
    <p>Click the button below to see JavaScript in action:</p>
    <button id="demoButton">Click Me!</button>
    <div id="messageDisplay"></div>
  </main>
  
  <script src="script.js"></script>
</body>
</html>
```

**Key HTML Concepts:**
- **Document structure**: DOCTYPE, html, head, body
- **Linking files**: CSS with `<link>`, JavaScript with `<script>`
- **Semantic elements**: header, main, div, p, button
- **IDs and classes**: `id="demoButton"` for JavaScript, `class="section-title"` for CSS

#### **CSS File Structure (style.css)**
```css
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');

body {
  font-family: 'Roboto', sans-serif;
  background-color: #ffffff;
  color: #111;
  margin: 0;
  padding: 0;
}

main {
  max-width: 800px;
  margin: 60px auto;
  padding: 0 20px;
}

.section-title {
  font-weight: 700;
  text-transform: uppercase;
  margin-top: 40px;
  margin-bottom: 12px;
  font-size: 14px;
}

button {
  background-color: #111;
  color: white;
  border: none;
  padding: 12px 24px;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #333;
}

#messageDisplay {
  margin-top: 20px;
  padding: 16px;
  border: 1px solid #ccc;
  background-color: #f9f9f9;
  min-height: 20px;
}
```

**Key CSS Concepts:**
- **Selectors**: Element selectors (`body`), class selectors (`.section-title`), ID selectors (`#messageDisplay`)
- **Properties**: Colors, fonts, spacing, layout
- **Units**: Pixels (px), percentages (%), viewport units (vw, vh)
- **Pseudo-classes**: `:hover` for interactive effects
- **Transitions**: Smooth animations between states

#### **JavaScript File Structure (script.js)**
```javascript
document.addEventListener('DOMContentLoaded', function() {
    console.log('JavaScript is now running!');
    
    // Find HTML elements by their IDs
    const button = document.getElementById('demoButton');
    const messageArea = document.getElementById('messageDisplay');
    
    // Add click event listener to the button
    button.addEventListener('click', function() {
        console.log('Button was clicked!');
        
        // Create a message with current time
        const currentTime = new Date().toLocaleTimeString();
        const message = 'Hello! You clicked the button at ' + currentTime;
        
        // Display the message in our HTML
        messageArea.textContent = message;
        
        // Change button text temporarily
        button.textContent = 'Thanks for clicking!';
        
        // Reset button text after 2 seconds
        setTimeout(function() {
            button.textContent = 'Click Me!';
        }, 2000);
    });
});
```

**Key JavaScript Concepts:**
- **Event listeners**: Responding to user actions (`click`, `DOMContentLoaded`)
- **DOM manipulation**: Finding and changing HTML elements
- **Functions**: Reusable blocks of code
- **Variables**: Storing data (`const`, `let`)
- **Timing**: `setTimeout` for delayed actions
- **Console logging**: Debugging and development tools

#### **How the Files Connect**
1. **HTML** (`index.html`) contains the structure and links to CSS and JavaScript
2. **CSS** (`style.css`) styles the HTML elements using selectors
3. **JavaScript** (`script.js`) finds HTML elements by ID and makes them interactive

**The Connection Points:**
- HTML links CSS: `<link rel="stylesheet" href="style.css">`
- HTML links JavaScript: `<script src="script.js"></script>`
- CSS targets HTML: `#demoButton`, `.section-title`
- JavaScript finds HTML: `document.getElementById('demoButton')`

#### **Complete Working Website**
The source code files (`index.html`, `style.css`, `script.js`) contain the complete working website with:
- **Full HTML structure** with semantic elements and proper organization
- **Comprehensive CSS styling** with responsive design and interactive effects
- **Complete JavaScript functionality** with event handling and DOM manipulation
- **Detailed comments** throughout all files for learning purposes

To see the website in action:
1. Open `index.html` in any web browser
2. Click the "Click Me!" button to see JavaScript functionality
3. Observe how the three files work together to create an interactive experience

This separation of concerns makes the code easier to understand, maintain, and learn from!