# Playing with Screen Flow

Exploring the various ways a developer can utilize screen flows.

## Invoke & Pass

The first challenge is to see if it is possible to:
1) Invoke a screen flow from a non-lightning object (Task, for instance) from a button on the record page.
2) Pass the sObject Id to the flow via the button.

Solution:
1) Create a Screen Flow with the [special recordId variable](https://youtu.be/n3S1zHL_AnQ?t=78).
2) Wire it to an Action Button.
3) Add the action button to the layout (assigned via Salesforce Mobile and Lightning Experience Actions).

## Calling an external API from a Screen Flow

Using the built-in callout feature for Flow. Lets try to pass some Account address data to the US Census Bureau and save the reponse somewhere on Account record. [View the feature request here](https://github.com/vaugood/sfdx-fun/issues/1).