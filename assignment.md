### Setting up

1. [Fork and clone this repo].  Take a moment to look through each of the models and familiarize yourself with the associations that have been added.

2. Run `rails db:setup` and `psql chinook_development < chinook.sql` to set up your database and import some data.
3. Start the rails console.

### Questions
Make use of the methods added to your models by the associations in order to answer the following questions. [The Rails guide on associations](http://guides.rubyonrails.org/association_basics.html#detailed-association-reference) can remind you what those methods are.

1. Find the album titled "Vinicius De Moraes", and then use an association-provided method to find all its tracks.
2. Find the artist called "Philip Glass Ensemble", and then use an association-provided method to find all their albums.
3. Find the "Brazilian Music" playlist and then use an association-provided method to find all its tracks.
4. Find the "Jazz" genre and then use an association-provided method to find all its tracks.
5. Find the track "My Time After Awhile" and then use an association-provided method to find its genre.
6. Use an association-provided method to find the media type of that same track.
7. Use an association-provided method to find the album that track appears on.

## Part 4
1. Add a `through` association to Chinook that will allow you to make the following query:
  ```ruby
  Artist.last.tracks
  ```
  Test it out in the Rails console to make sure it worked.
2. Add a `through` association to Chinook that will allow you to make the following query:
  ```ruby
  Playlist.last.genres
  ```
  Test it out in the Rails console to make sure it worked.
3. Add a `through` association to Chinook that will allow you to make the following query:
  ```ruby
  Album.last.playlists
  ```
  Test it out in the Rails console to make sure it worked.
4. Add a `through` association to Chinook that will allow you to make the following query:
  ```ruby
  Playlist.last.media_types
  ```
  Test it out in the Rails console to make sure it worked.
5. Add a `through` association to Chinook that will allow you to make the following query:
  ```ruby
  Artist.last.media_types
  ```
  Test it out in the Rails console to make sure it worked.
6. Add a `through` association to Chinook that will allow you to make the following query:
  ```ruby
  MediaType.last.genres  
  ```
  Test it out in the Rails console to make sure it worked.
