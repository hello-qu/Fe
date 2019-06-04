- path.resolve / path.join()

  `path.resolve` 会从右到左解析路径 ，`path.join` 是从左到右依次解析路径

  ```js
  var p1 = path.resolve('./a','./b','/c')
  //从右到左 /c 直接是个相对根路径 所以直接显示为/c
  var p2 = path.resolve('./a','./b','./c')
  //最右是相对路径下的c，还不是绝对路径，往左遇到 ./b 拼成 ./b/c 还不是绝对路径 再往左就是 .a/b/c
  //这样仍然是相对路径，这时候最终路径不是绝对路径的话需要拼接当前a文件所在的绝对路径
  var p3 = path.join('a','./b','c')
  
  
  ```

  