# Day 2

## Part 1
```js
let raw = `...`;
let safe_count = 0;
raw.split('\n').forEach((item)=>{
    let vals = item.split(' ');
    let last = parseInt(vals.shift());
    let safe = true;
    let dir = false;
    vals.forEach((val)=>{
        let cur = parseInt(val)
        let diff = last - cur;
        let cur_dir = diff > 0 ? "pos" : "neg";
        if (!dir) dir = cur_dir
        if (dir != cur_dir) safe = false;
        if (![1, 2, 3].includes(Math.abs(diff)))
            safe = false;
        last = cur;
    });
    if (safe) safe_count++
});
console.log("Safe Reports:", safe_count);
```
gross, right?

## Part 2
```js
TBD
```
