### General
1. All slices of the state tree should be Immutable.
2. Pure functions.
3. 

### Components
1. Keep components small.
2. Write functional _(pure, dumb, presentational, or whatever else they may be called now)_ components whenever possible. They are reusable and keep things simple. Example:
    ```javascript
    const MyComponent = props => (
        <div className={props.className}/>
    )
    ```
3. Write stateless components. Internal state for UI details that the parent does not need to know about are okay. Otherwise, you don't need it.
4. Use PropTypes. Always, always, always.
5. Don't use render callbacks.

### Performance
1. Do not bind functions (like event handlers passed ia props) in `render()`. With a new function created each time, it will force your component to render because it thinks the props have, even if no props have really changed. Instead, bind all your handlers in the constructor or declaire your handlers using arrow functions.
2. Use `shouldComponentUpdate`.
3. 

### Tests
1. Use shallow rendering.
2. 




### Where did you get this shit?
https://camjackson.net/post/9-things-every-reactjs-beginner-should-know
https://engineering.siftscience.com/best-practices-for-building-large-react-applications/
