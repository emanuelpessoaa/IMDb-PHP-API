# IMDb PHP API

## How To Use

### Create an instance

    $imdb = new IMDb;
    $imdb = new IMDb(true);	// this will anonymize your requests to prevent your IP address getting banned


### Search for a movie by title

    // Returns an array containing objects of matching titles
    $movies = $imdb->find_by_title("The Godfather"); 
    
    // $movies[0]->title => "The Godfather"
    // $movies[0]->year => "1972"
    // $movies[0]->tconst => "tt0068646"
    // ... 
    // $movies[1]->title => "The Godfather: Part II"
    // ...

### Get a movie by its imdb_id

    // Returns an object containing the movie's data
    $movie = $imdb->find_by_id("tt0068646");

    // $movie->title => "The Godfather"
    // $movie->rating => "8.1"
    // $movie->year => "1972"