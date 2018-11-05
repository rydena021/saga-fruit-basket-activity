# React Redux with Sagas

Let's add Sagas to our React Redux fruit basket.

## Setup

- `npm install`
- `npm run server`
- `npm run client`

## Sagas

Sagas listen, like Reducers, for actions. Sagas will intercept actions **BEFORE** the reducer, and the action will not make it to the reducer. Sagas can do many things. Common things are dispatching other actions, and triggering HTTP calls. Usually, the end of the saga dispatches a new action that sends info to the reducer to be saved in the store.

### Why Sagas?

Reducers **CAN NOT** make async requests. All changes withing a reducer happen immediately. This prevents us from being able to make API requests from our reducers.

As our application grows, we'll be making duplicate API requests in various components. We could move all of these to our `App.js` and pass them via props but that will quickly get difficult to manage. 
