# Create a function that walks through the dom.

input: dom node, callback
output: whatever you do with the callback, maybe find the first div?

```js
function walkTheDOM(node, func) {
    func(node);
    node = node.firstChild;
    while (node) {
        walkTheDOM(node, func);
        node = node.nextSibling;
    }
}

walkTheDOM(document.body, (node) => {
    if (node.nodeType === 3) {
        let text = node.data.trim();
        if (text.length > 0) {

        }
    }
});
```
