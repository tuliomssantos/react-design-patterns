#  [Composition](https://github.com/krasimir/react-in-patterns/blob/master/book/chapter-04/README.md)

* [Composition - Official Docs](https://reactjs.org/docs/design-principles.html#composition)
* [Composition vs Inheritance](https://reactjs.org/docs/composition-vs-inheritance.html)
* [Specialization](https://reactjs.org/docs/composition-vs-inheritance.html#specialization)

>The key feature of React is composition of components. Components written by different people should work well together. It is important to us that you can add functionality to a component without causing rippling changes throughout the codebase.

>For example, it should be possible to introduce some local state into a component without changing any of the components using it. Similarly, it should be possible to add some initialization and teardown code to any component when necessary.

>**Components are often described as “just functions” but in our view they need to be more than that to be useful. In React, components describe any composable behavior, and this includes rendering, lifecycle, and state.**
