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

Using the built-in callout feature for Flow. Lets try to pass some Account address data to the [US Census Bureau Geocoder](https://geocoding.geo.census.gov/geocoder/Geocoding_Services_API.html) and save the reponse somewhere on Account record. [View the feature request here](https://github.com/vaugood/sfdx-fun/issues/1).
1) Invoke Screen Flow from sObject (Account, for instance) from a button on the record page.
2) Pass address data from the record to the geocoder Screen Flow.
3) Parse the output and store the geocoding results on the Salesforce record.

Solution:
1) Configure remote site settings to allow responses from the geocoding service.
2) Create a custom field for each desired reponse field on your sObject(s).
3) Create a flow with a Callout to make the request, handle the response, and store the data.