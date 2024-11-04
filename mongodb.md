# MongoDB Exercise
## 1. Create a Database called movies.
```sh
test> use movies;
switched to db movies
```
## 2. Create a collection called moviedetails.
```sh
db.createCollection("moviedetails")
```
## 3. Create above 5 movie documents into a moviedetails collection.
```sh
movies> db.moviedtails.insertMany([
    { title: "Vikram", genre: "Drama", director: "Lokesh Kanakaraj", release_year: 2022 },
    { title: "Vettaiyan", genre: "Action", director: "Ganavel", release_year: 2024 },
    { title: "Kanguva", genre: "Fantasy", director: "Siva", release_year: 2025 },
    { title: "Leo", genre: "Action", director: "Lokesh Kanakaraj", release_year: 2023 },
    { title: "Vidamuyatchi", genre: "Thriller", director: "Magizh Thirumeni", release_year: 2025 }
])
```
## 4. List all documents created.
```sh
db.moviedetails.find()
```
## 5. List Lokesh Kanakaraj’s movies.
```sh
db.moviedetails.find({ director: "Lokesh Kanakaraj" })
```
## 6. List Lokesh Kanakaraj’s movies released in 2023.
```sh
db.moviedetails.find({ "Director": "Lokesh Kanakaraj", "Release Year": 2023 })
```
## 7. Delete the movie which you don’t like.
```sh
db.moviedetails.deleteOne({ "Movie-Title": "Vettaiyan" })
```
## 8. Add the movie which is your favourite.
```sh
Replace "Your_Movie_Title", "Your_Genre", "Your_Director", and Your_Year with your favorite movie details:


db.moviedetails.insertOne({
  title: "Your_Movie_Title",
  genre: "Your_Genre",
  director: "Your_Director",
  release_year: Your_Year}
)
```
## 9. List movie Directed by Magizh Thirumeni in 2025.
```sh
db.moviedetails.find({ director: "Magizh Thirumeni", release_year: 2025 })
```
## 10. List out the Director’s Name in your document.
```sh
db.moviedetails.distinct("director")
```





