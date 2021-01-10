#### Lesson Challenge

Read these 4 articles: [Understanding the React Component Lifecycle](http://busypeoples.github.io/post/react-component-lifecycle/), [React component’s lifecycle](https://medium.com/react-ecosystem/react-components-lifecycle-ce09239010df), [Understanding React — Component life-cycle](https://medium.com/@baphemot/understanding-reactjs-component-life-cycle-823a640b3e8d), and [React JS: what is a PureComponent?](http://lucybain.com/blog/2018/react-js-pure-component/) and answer the following questions in the #explain-it channel:

1.  Describe what the in the workspace below will render on the screen and explain why.
    1. A label (some color) and a value (in seconds) will display for each component referenced in app including: Pure, Stateless, Normal1, Normal2, and Normal3
    1. The Pure component's value will not change after the initial render because it extends PureComponent, which it's shouldComponentUpdate method skips prop updates for the whole component subtree. 
    1. The components: Stateless, Normal1, and Normal2 receive the props as they are updated and rerender with the updated values
    1. The Normal3 component's value changes because the rerender of the app component triggers it's render method.
2.  Describe a React anti-pattern that's used in the code.
    1. Managing derived state from props is the anti-pattern that create the behavior of the app. State is actually not needed in Pure, Normal1, and Normal2 components. It really could just use the props as they are where the state is handled in the app component.
3.  How do we need to modify the `Normal3` Component in order to keep it from re-rendering if the `App` Component's state remains the same?
    1. Change the class component to extend PureComponent rather than Component.

This exercise is based on this sandbox: https://codesandbox.io/s/3vpp84yp5.
