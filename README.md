# Uncommon HTML Bug: Event Listener on Non-Existent Element

This repository demonstrates a subtle bug in HTML related to event listeners and element existence.  The `bug.html` file showcases the incorrect implementation, while `bugSolution.html` provides the corrected version.  The core issue involves attaching an event listener to an element before the element is fully parsed and rendered by the browser. This can lead to the event listener not functioning correctly.

## Bug Description
The bug involves adding an event listener to a div element using the traditional method. However,if the div element is not yet available when the script runs, the event listener will not be attached correctly. 

## Solution
The solution utilizes event delegation; the event listener is attached to a parent element. This ensures the listener is active even if the target element is added dynamically after the script has run.