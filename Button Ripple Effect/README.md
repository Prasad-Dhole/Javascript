Javascript snippet expectations --> 
This code is typically used to create a hover effect where something (like a spotlight, gradient, or pseudo-element) follows the mouse cursor when it moves over the button. The --xPos and --yPos variables would be used in the CSS to position an effect relative to the mouse position within the button.



Event Listener code snippet in app.js -->
btnEl.addEventListener("mouseover", (event) => { ... });
    This attaches an event listener to the button element
    It listens for a "mouseover" event (when the mouse cursor moves over the button)
    When triggered, it executes an arrow function that takes an event parameter
    The event object contains information about the mouse event

Inside the event handler:->
const x = event.pageX - btnEl.offsetLeft;
    event.pageX gives the mouse's horizontal position relative to the entire page
    btnEl.offsetLeft gives the button's left position relative to its offset parent
    Subtracting these gives the mouse's x-coordinate relative to the button's left edge

const y = event.pageY - btnEl.offsetTop;
    event.pageY gives the mouse's vertical position relative to the entire page
    btnEl.offsetTop gives the button's top position relative to its offset parent

Subtracting these gives the mouse's y-coordinate relative to the button's top edge

