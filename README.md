http缓存

强制缓存
协商缓存

----------
#### Jquery中$(document).ready()的作用类似于传统JavaScript中的window.onload方法，不过与window.onload方法还是有区别的。 ####

1.执行时间 

        window.onload必须等到页面内包括图片的所有元素加载完毕后才能执行。 
        $(document).ready()是DOM结构绘制完毕后就执行，不必等到加载完毕。 

2.编写个数不同 

         window.onload不能同时编写多个，如果有多个window.onload方法，只会执行一个 
         $(document).ready()可以同时编写多个，并且都可以得到执行 

3.简化写法 

         window.onload没有简化写法 
         $(document).ready(function(){})可以简写成$(function(){});
----------
#### 三个简单实用的用于 DOM 操作的 jQuery 方法：<br>
text() - 设置或返回所选元素的文本内容<br>
html() - 设置或返回所选元素的内容（包括 HTML 标记）<br>
val() - 设置或返回表单字段的值<br>

----------
#### setTimeout(0)
场景：当浏览器尺寸发生变化时（window.onresize）、当某个标签样式为动态时<br>
问题：使用jQuery给div设置宽高报错<br>
原因：DOM还没有渲染完<br>
解决方法：setTimeout(fn, 0, false);（fn为设置宽高的函数）<br>
实现原理：<br>

----------
#### jQuery对象和DOM对象
场景：使用ng-repeat实现多条对话的展示，动态改变其展开/收起按钮的宽高<br>
问题:使用jQuery设置宽高报错<br>
原因：jquery对象不能使用dom的方法，dom对象不能使用jquery方法<br>
解决方法：使用query对象转换成一个dom对象的方法：[index]和get(index)<br>

