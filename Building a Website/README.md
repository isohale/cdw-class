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

**Example of HTML structure:**
```html
<!-- This is the main heading of our webpage -->
<h1>Welcome to My Website</h1>

<!-- This is a paragraph with some text -->
<p>This is my first website built with HTML, CSS, and JavaScript!</p>

<!-- This creates a button that users can click -->
<button>Click Me!</button>

<!-- This is a container that holds other elements -->
<div>
    <h2>About Me</h2>
    <p>I'm learning web development.</p>
</div>
```

#### **CSS (Cascading Style Sheets) - The Design**
CSS handles the **styling and visual presentation** of your website. It controls how everything looks and is arranged.

**What CSS does:**
- Controls colors, fonts, and text styling
- Arranges elements on the page (layout)
- Adds spacing, borders, and backgrounds
- Makes websites responsive (work on different screen sizes)
- Creates animations and visual effects

**Example of CSS styling:**
```css
/* This makes the main heading red and centered */
h1 {
    color: red;           /* Text color */
    text-align: center;   /* Center the text */
    font-size: 24px;      /* Make text bigger */
}

/* This styles paragraphs with blue text and some spacing */
p {
    color: blue;
    margin: 10px 0;       /* Add space above and below */
    line-height: 1.5;     /* Space between lines */
}

/* This makes the button look nice with a background and border */
button {
    background-color: green;    /* Green background */
    color: white;               /* White text */
    padding: 10px 20px;         /* Space inside the button */
    border: none;               /* Remove default border */
    border-radius: 5px;         /* Rounded corners */
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

**Example of JavaScript functionality:**
```javascript
// This code runs when the page loads
document.addEventListener('DOMContentLoaded', function() {
    // Find the button on our page
    const button = document.querySelector('button');
    
    // When someone clicks the button, do something
    button.addEventListener('click', function() {
        // Change the button text
        button.textContent = 'You clicked me!';
        
        // Change the button color
        button.style.backgroundColor = 'orange';
        
        // Show a message to the user
        alert('Hello! You clicked the button!');
    });
});
```

#### **How They Work Together**
1. **HTML** provides the structure and content
2. **CSS** makes it look good and organized
3. **JavaScript** makes it interactive and dynamic

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
my-website/
├── index.html      (HTML structure)
├── styles.css      (CSS styling)
└── script.js       (JavaScript functionality)
```

#### **HTML File (index.html)**
```html
<!DOCTYPE html>
<!-- This tells the browser this is an HTML5 document -->
<html lang="en">
<!-- The html tag contains everything on the page -->

<head>
    <!-- The head contains information about the page, not visible content -->
    
    <!-- This sets the character encoding for the page -->
    <meta charset="UTF-8">
    
    <!-- This makes the page responsive on mobile devices -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- This is the title that appears in the browser tab -->
    <title>My First Website</title>
    
    <!-- This links our CSS file to style the page -->
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <!-- The body contains all the visible content on the page -->
    
    <!-- This is the main heading of our website -->
    <header>
        <h1>Welcome to My Website</h1>
        <p>Built with HTML, CSS, and JavaScript</p>
    </header>
    
    <!-- This is the main content area -->
    <main>
        <section>
            <h2>About This Website</h2>
            <p>This is a simple website created to learn web development fundamentals.</p>
        </section>
        
        <section>
            <h2>Interactive Elements</h2>
            <!-- This button will be styled by CSS and made interactive by JavaScript -->
            <button id="changeColorBtn">Change Background Color</button>
            <button id="showMessageBtn">Show Message</button>
        </section>
    </main>
    
    <!-- This is the footer at the bottom of the page -->
    <footer>
        <p>&copy; 2024 My First Website. All rights reserved.</p>
    </footer>
    
    <!-- This links our JavaScript file - always put it at the end of the body -->
    <script src="script.js"></script>
</body>
</html>
```

