# "Mutations in Relay" by [Laney Kuenzel](https://twitter.com/laneykuenzel)

This talk introduced fetching & organizing data with [Relay](http://facebook.github.io/react/blog/2015/02/20/introducing-relay-and-graphql.html#what-is-relay).

Here a *mutation* means a user action that causes data to change.

([slides + notes](https://speakerdeck.com/laneyk/mutations-in-relay))

* Previous situation
  * Data hierarchy, where parents must know the data that its children need
  * Server must fetch all data that *might* be needed on the client.
  * Each feature had its own custom JS, endpoint, and data format.
* Relay: data fetching & rendering together
* GraphQL: data query language
  * JS object of properties and their hierarchy structure:
        ```javascript
        {
          id,
          name,
          profile_picture: {
            uri,
            width,
            height
          }
        }
        ```
* Relay composes queries, performs a fetch, and returns data to the renderer.
* Mutations
  * Provide it with GraphQL with the type of mutation, any inputs, and a query for the desired after-update data
  * Fills out the query's properties and returns the current values
  * Auto-creates a query that intersects the properties of what the mutation can change + what has been stored
* "Optimistic Updates"
  * Provides the view with a mimic payload so it can update immediately instead of waiting on server.
  * Handles server errors -- just removes the mimic from the OU queue
  * Handles race conditions (e.g. liking and unliking a post multiple times in rapid succession)
* New/soon: pubsub with the server, in case of outside changes
* Benefits
  * Keeps the logic for data fetching and rendering inside the view
  * Frees up time for actual UI work
  * Eases scaling up of large apps & teams
