# Client Side Routing w/ React Router v.5

Topics:

- React Router
- Using Link and NavLink to navigate to specific routes
- Passing Route Parameters
- Passing props to components rendered by the Router

## Instructions

- [0] **Fork** this repository, then clone your fork.
- [0] **NOTE** You have 2 servers that you will be running here so read these instructions carefully.
- [0] **In the root of this directory**: Run `npm install` to download dependencies.
- [0] Run the server using `npm start` or `node server.js`. (Don't worry too much about this process, you'll get used to doing this and it will be explained more in the future).
- [0] In a separate terminal cd into the `client` folder and run `npm install` to download dependencies.
- [0] Still inside the `client` folder run `npm start` to run the client application.

- [0] Once your application is up and running on the client, you should see a browser window that looks like this at `localhost:3000` (although the port number will be different if 3000 is being used).

  ![Movies Home](https://ibin.co/3xhmmHVl9BKF.png)

### Part 1

- [0] Wrap your app with the router.
- [0] Inside your App file add two routes.
  - [0] one route for `/` that loads the `MovieList` component. **This component will need the movies injected into it via props**.
  - [0] one route that will take an `id` parameter after`/movies/` (ex: `/movies/2`, `/movies/3` where the id is dynamic). This route should load the `Movie` component.

### Part 2

- [0] Make it so that the card in `MovieList` is a link, this should direct the user to the `/movies/{id of movie here}` URL, where `:id` is the id of the individual movie.
- [0] When a user clicks on a movie card they should be taken to `/movies/{id of movie here}` to see the details for the selected movie.
- [0] You will need to modify line 13 of `Movie.js` in order to accept the correct id for the movie selected.
- [0] Add functionality so the `Home` button on the `SavedList` component navigates back to home.
- [0] You should now be able to navigate back and forth between the individual movies and the home screen.

## Stretch Goals

If you have completed Parts 1 & 2 feel free to move on to these stretch goals.

### Refactor so that our code is DRY

- [ ] You may notice that we are using essentially the same exact JSX code in the `Movie` component and the `MovieDetails` component in `MovieList.js` create a new component in `MovieCard.js` that returns this JSX code. Then remove the old code from `Movie` and `MovieDetails` and instead return the new `MovieCard` component.

### Add `Save Movie` functionality

- [ ] You will notice there is a 'Saved Movies' component that we are not currently using. In this step you will add the functionality to save a movie. You will need to pass the `addToSavedList` function to the `Movie` component. Once you have done that you will need to add a click handler to the save button. You will need to uncomment lines 24-27 in `Movie.js` to complete this.

### Turn your Saved Movie list into `Link`s

- [ ] Your list of saved movies should be links to the movie itself. Study and understand what the `saveMovie` function is doing.

### Turn your Saved Movie `Link`s into `NavLink`s

- [ ] Navlink
