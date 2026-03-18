# Codewars-Sort the odd (Javascript)
1. 
```
function sortArray(array) {
  const oddArr = [];
  const oddArrIndex = [];
  array.forEach((v, i) => {
    if (v%2 !== 0) {
      oddArr.push(v);
      oddArrIndex.push(i);
    }
  })
  oddArr.sort((a, b) => a-b);
  oddArrIndex.forEach((v, i) => {
    array[v] = oddArr[i];
  })
  return array;
}
```
2. 
```
function sortArray(array) {
  const oddArr = array.filter(v => v%2 !== 0).sort((a, b) => a-b);
  
  array.forEach((v, i) => {
    if (v%2 !== 0) {
      array[i] = oddArr.shift();
    }
  })
  
  return array;
}
```
---

[KATA](https://www.codewars.com/kata/578aa45ee9fd15ff4600090d/javascript)
