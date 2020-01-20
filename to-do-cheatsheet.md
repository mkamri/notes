# The To-Do List: what you need to know

Here are all the tools you need to complete [this tutorial](https://youtu.be/b8sUhU_eq3g) on how to make a to-do list app using JavaScript. I've also linked all of the resources I used for my information, as well. Enjoy! 

### Table of Contents

[insertAdjacentHTML()](#insert-adjacent-html)\
[addEventListener()](#add-an-event-listener)\
[Get the Value of Text Input Field](#get-the-value-of-text-input-field) 

## Insert Adjacent HTML

[MDN documentation](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentHTML) 
[Multiline HTML Template Strings](https://wesbos.com/template-strings-html/)
 
**SYNTAX**: 
```element.insertAdjacentHTML(position, text);``` 
 
*position*: 'beforebegin', 'afterbegin', 'beforeend', 'afterend' 
 
*text*: the string to be parsed as HTML. Use backticks (``) for multiline HTML strings.

## Add an Event Listener

[MDN documentation](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)

**SYNTAX**: 
```target.addEventListener(type, listener)``` 
 
*type*: 'keyup', 'click', etc. 
 
*listener*: The object that receives a notification of the event (like a JavaScript function) 
 
*example:*
```
document.addEventListener("keyup", function(event){
    if(event.keyCode == 13){
        console.log("The ENTER key was pressed!");
    }
});
```

## Get the Value of Text Input Field

[TutorialRepublic Resource](https://www.tutorialrepublic.com/faq/how-to-get-the-value-of-text-input-field-using-javascript.php) 

**SYNTAX**:
```
const inputBox = document.getElementByID("inputBox");
inputBox.value
``` 

