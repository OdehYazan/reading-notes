# State and Props

## Component Lifecycle Events

**The methods that you are able to use on these are called lifecycle events,These methods can be called during the lifecycle of a component, and they allow you to update the UI and application states.**

**We have three phases of the component lifecycle.<br>1. Mounting(which is the first thing happened in the lifecycle of React).<br>2. Updating<br>3. Unmounting.**

**Thing in lifecycle happened in order:<br>1. Constructor.<br>2. Render.<br>3. React Updates.<br>4. ComponentDidMount.(used  load anything using a network request or initialize the DOM and it is good to set any subscriptions)<br>5. ComponentWillUnmount**

**`Cnstructor()`<br>The constructor for a React component is called before it is mounted.If the component is a subclass you should call super(props), or the props will be undefined and it can be used to assign state using `this.state`(avoid using it can lead to side effects).<br> EX:**

![Cnstructor](../img/301.1.jpg)

**`ComponentDidMount()`<br>This method is invoked immediately after a component is mounted, we use it to load anything using a network request or initialize the DOM, `setState()` can be called here, but it should be used sparingly, because it will cause a rerender, which can lead to performance issues.<br>This method is good  to set up any subscriptions. If you do that, don’t forget to unsubscribe in componentWillUnmount().**
