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

Paste the README template for part 2 of this assignment here at the top. This will show a history of your development process, which users stories you completed and how your app looked and functioned at each step.

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