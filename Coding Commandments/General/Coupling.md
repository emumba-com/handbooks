Coupling is a commonly used term in software development that identifies degree of interdependence between two pieces of code. When this interdependence is high, you have strong coupling. When this interdependence is low, you have low coupling. Consider this example:

```
const doc = await fs.readFile('/usr/local/test.json')

export function makeJSON() {
    return JSON.stringify(doc)
}
```

The function `makeJSON()` here is tightly coupled to the file it is placed in, because it is dependent upon a reference from its environment to execute. Which implies that the reusability of logic you've written under this function is greatly reduced. 

Loosening up the coupling of this function with its environment will dramatically improve its re-usability, and testability. Here is how you'd do it:

```
export function makeJSON(doc) {
    return JSON.stringify(doc)
}
```

You can judge quality of a codebase by seeing how tightly coupled are different pieces of code. Tighter the coupling, lower the quality.