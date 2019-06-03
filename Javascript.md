- Array.protptype.map

  ```js
  [0,1,2].map(Boolean)  //[false,true,true]
  ```

  map 传入的callback 函数会自动的传入三个参数，**当前的值，当前的索引，数组本身**，所以上面的代码等价于

  ```js
  [0,1,2].map((item,index,arr)=>Boolean(item,index,arr))  //[false,true,true]
  ```

  举一个更容易明白的例子

  ```js
  const func = (item,index,arr) => {
  	console.log(`索引为${index}的值是${item}`)
  }
  ['a','b','c'].forEach(func)
  /*
  索引为0的值是a
  索引为1的值是b
  索引为2的值是c
  */
  ```

  > map / forEach / fliter 等均有此特性

  