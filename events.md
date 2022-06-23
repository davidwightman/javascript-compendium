## Event-Driven Programming

### Event Propagation

- The process by which an event travels throught the DOM to call event listeners on nested elements. Event propagation consists of 3 phases:

1. capturing: the event travels down from the root of the document to the event target
2. target: the event fires on the event target
3. Bubbling: the event travels up from the event target to the root of the document

- at any point in the process you can call `event.stopPropagation()`

- Event Delegation: the process of using a single event listener on a parent element to manually delegate events to children, rather than using event listeners on a child.

click

resize

keydown, keypress, keyup

mouseover

load

///

addEventListener
