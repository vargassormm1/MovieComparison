# Movie Fight Documentation

## Overview

This documentation provides an overview of the Movie Fight application, a web-based tool that allows users to search for movies and compare their statistics side-by-side. The application leverages the OMDB API for movie data and utilizes custom JavaScript to provide an interactive and responsive user experience.

## Files and Structure

The project consists of the following files and directories:

- `autocomplete.js`: Contains the logic for the autocomplete functionality used in the search fields.
- `index.html`: The HTML structure of the application.
- `index.js`: Contains the application's main logic, including API requests and comparison logic.
- `style.css`: The CSS styles for the application.
- `utils.js`: Includes utility functions, such as a debounce function to limit API request frequency.
- `sounds/`: (If applicable) This directory would contain sound files, not mentioned but implied by project structure.

## Key Features

- **Autocomplete Search**: As users type in the search fields, suggestions appear based on the input, allowing for an easy selection of movies.
- **Side-by-Side Comparison**: Once two movies are selected, their key statistics are displayed next to each other for easy comparison.
- **Dynamic Content Loading**: Movie data, including images, ratings, and financial information, is fetched in real-time from the OMDB API.
- **Responsive Design**: Utilizes Bulma CSS for a responsive layout that adjusts to different screen sizes and devices.

## How to Use

1. **Start Searching**: Type a movie name into either of the search fields. As you type, a dropdown will appear with movie suggestions.
2. **Select Movies**: Click on a movie in the dropdown to select it for comparison. Repeat for the second search field.
3. **Compare**: Once both movies are selected, their statistics are displayed side-by-side. Compare their ratings, box office earnings, and other key metrics.
4. **Restart**: To compare two different movies, simply start a new search in either search field.

## Development Details

### Autocomplete Widget

The `createAutoComplete` function in `autocomplete.js` provides a reusable widget that can be applied to multiple search fields. It requires configuration options like `renderOption`, `onOptionSelect`, `inputValue`, and `fetchData` to tailor its functionality.

### API Requests

`index.js` includes the `fetchData` function that makes API requests to OMDB based on the user's search term, using Axios for HTTP requests.

### Debounce Utility

To minimize the number of API requests while typing, `utils.js` contains a `debounce` function that waits until the user stops typing before sending a request.

### Movie Selection and Comparison

Once a movie is selected from the suggestions, `index.js` fetches detailed information about the movie and displays it. When both movies are selected, the `runComparison` function compares their statistics and highlights the superior metrics.

## Requirements

- A modern web browser with JavaScript enabled.
- An active internet connection to fetch movie data from the OMDB API.

## Conclusion

Movie Fight is an interactive web application that utilizes modern JavaScript, CSS frameworks, and external APIs to create a dynamic and engaging user experience. It demonstrates key principles in web development, such as asynchronous programming, API integration, and responsive design.
