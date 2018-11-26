### 盒子模型有哪几种，有什么区别？

有两种： border-box 和 content-box

主要区别有：border-box 会将自身的border宽度和padding计算在width之内。而content-box 则会叠加在自身本身的width之上。

### CSS 选择符有哪些？

- id 选择器

  ```css
  #root{ width: 10px; }
  ```

- 类名选择器

  ```css
  .root{ width: 10px; }
  ```

- 标签选择器

  ```css
  h1{ width: 10px; }
  ```

- 相邻选择器

  ```css
  h1+p{ width: 10px; }
  ```

- 子选择器

  ```css
  ul > li { width: 10px; }
  ```

- 后代选择器

  ```css
  ul li { width: 10px; }
  ```

- 通配符选择器

  ```css
  *{ margin: 0; padding: 0; }
  ```

### 如何居中div？

```css
div{
    width: 100px;
    height: 100px;
}

.first{
    position: relative;
    left: 50%;
    top: 50%;
    margin-left: -50px;
    margin-top: -50px;
}

.second{
    display: flex;
    justify-content: center;
    align-items: center;
}

.third{
    .content{
        position: relative;
        .inner{
            position: absolute;
            left: 50%;
            top: 50%;
            margin-left: -50px;
            margin-top: -50px;
        }
    }
}

.forth{
    margin-left: -100%;
    transform: translate(-50%, -50%);
}

.fifth{
    .content{
        position: relative;
        .inner{
            position: absolute;
            left: 0;
            right: 0;
            top: 0;
            bottom: 0;
            margin: auto;
        }
    }
}
```

### position 有哪些值？relative 和 absolute 定位的原点是什么？

- absolute: 生成绝对定位的元素，相对于值不为static的第一个元素进行定位。
- fixed：生成绝对定位的元素，相对于浏览器窗口进行定位。
- relative：生成相对定位的元素，相对于其正常位置进行定位。
- static：默认值，没有定位，元素处于正常的文档流。
- inherit：从父元素继承position的值。

### CSS3 有哪些新特性？

- 新增选择器：

  ```css
  p:nth-child(1){ width: 10px; }
  ```

- 新增盒模型： 

  ```css
  div{ display: flex; }
  ```

- 媒体查询：

  ```css
  @media (max-width: 480px){
      div{ width: 10px; }
  }
  ```

- 圆角：

  ```css
  div{ border-radius: 50%; }
  ```

- 阴影：

  ```css
  div{ box-shadow: 3px 3px 3px rgba(0, 0, 0, 0); 
  ```

- 平滑过渡：

  ```css
  div{ transition: all .3s ease-in; }
  ```

- 动画：

  ```css
  @keyframes anima{
      50%{
          border-radius: 50%;
      }
      100%{
          border-radius: 100%;
      }
  }
  div{
      animation: anima 1s;
  }
  ```

- 转换：

  ```css
  div{ transform: rotate(20deg);}
  ```

### 如何设置品字布局

上面div宽100%， 下面两个div 宽度50% ，然后不让其换行。

### 圣杯布局

```html
  <div class="outer">
    <div class="middle"></div>
    <div class="left"></div>
    <div class="right"></div>
  </div>
```

```css
*{
  margin: 0;
  padding: 0;
  
}

.outer{
  border:1px solid red;
  padding: 0 100px;
}


.middle{
  position: relative;
  float: left;
  background-color: red;
  width: 100%;
  height: 100px;
  
}

.left{
  position: relative;
  float: left;
  background-color: blue;
  width: 100px;
  height: 100px;  
  left: -100px;
  margin-left: -100%;
}

.right{
  position: relative;
  float: left;
  background-color: pink;
  width: 100px;
  height: 100px; 
  right: -100px;
  margin-left: -100px;
}

```

### 双飞翼布局

```html

```



