# Local Weather Application

Use the [OpenWeatherMap](http://openweathermap.org/API) API to build an application that meets the following criteria.

**given** a user wants to view weather information<br/>
**when** the user visits your application<br/>
**then** they should be presented with an authentication mechanism that allows login via Google, Twitter, Facebook, or Github. Pick one, at a minimum, but if you want to add all, that would be impressive.

**given** a user wants to view weather information<br/>
**when** the user visits your initial view<br/>
**then** there should be an input field to accept a zip code value

**given** a user wants to view weather information<br/>
**when** the user visits your initial view<br/>
**then** there should be a submit button next to the zip code field

**given** a user has entered in some text into the zip code field<br/>
**when** the user presses the enter key<br/>
**or** the user clicks the submit button<br/>
**then** the value should be validated as a zip code (5 digit number)

**given** the user has entered a valid zip code<br/>
**when** the user presses the enter key<br/>
**or** clicks the submit button<br/>
**then** the current weather for the provided zip code should be displayed, which includes

1. Temperature
1. Conditions
1. Air pressure
1. Wind speed
1. An affordance to view the forecast for the current day, the next three days, or the next 7 days

**given** the user is viewing the current forecast<br/>
**when** the user clicks on the link to view the 3 day forecast<br/>
**then** the current data (see above), and the data for the next 3 days should be displayed

**given** the user is viewing the current forecast<br/>
**when** the user clicks on the link to view the 7 day forecast<br/>
**then** the current data (see above), and the data for the next 7 days should be displayed

**given** a user wants to view weather information<br/>
**when** the user visits your initial view<br/>
**then** there should be social sharing buttons for Facebook and Twitter

**given** a user wants to share a day's forecast<br/>
**when** the user performs a gesture on one of the social sharing elements<br/>
**then** the user should be authenticated against that service's OAuth API and prompted with a status update affordance with the day's forecast pre-populated

**given** a user wants to save weather information<br/>
**when** the user visits your initial view<br/>
**then** there should be an affordance (e.g. a star or link) that allows them to save a day's forecast to their profile

**given** a user wants to view their saved forecasts<br/>
**when** the user performs a gesture on an element that clearly states its purpose is to view saved data<br/>
**then** the user should be shown a list of all of their saved forecasts

