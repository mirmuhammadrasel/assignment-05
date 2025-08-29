### 6. Answer the following questions clearly:

1. What is the difference between **getElementById, getElementsByClassName, and querySelector / querySelectorAll**?
2. How do you **create and insert a new element into the DOM**?
3. Insert into the DOM → use methods like:

appendChild() → adds inside at the end.

prepend() → adds inside at the beginning.

before() / after() → adds outside before or after a node.
4. What is **Event Delegation** in JavaScript? Why is it useful?
5. What is the difference between **preventDefault() and stopPropagation()** methods?



Ans 1: The differences between getElementById, getElementsByClassName, and querySelector / querySelectorAll are 
1 getElementById("id")

.Selects only one element by its id.

.Always returns a single element (since id should be unique).

2 getElementsByClassName("className")

.Selects all elements with a given class.

.Returns an HTMLCollection (like a list), so you usually loop through it.

3 querySelector("css selector")

.Lets you use a CSS selector (like #id, .class, div p, etc.).

.Returns only the first matching element.

4 querySelectorAll("css selector")

.Same as querySelector, but returns all matching elements.

.Gives a NodeList, which you can also loop through.

Ans 2: To creat and insert a new element in DOM-

1 Create the element → use document.createElement("tagName").
Example: let newDiv = document.createElement("div");

2 Add content or attributes → like text or class.
Example: newDiv.textContent = "Hello World";

3 Insert into the DOM → use methods like:

.appendChild() → adds inside at the end.

.prepend() → adds inside at the beginning.

.before() / after() → adds outside before or after a node.

Ans 3: Insert into the DOM → main methods

.appendChild() → puts the new element inside a parent, at the end.

.prepend() → puts it inside a parent, at the beginning.

.before() → inserts it just before a target element (outside it).

.after() → inserts it just after a target element (outside it).

Ans 4: Event delegation means putting the event listener on a parent element, instead of each child element.

The event bubbles up from the child to the parent, so the parent can “catch” the event.

Why it is useful:

Less code → You don’t need to add event listeners on every single child.

Better performance → One listener handles many elements.

Dynamic elements → If new child elements are added later, the parent listener still works for them.

Ans 5: 
Difference between preventDefault() and stopPropagation()

preventDefault()

Stops the default action of an element.

Example: Clicking a link won’t go to another page, submitting a form won’t reload.

stopPropagation()

Stops the event from bubbling up to parent elements.

Example: If a button is inside a div, the button’s event won’t reach the div.