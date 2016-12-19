# Refactoring existing applications

Time to see how well you documented, and modularized your code.

Stay in your team, but fork another team's movie history application on Github and refactor it based on your understanding of the following requirements.

## Requirements

1. Stars must be between 1-10 instead of 1-5.
2. When the customer clicks the delete button, don't remove the entry from the database, but rather make it inactive so that it no longer shows up in the search results.
3. Instead of the filter for 5-start movies, put in a slider control with a min value of 0, and a max value of 10.
4. If the slider value is at 0, view all movies that match the search criteria.
5. If the slider value is 1-10 only show watched movies with the corresponding star rating.