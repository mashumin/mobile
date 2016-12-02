# flex 弹性布局盒模型
## 设置弹性盒模型
1. display:flex (新版)
2. display:-webkit-box; (旧版)
##flex容器
1. 项目排列方向
  1.1 从左到右排练 <br>
  1.2 row-reverse 从右到左<br>
  1.3 column从上到下<br>
  1.4 column-reverse从下到上<br>


     flex-direction: row | row-reverse |column |column-reverse


    horizontal 水平方向
    vertical 垂直方向

    -webkit-box-orient:horizontal | vertical

    normal 顺序正常

    reverse 反向

    -webkit-box-direction:normal |reverse
2. 项目包裹方式
  2.1 nowrap不换行（默认）<br>
  2.2 wrap容器如果不足以放下项目，自动换行倒下一行。<br>
  2.3  wrap-reverse 容器如果不足以放下项目,自动换行到上一行<br>


      flex-wrap:nowrap | wrap | wrap-reverse

3. 项目水平对齐方式
    3.1 flex-start 左对齐 <br>
    3.2 flex-end 右对齐 <br>
    3.3 center对齐<br>
    3.4 space-between两端对齐<br>
    3.5 space-around 每个项目两侧的间隔相等<br>


     justify-content:flex-start | flex-end | center | space-between | space-around


    start 左对齐
    end 右对齐
    justiry 两队对齐



    -webkit-box-pack: start | end |center |justify



5. 多行对齐方式
  5.1 flex-start左对齐
  5.2 flex-end 右对齐
  5.3 center居中对齐
  5.4 space-between 两端对齐
  5.5 space-around 每个人项目距离项目距离相同
  5.6 stretch 项目沾满个屏幕（拉申）



    align-content:  flex-start | flex-end | center | space-between | space-around | stretch


## 项目列表
1.项目排序
  1.1项目的排序，数字越小越靠前。默认为0 `接受负值`



  order：<int>




    项目的排序，数字越小越靠前，默认为1，`将0或负数转为1`




    -webkit-box-ordinal-group:




2.项目占比（放大）
  2.1 所占栅格比例，默认为零 `项目的尺寸=容器的尺寸、总栅格数*当前栅格数`




  flex-grow：<int>




    老版弹性布局设置项目栅格




    -webkit-box-flex : <int>




3.项目占比（缩小）
  3.1 所占栅格比例默认为1



     flex--shrink:<int>



4.项目所占空间大小
  4.1可以设置项目大小 类似于width/height属性



  flex-basis:<size> | auto




5.项目自己的对齐方式 `优先级高于容器的align-items`



     align-self: auto | flex-start | flex-end | center | baseline | stretch;



