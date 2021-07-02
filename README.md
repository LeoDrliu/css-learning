# css-learning
### 浏览器渲染大致过程

1. 根据HTML文件构建一个DOM Tree
2. 再根据CSS构建一个CSS Rule Tree
3. 把以上两棵树合并成一颗Render Tree
4. 有了Render Tree便可以知道该网页中得所有节点及其属性，便可以进行layout布局，即根据文档流和盒模型确定每个节点的大小和其屏幕中所属的位置
5. 再进行绘制，即paint，把各个节点的边框颜色、文字颜色和阴影等画在屏幕上
6. 最后完成compose，即根据层叠关系来展示画面



### CSS动画的做法

#### transition

- 作用：在CSS动画变化过程中，补充中间帧，使图形的变化连续
- 语法：transition: 属性名 | 时长 | 过渡方式 | 延迟
- 多属性之间可以用逗号进行分隔，同时可以用all来统一表示所有属性
- 但并不是所有属性的变化都可以用transition过渡，如display:none->block

#### animation

- 作用：在CSS动画过渡过程中，增加中间点，使其非一次连续

- 语法：animation: 属性名(keyframes名) | 时长 | 过渡方式 | 延迟| 次数|方向| 填充模式| 是否暂停| 动画名。

  keyframes语法有如下两种：

  1. from to

     ```css
     @keyframes slidein {
       from {
         transform: translateX(0%);
       }
     
       to {
         transform: translateX(100%);
       }
     }
     ```

  2. 百分号

     ```css
     @keyframes identifier {
       0% { top: 0; left: 0; }
       30% { top: 50px; }
       68%, 72% { left: 50px; }
       100% { top: 100px; left: 100%; }
     }
     ```

     



