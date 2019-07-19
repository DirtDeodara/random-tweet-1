# Random Tweet

Create an API that deals with tweets. A tweet schema looks like

```js
const tweetSchema = new mongoose.Schema({
  handle: {
    type: String,
    required: true
  },
  text: {
    type: String,
    required: true
  }
});
```

## Routes

* `POST /api/v1/tweets` to create a new tweet
* `GET /api/v1/tweets` to get all tweets
* `GET /api/v1/tweets/:id` to get a tweet by ID
* `PATCH /api/v1/tweets/:id` to update a tweets text **ONLY**
* `DELETE /api/v1/tweets/:id` to delete a tweet

## Randomness

Update your `POST` route so it can take a query string.

```js
.post('/', (req, res, next) => {
  // /api/v1/tweets?random=true
  // { random: 'true' }
  const { random = 'false' } = req.query
});

If the random query string is set, get a random quote from an API (e.g. the futurama API).
Create a random tweet based on that quote.

## Resources

* [Ron Swanson](https://ron-swanson-quotes.herokuapp.com/v2/quotes)
* [Futurama](http://futuramaapi.herokuapp.com/)
* [The Simpsons](https://thesimpsonsquoteapi.glitch.me/)
