17-Movie App

This code creates a web page that displays movies fetched from an API. The code defines three constants: API_URL, IMG_PATH, and SEARCH_API which contain URLs for fetching movie data and images. It then creates three variables: main, form, and search to reference elements in the HTML of the web page.

The getMovies(url) function fetches data from the API by making an HTTP request using fetch() method, waits for the response using await, parses the response into JSON format with .json(), and then calls another function showMovies(movies) to render the resulting movie data on the web page in a visually appealing way.

The showMovies(movies) function first clears the HTML content of the main element and then loops through each movie object in the movies array returned by the API. For each movie, it creates a new div element dynamically using Javascript and populates it with information such as the title, vote average, overview, and poster image. The background color of the rating is set based on the value of the vote_average using getClassByRate(vote_average) function.

The getClassByRate(vote) function returns a class name for styling purposes based on the value of the parameter vote. If vote >= 8 the function returns "green", if vote >= 5 the function returns "orange", and if vote is less than 5, it returns "red".

Finally, the code adds an event listener to the form element so that when a user submits the form (by searching for a movie), it prevents the default behavior of reloading the page, retrieves movie data using the getMovies(SEARCH_API + searchTerm) function, and updates the main element with the search results.
