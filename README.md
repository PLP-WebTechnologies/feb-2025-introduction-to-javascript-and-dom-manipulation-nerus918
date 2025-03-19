# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dynamic JavaScript Example</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1 id="title">Welcome to Dynamic Web Page!</h1>
    
    <button id="changeTextBtn">Change Text</button>
    <button id="changeStyleBtn">Change Style</button>
    <button id="toggleElementBtn">Toggle Element</button>

    <div id="dynamicElement" class="hidden">This is a dynamically added element!</div>

    <script src="script.js"></script>
</body>
</html>

// Select elements
const title = document.getElementById('title');
const changeTextBtn = document.getElementById('changeTextBtn');
const changeStyleBtn = document.getElementById('changeStyleBtn');
const toggleElementBtn = document.getElementById('toggleElementBtn');
const dynamicElement = document.getElementById('dynamicElement');

// Change text content when the "Change Text" button is clicked
changeTextBtn.addEventListener('click', function() {
    title.textContent = "The Text Has Been Changed!";
});

// Change CSS styles when the "Change Style" button is clicked
changeStyleBtn.addEventListener('click', function() {
    title.style.color = "blue";
    title.style.fontSize = "3rem";
});

// Toggle visibility of the dynamically added element when the "Toggle Element" button is clicked
toggleElementBtn.addEventListener('click', function() {
    if (dynamicElement.classList.contains('hidden')) {
        dynamicElement.classList.remove('hidden');
        dynamicElement.classList.add('visible');
    } else {
        dynamicElement.classList.remove('visible');
        dynamicElement.classList.add('hidden');
    }
});


/* Default hidden class to hide elements */
.hidden {
    display: none;
}

/* Visible class to display elements */
.visible {
    display: block;
    margin-top: 20px;
    padding: 10px;
    background-color: lightyellow;
    border: 1px solid #ccc;
    text-align: center;
}

