# Playing with Screen Flow

This project explores the various ways a developer can utilize screen flows.

## Invoke & Pass

The first challenge is to see if it is possible to:
1) Invoke a screen flow from a non-lightning object (Task, for instance) from a button on the record page.
2) Pass the sObject Id to the flow via the button.

Solution:
1) Create a Screen Flow with the [special recordId variable](https://youtu.be/n3S1zHL_AnQ?t=78).
2) Wire it to an Action Button.
3) Add the action button to the layout (assigned via Salesforce Mobile and Lightning Experience Actions).