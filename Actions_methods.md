1. Creating an Actions Object
To use the Actions class, you need to initialize it:

java
Copy code
Actions actions = new Actions(driver);
2. Methods in the Actions Class
a. click()
Performs a single left mouse click on the current element.

java
Copy code
actions.click(element).perform();
b. clickAndHold()
Performs a click-and-hold at the current mouse location or on the specified element.

java
Copy code
actions.clickAndHold(element).perform();
c. contextClick()
Performs a right-click (context click) at the current mouse location or on the specified element.

java
Copy code
actions.contextClick(element).perform();
d. doubleClick()
Performs a double-click at the current mouse location or on the specified element.

java
Copy code
actions.doubleClick(element).perform();
e. dragAndDrop()
Performs a drag-and-drop from the source element to the target element.

java
Copy code
actions.dragAndDrop(sourceElement, targetElement).perform();
f. dragAndDropBy()
Drags an element and drops it by an offset (x, y).

java
Copy code
actions.dragAndDropBy(element, xOffset, yOffset).perform();
g. moveToElement()
Moves the mouse pointer to the center of the specified element.

java
Copy code
actions.moveToElement(element).perform();
h. moveByOffset()
Moves the mouse pointer from the current location by an offset (x, y).

java
Copy code
actions.moveByOffset(xOffset, yOffset).perform();
i. release()
Releases a pressed mouse button at the current mouse location or on the specified element.

java
Copy code
actions.release().perform();
j. keyDown()
Simulates pressing a modifier key (e.g., Shift, Ctrl, Alt) on the keyboard.

java
Copy code
actions.keyDown(Keys.CONTROL).perform();
k. keyUp()
Simulates releasing a modifier key.

java
Copy code
actions.keyUp(Keys.CONTROL).perform();
l. sendKeys()
Sends a sequence of keys to the active element or a specified element.

java
Copy code
actions.sendKeys(element, "text").perform();
m. pause()
Pauses the action for a specified duration.

java
Copy code
actions.pause(Duration.ofSeconds(2)).perform();
n. build()
Compiles all actions into a single composite action. Use this when chaining multiple actions.

java
Copy code
Action action = actions.moveToElement(element).click().build();
action.perform();
o. perform()
Executes the compiled actions.

java
Copy code
actions.perform();
3. Example: Chaining Actions
The Actions class allows chaining multiple methods:

java
Copy code
actions.moveToElement(element)
       .clickAndHold()
       .moveByOffset(50, 0)
       .release()
       .perform();
