Instead of re-rendering the entire DOM on state change, React uses a Diffing algorithm
=> The Diffing algorithm is responsible to determine the minimal number of changes required to update the DOM, improving performance

- Compares the new Virtual DOM with the previous version
- Identifies What has changed
- Updates only the necessary parts of the actual DOM

Tree Comparison => Element Comparison => Reconciliation of Child Nodes => Recursive Application