#### **CSS File (styles.css)**
```css
/* Reset default browser styles for consistent appearance */
* {
    margin: 0;          /* Remove default margins */
    padding: 0;         /* Remove default padding */
    box-sizing: border-box; /* Include padding in element width */
}

/* Style the entire body of the page */
body {
    font-family: Arial, sans-serif;  /* Choose a nice font */
    line-height: 1.6;                /* Space between lines */
    color: #333;                     /* Dark gray text color */
    background-color: #f4f4f4;       /* Light gray background */
}

/* Style the header section */
header {
    background-color: #2c3e50;       /* Dark blue background */
    color: white;                    /* White text */
    text-align: center;              /* Center the text */
    padding: 2rem 0;                 /* Add space inside */
    margin-bottom: 2rem;             /* Add space below */
}

/* Style the main heading */
h1 {
    font-size: 2.5rem;               /* Large text size */
    margin-bottom: 0.5rem;           /* Space below the heading */
}

/* Style all headings */
h2 {
    color: #2c3e50;                  /* Dark blue color */
    margin-bottom: 1rem;             /* Space below headings */
    border-bottom: 2px solid #3498db; /* Blue underline */
    padding-bottom: 0.5rem;          /* Space above the line */
}

/* Style paragraphs */
p {
    margin-bottom: 1rem;             /* Space below paragraphs */
    font-size: 1.1rem;               /* Slightly larger text */
}

/* Style the main content area */
main {
    max-width: 800px;                /* Limit width for readability */
    margin: 0 auto;                  /* Center the content */
    padding: 0 20px;                 /* Add space on the sides */
}

/* Style sections */
section {
    background-color: white;         /* White background */
    padding: 2rem;                   /* Space inside sections */
    margin-bottom: 2rem;             /* Space between sections */
    border-radius: 8px;              /* Rounded corners */
    box-shadow: 0 2px 5px rgba(0,0,0,0.1); /* Subtle shadow */
}

/* Style buttons */
button {
    background-color: #3498db;       /* Blue background */
    color: white;                    /* White text */
    border: none;                    /* Remove default border */
    padding: 12px 24px;              /* Space inside button */
    font-size: 1rem;                 /* Button text size */
    border-radius: 5px;              /* Rounded corners */
    cursor: pointer;                 /* Hand cursor on hover */
    margin-right: 10px;              /* Space between buttons */
    transition: background-color 0.3s; /* Smooth color change */
}

/* Change button color when you hover over it */
button:hover {
    background-color: #2980b9;       /* Darker blue on hover */
}

/* Style the footer */
footer {
    text-align: center;              /* Center the text */
    padding: 2rem;                   /* Space inside footer */
    background-color: #2c3e50;       /* Dark background */
    color: white;                    /* White text */
    margin-top: 2rem;                /* Space above footer */
}
```

#### **JavaScript File (script.js)**
```javascript
// Wait for the HTML page to fully load before running our JavaScript
document.addEventListener('DOMContentLoaded', function() {
    // This function runs when the page is ready
    
    console.log('Website loaded successfully!'); // This shows in browser console
    
    // Get references to our buttons using their IDs
    const changeColorBtn = document.getElementById('changeColorBtn');
    const showMessageBtn = document.getElementById('showMessageBtn');
    
    // Array of different background colors we can cycle through
    const colors = ['#f4f4f4', '#ffe6e6', '#e6ffe6', '#e6e6ff', '#fff2e6'];
    let currentColorIndex = 0; // Keep track of which color we're on
    
    // Add click event listener to the "Change Background Color" button
    changeColorBtn.addEventListener('click', function() {
        // Move to the next color in our array
        currentColorIndex = (currentColorIndex + 1) % colors.length;
        
        // Change the body background color
        document.body.style.backgroundColor = colors[currentColorIndex];
        
        // Show a message to the user
        alert('Background color changed!');
        
        // Log the change to the console (for debugging)
        console.log('Background color changed to:', colors[currentColorIndex]);
    });
    
    // Add click event listener to the "Show Message" button
    showMessageBtn.addEventListener('click', function() {
        // Create a new paragraph element
        const newMessage = document.createElement('p');
        
        // Set the text content of the new paragraph
        newMessage.textContent = 'Hello! This message was added by JavaScript!';
        
        // Add some styling to make it stand out
        newMessage.style.color = '#e74c3c';
        newMessage.style.fontWeight = 'bold';
        
        // Find the section with the buttons and add our new message
        const buttonSection = showMessageBtn.closest('section');
        buttonSection.appendChild(newMessage);
        
        // Show a confirmation message
        alert('Message added to the page!');
    });
    
    // Add a welcome message when the page loads
    setTimeout(function() {
        alert('Welcome to my website! Click the buttons to see some interactivity.');
    }, 1000); // Wait 1 second before showing the message
});
```

#### **How to Use These Files**
1. Create a new folder called `my-website`
2. Create the three files with the exact names shown above
3. Copy the code into each file
4. Open `index.html` in your web browser
5. You should see a styled website with working buttons!

#### **What You'll See**
- A styled website with a header, main content, and footer
- Two interactive buttons that change the page
- Responsive design that works on different screen sizes
- Clean, professional appearance

This structure teaches you the separation of concerns: HTML for structure, CSS for styling, and JavaScript for behavior!