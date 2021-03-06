## ES6中的rest与spread

rest和spread作用类似且相反

### rest

rest类似于数组，作用于函数参数传递，基本构成为在数组名前添加**...**

基础示例：

```
function fun(...vals){
    for(let i = 0; i < vals.length; i ++){
        console.log(i);
    }
    let arr = vals;
    console.log(arr);
}

fun('a', 'b', 'c');
```

### spread

spread用于分割数组/字符串，作用类似于split，写法和rest非常相似，但是作用恰好相反

1） 基础示例

```
function fun(...vals){
    let arr = vals;
    console.log(...arr);
}

fun('a', 'b', 'c');
```

2） 数组合并

spread也可以用于辅助数组合并

```
let arr = ['a', 'b', 'c'];
function fun(...vals){
    let newArr = [...arr, ...vals];
    console.log(newArr);
}
fun('d', 'e', 'f');
```

3） 字符串分割

```
let val = 'hello';
console.log(...val);
```

### rest与spread的区别

1）rest用于函数参数传递
2）spread用于数组分割

