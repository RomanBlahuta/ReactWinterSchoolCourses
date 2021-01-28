# React Hook Flow

## 1st Run
* React starts to render the component
* React executes the useState callback
* React ends rendering the component
* All useEffects are called in order (asynchronously after rendering)

## Rerender with Children Example

* Start to render the component
* If useState uses lasy initializer then it is skipped
* Render ends
* Starting to render the child
* Child initial useSatte callback execution
* Child render end
* Child useEffects are called
* Parent useEffect cleanups
* Parent useEffect calls (if dependencies were not given or changed value)

<br/>

* If something changed inside the child only the child will be actually rerendered, not the entire app.

## Removing the Child

* Rerendering the parent component
* End of rerender
* All child useEffect cleanups
* Parent's cleanups
* Parent's useEffects