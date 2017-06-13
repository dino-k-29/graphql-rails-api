# GraphQL Rails API

This is a simple demonstration of integrating GraphQL into a Rails API, an alternative to traditional REST endpoints.

---

Live demo: `https://secret-garden-22357.herokuapp.com/movies?query={movie(id:1){title,year,actors{name}}}`

The above code requests the Movie with an id of 1, it's title, year and actors, along with each actor's name:

```
"query={
  movie(id: 1) {
    title,
    year,
    actors {
      name
    }
  }
}"
```

---

This project was created following this tutorial: [https://www.sitepoint.com/building-apis-ruby-rails-graphql/](https://www.sitepoint.com/building-apis-ruby-rails-graphql/)

Changes from the tutorial:

* Instead of the method presented in the tutorial `create_join_table` was used to create the association
* `get 'movies/', to: 'movies#query'` was added to `routes.rb`
* Erroneous spaces removed from copied code e.g. `movie.actors << actor`
