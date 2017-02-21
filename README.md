# Jive-tiles

This tile is a modification of the `ask-a-question` tile available here: [https://github.com/mdsol/jive](https://github.com/mdsol/jive).

Our users wanted to ability to see what ideas had already been submitted before submitting a new one. This tile provides a search field that displays a list of existing feature requests matching a keyword, including the status (Open for Voting, etc.), author, and data submitted. (This can be modified. See below.) A button at the bottom of the list of results opens a new feature request form. The number of search results to show and which spaces to search are configurable when installing the tile.

## Prerequisites
- Jive SDK
- Command-line tool like Bash

## To use

Open Bash at the root of the `search-feature-requests` folder.

```npm update```

```jive-sdk build add-on --apphosting="jive"```

(Alternatively, to customize the name of the add on, add the `--name="YourName"` flag.)

Go to `https://<your jive instance>/addon-services!input.jspa?filterID=allServices`.

Click `Upload Package`.

Click `Install`.

On a Jive page you want to place the tile, click the cog > `Edit page`.

Click `Add a new tile`.

Select the `Search Feature Requests` tile.

Select your configuration settings.

Save the Jive page.

##To customize

To customize the language in the search field, on the button, etc. (e.g., from `feature request` to `idea`), go to `\jive-tiles\search-feature-requests\tiles\search-feature-requests\public\view.html`.

To change what information is displayed with the search results (author name, voting status, etc.), go to approximately lines 94 and 148 of `\jive-tiles\search-feature-requests\tiles\search-feature-requests\public\javascripts\view.js`.
