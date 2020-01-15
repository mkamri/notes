# Basic JavaScript DOM Manipulation Cheatsheet

These are my notes on DOM manipulation. This cheatsheet uses a lot of info and charts based on [this tutorial](https://www.digitalocean.com/community/tutorial_series/understanding-the-dom-document-object-model), so please check it out for a fantastic in-depth guide on the basics of DOM manipulation with vanilla JavaScript!

## Accessing the DOM

| Grab it by the... | CSS selector syntax | Method                                  |
| ----------------- | ------------------- | --------------------------------------- |
| ID                | #selectorName       | getElementById('selectorName')          |
| Class             | .selectorName       | getElementByClassName('className')      |
| Tag               | tagName             | getElementByTagName('tagName')          |
| Selector (single) | [#/./ ]selectorName | querySelector('[#/./ ]selectorName')    |
| Selector (all)    | [#/./ ]selectorName | querySelectorAll('[#/./ ]selectorName') |

## Traversing the DOM

_Note: items in **bold** are most commonly used. Please check out [this reference guide](https://www.digitalocean.com/community/tutorials/how-to-traverse-the-dom) for more information on why._

### Parent Nodes

| Property       | Gets the...                        |
| -------------- | ---------------------------------- |
| **parentNode** | parent node                        |
| parentElement  | parent node that's also an element |

### Child Nodes

| Property              | Gets the...                             |
| --------------------- | --------------------------------------- |
| childNodes            | all child nodes                         |
| firstChild            | first child node                        |
| lastChild             | last child node                         |
| **children**          | child node that's also an element       |
| **firstElementChild** | first child node that's also an element |
| **lastElementChild**  | last child node that's also an element  |

### Sibling Nodes

| Property                   | Gets the...                                  |
| -------------------------- | -------------------------------------------- |
| previousSibling            | previous sibling node                        |
| nextSibling                | next sibling node                            |
| **previousElementSibling** | previous sibling node that's also an element |
| **nextElementSibling**     | next sibling node that's also an element     |

## Changing the DOM

### Creating New Nodes

| Property / Method                        | What it does:                        |
| ---------------------------------------- | ------------------------------------ |
| createElement('elementTag')              | create a new element node            |
| createTextNode("A lovely block of text") | create a new text node               |
| node.textContent                         | get/set text content of element node |
| node.innerHTML                           | get/set HTML content of element      |

### Inserting Nodes Into the DOM

| Property / Method                       | What it does:                                    |
| --------------------------------------- | ------------------------------------------------ |
| node.appendChild()                      | add a node as the last child of a parent element |
| node.insertBefore(newNode, nextSibling) | insert newNode before nextSibling                |
| node.replaceChild(newNode, oldNode)     | replace oldNode with newNode                     |

### Removing Nodes From the DOM

| Method                                        | What it does:                                                        |
| --------------------------------------------- | -------------------------------------------------------------------- |
| node.removeElementChild(node.specifyTheChild) | removes a child of a node (firstElementChild, lastElementChild, etc) |
| node.remove()                                 | removes a specified node from the DOM                                |

## Events

Two parts to an event:
Event **Handler**: A script that runs when an event occurs
Event **Listener**: Allows an element to wait and "listen" for an event to fire

### Inline Event Handler

Location: directly on the element in HTML
Example:
&lt;button onclick="js/script.js"&gt;

### Event Handler Property in JS

Location: JavaScript file
Example:
button.onclick = functionName;
_Note: all but the last will be ignored if you want more than one event handler with the same event (onclick, etc)_

### Event Listeners (common practice)

Location: JavaScript file
Example:
button.addEventListener('click', functionName);

### Anonymous Function Event Listener

Location: JavaScript file
Example:
button.addEventListener('click', () => {
p.textContent = "A glorious line of text";
})

## Some Common Events

### Mouse Events

| event      | triggered by...                        |
| ---------- | -------------------------------------- |
| click      | when mouse is pressed and released     |
| dbclick    | when an element is clicked twice       |
| mouseenter | pointer enters and element             |
| mouseleave | pointer leaves an element              |
| mousemove  | pointer moves around within an element |

### Form Events

| event  | triggered by...                |
| ------ | ------------------------------ |
| submit | when a form is submitted       |
| focus  | when an element receives focus |
| blur   | when an element loses focus    |

### Keyboard Events

| event    | triggered by...                                                 |
| -------- | --------------------------------------------------------------- |
| keydown  | when a key is pressed                                           |
| keyup    | when a key is released                                          |
| keypress | fires continuously while a key is pressed (only for characters) |
