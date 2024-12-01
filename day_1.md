# Day 1

## Part 1
```js
let raw = `...`; // Paste you own raw data here 
let left = [];
let right = [];
let distances = [];
raw.split('\n').forEach((a)=>{
    let row = a.split('   ');
    left.push(row[0]);
    right.push(row[1]);
})
left.sort((a,b)=>a-b);
right.sort((a,b)=>a-b);
left.forEach((item, i)=>{
    distances.push(Math.abs(left[i] - right[i]));
})
console.log("Sum:", distances.reduce((a,b)=>a+b));
```

## Part 2
```js
let left = [];
let right = [];
raw.split('\n').forEach((a)=>{
    let row = a.split('   ');
    left.push(row[0]);
    right.push(row[1]);
})
left.sort((a,b)=>a-b);
right.sort((a,b)=>a-b);
let occurances = [];
left.forEach((item, i)=>{
    let count = right.filter((a)=>a == item).length;
    if (count != 0)
        occurances.push([item, count]);
})
let total = 0;
occurances.forEach((item)=>{
   total += (parseInt(item[0]) * item[1]); 
});
console.log("Score:", total);
```
