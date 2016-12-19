## Setup

### Create a new branch

`git checkout -b version10`

## Requirements

Refactor Music History, or choose to rebuild from scratch (whichever you deem most effecient), using Angular.

1. You will need two partials
    1. song-list.html
    1. song-details.html
1. You will need a controller for each partial
1. Use `ngRoute` to specify which URL route loads each partial
1. If you find that you are making similar requests to get your data in each of the controllers, make a factory for each controller to use.

### Song List View

Remove the filter form that you've used on previous versions, and just provide a text box above the song list that will use whatever the user types in to filter the list on song title, album or artist name.

```
 -----------------------------------------------------------------------------
|                    _________________________________________                |
|    Filter songs:  |_________________________________________|               |
|                                                                             |
|                                                                             |
|                                                                             |
|                                                                             |
|                                                                             |
|         My Favorite Song                                                    |
|         The Grey Album (1998)                                               |
|                                                                             |
|                                                                             |
|                                                                             |
|         All Those Things                                                    |
|         Albatross (1976)                                                    |
|                                                                             |
|                                                                             |
|                                                                             |
|         Man on the Corner                                                   |
|         Abacab (1981)                                                       |
|                                                                             |
|                                                                             |
|                                                                             |
|         O.P.P                                                               |
|         Naughty by Nature (1991)                                            |
|                                                                             |
|                                                                             |
|                                                                             |
|                                                                             |
 -----------------------------------------------------------------------------



```

### Song Detail View

Display all the details of the song however you like.
