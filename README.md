# Meetup Events app

This Meet app is a serverless progressive web app built with Create-React-App and Amazon Web Services that allows users to find events in a city near them.

## Serverless Functions:
This app will use serverless functions by authorizing the client-side app to connect to Google's Calendar API and receive event data. Any time the user triggers an event that requires connecting to the API, the app will utilize serverless functions facilitated by AWS Lambda to receive the requested data. Such an event could be as simple as filtering the list of events.

## Features and Scenarios

User stories for each feature and each test case scenario described using Gherkin's "given-when-then" syntax.

### Feature 1: Filter Events By City
  - **User Story**: As a user, I should be able to filter events by city so I can see a list of events in that city. 
  - **Scenario 1**: When user hasn’t searched for a city, show upcoming events from all cities.
    - GIVEN the user hasn’t searched for a city, WHEN they open the app, THEN the user should see a list of upcoming events from all cities.
  - **Scenario 2**: User should see a list of suggestions when they search for a city.
    - GIVEN the main page is open, WHEN the user starts typing in the textbox, THEN the user should see a list of suggestions (cities) when they search for a city.
  - **Scenario 3**: User can select a city from the suggested list.
    - GIVEN the user typed a city in the textbox and the suggested cities are showing, WHEN the user selects a city, THEN the user should see a list of upcoming events for that city.

### Feature 2: Show/Hide Event Details
  - **User Story**: As a user, I should be able to show or hide the details of any chosen event so that I can learn more about them.
  - **Scenario 1**: An event element is collapsed by default.
    - GIVEN the user hasn't clicked any event details, WHEN the default or city event list has loaded, THEN all the events' details should be collapsed.
  - **Scenario 2**: User can expand an event to see details.
    - GIVEN the user hasn't opened any event details, WHEN they want to learn more about an event, THEN the chosen event should expand to reveal more details.
  - **Scenario 3**: User can collapse an event to hide details.
    - GIVEN the user has expanded an event's details, WHEN they choose to hide the event details, THEN the expanded information should collapse. 

### Feature 3: Specify Number of Events
  - **User Story**: As a user, I should be able to choose how many events are shown so I can limit or expand my options.
  - **Scenario 1**: When user hasn’t specified a number, 32 events are shown by default.
    - GIVEN the user hasn't specified how many events to show, WHEN the default or city-specific events list is shown, THEN at most 32 events should be listed. 
  - **Scenario 2**: User can change the number of events displayed.
    - GIVEN the user hasn't specified how many events to show, WHEN they input how many events they want to see, THEN the user will see that many events at a maximum.

### Feature 4: Use the App When Offline
  - **User Story**: As a user, I should be able to use the meet app even when I don't have internet access so I can use it whenever I want.
  - **Scenario 1**: Show cached data when there’s no internet connection.
    - GIVEN the user doesn't have internet access, WHEN the user wants to use the app to see events, THEN they should be able to see the events viewed in-app when last online. 
  - **Scenario 2**: Show error when user changes search settings (city, number of events).
    -  GIVEN the user doesn't have internet access, WHEN the user specifies a city or number of events, THEN they should be shown an error.

### Feature 5: Add an App Shortcut to the Home Screen
  - **User Story**: As a user, I should be able to save a shortcut to the meet app on my homescreen so I can see it and more easily open it again.
  - **Scenario 1**: User can install the meet app as a shortcut on their device home screen.
    - GIVEN the user has downloaded the app, WHEN they want to open/use the app, THEN they should be able to pin a shortcut to their homescreen for easy access. 

### Feature 6: Display Charts Visualizing Event Details
  - **User Story**: As a user, I should be able to see charts about the events so I can more easily tell what's popular and in which city.
  - **Scenario 1**: Show a chart with the number of upcoming events in each city
    - GIVEN the main page is open and a city hasn't been selected, WHEN the user is viewing events from all cities, THEN they should see a scatterplot chart of how many events will take place in each city.

## Link to app
You can view the app via GitHub pages [here](https://jeffellingham.github.io/meet-app/).

## Contact and Credit
Thank you to CareerFoundry for their Full-Stack Web Development bootcamp which I created this project during to learn Test-Driven and Behavior-Driven Development processes using Jest and Cucumber.

Find my portfolio and more about me [here](https://jeffellingham.github.io).
