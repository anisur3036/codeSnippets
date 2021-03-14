# JavaScript CodeSnippet

__Removing duplicates in an Array of Objects__
  - Method 1:
```js
const myArrayOfObjects = [...]; 

const myArrayOfObjects = Array.from(new Set(myArrayOfObjects.map(a => a.id)))
 .map(id => {
   return myArrayOfObjects.find(a => a.id === id)
 })
```
  - Method 2:
```js
const myArrayOfObjects = [
  { id: 1, name: "test1" },
  { id: 2, name: "test2" },
  { id: 2, name: "test3" },
  { id: 3, name: "test4" },
  { id: 4, name: "test5" },
  { id: 5, name: "test6" },
  { id: 5, name: "test7" },
  { id: 6, name: "test8" }
];

const filteredArr = myArrayOfObjects.reduce((acc, current) => {
  const x = acc.find(item => item.id === current.id);
  if (!x) {
    return acc.concat([current]);
  } else {
    return acc;
  }
}, []);
```
