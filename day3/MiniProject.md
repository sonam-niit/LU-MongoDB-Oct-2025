# Mini Project: Movie Data Analysis

**Objective**

- Having a set of data for Movie Database 
- Analyze data for taking some desicions
- understand how to write basic to complex Queries

## Let's Setup a Database

```bash
# Create Database
use moviedb
# Create Collection
db.createCollection('movies')
```

## Data Insertion using insertMany

```bash
db.movies.insertMany([
  {
    _id: 1,
    title: "Midnight Run",
    year: 2015,
    genres: ["Drama", "Thriller"],
    director: { name: "Asha Rao", born: 1976 },
    cast: ["Ravi Kumar", "Maya Sen", "Arjun Roy"],
    runtimeMin: 128,
    language: "Hindi",
    country: "India",
    ratings: [
      { source: "IMDb", score: 7.4 },
      { source: "Critic", score: 8.0 }
    ],
    boxOfficeUSD: 4200000,
    budgetUSD: 1500000,
    released: ISODate("2015-08-21"),
    awards: { wins: 2, nominations: 5 },
    tags: ["road", "revenge"]
  },
  {
    _id: 2,
    title: "Celestial",
    year: 2018,
    genres: ["Sci-Fi", "Adventure"],
    director: { name: "Marcus Li", born: 1980 },
    cast: ["Evelyn Park", "Tomás Silva"],
    runtimeMin: 140,
    language: "English",
    country: "USA",
    ratings: [
      { source: "IMDb", score: 8.2 },
      { source: "RottenTomatoes", score: 88 }
    ],
    boxOfficeUSD: 98000000,
    budgetUSD: 40000000,
    released: ISODate("2018-11-02"),
    awards: { wins: 6, nominations: 11 },
    tags: ["space", "epic"]
  },
  {
    _id: 3,
    title: "The Quiet Orchard",
    year: 2012,
    genres: ["Drama"],
    director: { name: "Asha Rao", born: 1976 },
    cast: ["Neel Patel", "Sana Qureshi"],
    runtimeMin: 95,
    language: "Hindi",
    country: "India",
    ratings: [{ source: "IMDb", score: 6.8 }],
    boxOfficeUSD: 800000,
    budgetUSD: 300000,
    released: ISODate("2012-03-15"),
    awards: { wins: 1, nominations: 2 },
    tags: ["art", "family"]
  },
  {
    _id: 4,
    title: "City of Mirrors",
    year: 2020,
    genres: ["Crime", "Mystery"],
    director: { name: "Liam O'Connor", born: 1972 },
    cast: ["Eva Wong", "Ravi Kumar"],
    runtimeMin: 110,
    language: "English",
    country: "UK",
    ratings: [
      { source: "IMDb", score: 7.9 },
      { source: "Critic", score: 7.5 }
    ],
    boxOfficeUSD: 21000000,
    budgetUSD: 12000000,
    released: ISODate("2020-05-10"),
    awards: { wins: 3, nominations: 8 },
    tags: ["noir", "detective"]
  },
  {
    _id: 5,
    title: "Sunny Side Up",
    year: 2021,
    genres: ["Comedy", "Romance"],
    director: { name: "Priya Menon", born: 1988 },
    cast: ["Maya Sen", "Adil Khan"],
    runtimeMin: 102,
    language: "Hindi",
    country: "India",
    ratings: [
      { source: "IMDb", score: 7.1 },
      { source: "Audience", score: 78 }
    ],
    boxOfficeUSD: 5200000,
    budgetUSD: 1000000,
    released: ISODate("2021-02-12"),
    awards: { wins: 0, nominations: 3 },
    tags: ["romcom"]
  },
  {
    _id: 6,
    title: "Neon Samurai",
    year: 2019,
    genres: ["Action", "Sci-Fi"],
    director: { name: "Hiro Tanaka", born: 1982 },
    cast: ["Takeshi Ito", "Eva Wong", "Tomás Silva"],
    runtimeMin: 132,
    language: "Japanese",
    country: "Japan",
    ratings: [
      { source: "IMDb", score: 8.5 },
      { source: "Critic", score: 9.0 }
    ],
    boxOfficeUSD: 65000000,
    budgetUSD: 30000000,
    released: ISODate("2019-09-06"),
    awards: { wins: 10, nominations: 14 },
    tags: ["cyberpunk", "martial"]
  },
  {
    _id: 7,
    title: "Hidden Currents",
    year: 2010,
    genres: ["Documentary"],
    director: { name: "Lina Gomez", born: 1969 },
    cast: ["Narrator: Priya Menon"],
    runtimeMin: 78,
    language: "Spanish",
    country: "Mexico",
    ratings: [{ source: "IMDb", score: 7.0 }],
    boxOfficeUSD: 120000,
    budgetUSD: 50000,
    released: ISODate("2010-07-28"),
    awards: { wins: 1, nominations: 1 },
    tags: ["environment"]
  },
  {
    _id: 8,
    title: "Echoes of Tomorrow",
    year: 2022,
    genres: ["Sci-Fi", "Drama"],
    director: { name: "Marcus Li", born: 1980 },
    cast: ["Evelyn Park", "Neel Patel"],
    runtimeMin: 150,
    language: "English",
    country: "USA",
    ratings: [
      { source: "IMDb", score: 8.7 },
      { source: "RottenTomatoes", score: 92 }
    ],
    boxOfficeUSD: 160000000,
    budgetUSD: 80000000,
    released: ISODate("2022-12-01"),
    awards: { wins: 12, nominations: 20 },
    tags: ["time", "philosophy"]
  },
  {
    _id: 9,
    title: "Small Fires",
    year: 2016,
    genres: ["Thriller", "Crime"],
    director: { name: "Priya Menon", born: 1988 },
    cast: ["Arjun Roy", "Adil Khan"],
    runtimeMin: 105,
    language: "Hindi",
    country: "India",
    ratings: [{ source: "IMDb", score: 6.9 }],
    boxOfficeUSD: 2300000,
    budgetUSD: 900000,
    released: ISODate("2016-10-11"),
    awards: { wins: 0, nominations: 1 },
    tags: ["suspense"]
  },
  {
    _id: 10,
    title: "Laugh Lines",
    year: 2013,
    genres: ["Comedy"],
    director: { name: "Samir Gupta", born: 1975 },
    cast: ["Maya Sen", "Tomás Silva"],
    runtimeMin: 98,
    language: "Hindi",
    country: "India",
    ratings: [{ source: "IMDb", score: 6.2 }],
    boxOfficeUSD: 1400000,
    budgetUSD: 600000,
    released: ISODate("2013-04-05"),
    awards: { wins: 0, nominations: 0 },
    tags: ["satire"]
  }
])
```