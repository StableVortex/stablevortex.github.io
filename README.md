index.html
 
Function addChallenge(this):
This function is designed to add a challenge to the local storage of the browser. 
It is triggered when a user clicks the "Add challenge" button associated with a specific challenge card. The function extracts information about the challenge from the DOM, such as its name, distance, description, and price, and then stores this data in an array in the local storage. If the "challenges" array already exists in local storage, the function appends the new challenge to it; otherwise, it creates a new array.

CSS

Body: Sets the font family for the entire page to Arial, sans-serif.
Header: Styles the header with a light grey background, centered text alignment, and a bottom margin for spacing.
Navigation Links: Styles the navigation links within the header to remove text decoration and set the color to a dark grey.
Main Grid Layout: Utilizes CSS Grid to display challenge cards in a responsive grid layout. The number of columns adjusts based on the viewport width.

Challenge Card:
The .card class positions the card and adds spacing.
The .sub-card class adds a white background, shadow, border, and rounded corners to each card.
An image is absolutely positioned within each card.
The .content class provides padding and centers the text within the card.

summary.html

Function: window.onload:
This function is set to execute the displayChallenges function as soon as the window is fully loaded. It ensures that the challenges stored in local storage are displayed to the user immediately upon accessing the page.
Automatically invoked when the HTML document's load event is triggered.

Function: displayChallenges():
Retrieves challenge data from local storage and dynamically displays each challenge in the #order-summary container. It also calculates and displays the total price of all challenges.

Steps:
Fetches the array of challenges from local storage. If no array is found, an empty array is used instead.
Iterates over the array of challenges.
For each challenge, creates a new div element with the class challenge and populates it with the challenge's details (name, distance, description, price).
Appends each challenge div to the #order-summary container.
Calculates the total price of all challenges and displays it in the #total element.
This function is automatically called when the page loads.

Function: clearChallenges():
Clears all challenge data from local storage and the display, effectively resetting the order summary. It also resets the total price display to zero and alerts the user that the challenges have been deleted.

Steps:
Removes the "challenges" item from local storage.
Clears the inner HTML of the #order-summary container.
Sets the inner HTML of the #total element to indicate a zero total.
Displays an alert to inform the user that the challenges have been deleted.
