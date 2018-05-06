# interesting-interview-question

## 搜集觉得有意思的面试题

1. ‘goo4 comp1ny alway3 d2 thing5 righ6’ 将以上字符串按照正确的数字顺序排序.

``` js
var str='goo4 comp1ny alway3 d2 thing5 righ6';
function randomStr(str){
    var strArray= str.split(' ');
    strArray.sort((item1,item2)=>{
        return Number.parseInt(item1.match(/\d/)) - Number.parseInt(item2.match(/\d/));
    })
    return strArray.join(' ')
}

```

2. 编写一个getUID函数，每次调用时按调用先后返回 0,1,2,3….要求不污染全局变量。
``` js

var getUID = (function (){
    var number =0;
    return function (){
        return number++;
    }
})()
```

3. 实现一个洗牌算法（有序数组）
``` js

var arr=[1,2,3,4,5,6,7,8,9]
function random(arr){
    var length=arr.length;
    return arr.sort((item1,item2)=>{
            return Math.random() - Math.random();
    })
}

```