# Flix

Flix is an app that allows users to browse movies from the [The Movie Database API](http://docs.themoviedb.apiary.io/#).

📝 `let url = URL(string: "https://api.themoviedb.org/3/movie/now_playing?api_key=a07e22bc18f5cb106bfe4cc1f83ad8ed")!
let request = URLRequest(url: url, cachePolicy: .reloadIgnoringLocalCacheData, timeoutInterval: 10)
let session = URLSession(configuration: .default, delegate: nil, delegateQueue: OperationQueue.main)
let task = session.dataTask(with: request) { (data, response, error) in
   // This will run when the network request returns
   if let error = error {
      print(error.localizedDescription)
   } else if let data = data {
      let dataDictionary = try! JSONSerialization.jsonObject(with: data, options: []) as! [String: Any]

      // TODO: Get the array of movies
      // TODO: Store the movies in a property to use elsewhere
      // TODO: Reload your table view data

   }
}
task.resume()` 

## Flix Part 2

### User Stories

#### REQUIRED (10pts)
- [x] (5pts) User can tap a cell to see more details about a particular movie.
- [x] (5pts) User can tap a tab bar button to view a grid layout of Movie Posters using a CollectionView.

#### BONUS
- [ ] (2pts) User can tap a poster in the collection view to see a detail screen of that movie.
- [ ] (2pts) In the detail view, when the user taps the poster, a new screen is presented modally where they can view the trailer.

### App Walkthrough GIF

<img src="http://g.recordit.co/qNikShiibZ.gif" width=250><br>

### Notes
Describe any challenges encountered while building the app.

I was working through the collection view and didn't realize that when connected the image view it was of the UIView type and not the UIImageView type. This took me a little bit of time to realize, but it was a good learning experience and something I will now watch out for.

---

## Flix Part 1

### User Stories

#### REQUIRED (10pts)
- [x] (2pts) User sees an app icon on the home screen and a styled launch screen.
- [x] (5pts) User can view and scroll through a list of movies now playing in theaters.
- [x] (3pts) User can view the movie poster image for each movie.

#### BONUS
- [ ] (2pt) User can view the app on various device sizes and orientations.
- [ ] (1pt) Run your app on a real device.

### App Walkthrough GIF

<img src="http://g.recordit.co/XEgdkoRT0e.gif" width=250><br>

### Notes
Describe any challenges encountered while building the app.

I realized I accidently made two TableViews on top of each other and was assigning different labels to each without knowing, so I had to go back and redo a lot to get a clean storyboard and code.
