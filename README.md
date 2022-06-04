# layout-page-training
Page layout in interview exercise

```
<div class="container">
  <div class="left"></div>
  <div class="center"></div>
  <div class="right"></div>
</div>
```

## 1、弹性盒
```
  .container {
    display: flex;
    overflow: hidden;
    height: 10px;
  }
  .container div {
    height: 100%;
  }

  .center {
    flex: 1;
    background: red;
  }
  .left {
    width: 10%;
    background-color: #090;
  }
  .right {
    width: 10%;
    background-color: #708;
  }
```

## 2、定位 
  position: absolute;
```
  .container {
    position: relative;
    overflow: hidden;
    height: 10px;
  }
  .container div {
    height: 100%;
  }

  .left,
  .center,
  .right {
    position: absolute;
  }

  .center {
    background: red;
    left: 10%;
    right: 10%;
  }
  .left {
    width: 10%;
    left: 0;
    background-color: #090;
  }
  .right {
    width: 10%;
    right: 0;
    background-color: #708;
  }
```
  
## 3、浮动解决方案（三列左浮动，右一右浮动，三列设置宽度）
```
  .container {
      position: relative;
      overflow: hidden;
  }
  .container div {
      height: 10px;
  }

  .left,
  .center,
  .right {
      float: left;
  }

  .center {
      background: red;
      width: 80%;
  }

  .left {
      width: 10%;
      float: left;
      background-color: #090;
  }
  .right {
      width: 10%;
      float: right;
      background-color: #708;
  }
  ```
float

## 4、表格
  display：table
  ```
  .container {
    display: flex;
    overflow: hidden;
    height: 10px;
  }
  .container div {
    height: 100%;
  }

  .center {
    flex: 1;
    background: red;
  }
  .left {
    width: 10%;
    background-color: #090;
  }
  .right {
    width: 10%;
    background-color: #708;
  }
  ```

## 5、网格布局
  display：grid；
  ```
  .container {
    display: grid;
    overflow: hidden;
    width: 100%;
    grid-template-columns: 100px auto 100px;
    grid-template-rows: 10px;
  }

  .center {
    background: red;
  }
  .left {
    background-color: #090;
  }
  .right {
    background-color: #708;
  }
  ```

```
五种方案的区别？优缺点？
假设去掉高度，哪一个不适用？（浮动原理，BFC ）
这几种方案的兼容性如何？
```

```
页面布局小结：
  语义化掌握要到位
  页面不绝理解深刻
  CSS基础知识扎实
  思维灵活且积极上进
  代码书写规范
  
页面布局的变通：
  三栏布局：
    左右宽度固定，中间自适应
    上下高度固定，中间自适应
  两栏布局：
    左宽度固定，右自适应
    右宽度固定，左自适应
    上高度固定，下自适应
    下高度固定，上自适应
```
    
    
    
