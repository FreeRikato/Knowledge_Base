Virtual DOM is the lightweight copy of the Real DOM that allows React to manage changes more efficiently by minimizing the direct manipulation required on the Real DOM.

- Reconciliation Process in POV of VDOM
> Instead of directly manipulating the real DOM whenever something changes in the application, React first makes these changes to the Virtual DOM.
> After that, React compares the updated Virtual DOM with a snapshot of the previous version and determines the efficient way to apply these changes to the actual DOM

Initial rendering => State changes => Diffing algorithm => Minimal updated to the real DOM => Re-rendering the UI
