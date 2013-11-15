javascript-selector
===================

javascript 选择器学习

今天开始我要研究一下javascript选择器，javascript选取一组或一个DOM元素。这就是选择器的作用。
初学javascript真的是一头雾水，不知从哪看起，现在先分析一下css选择器和jquery的的sizzle选择器吧。

**css3选择器：**

No·1

    选择器                    例子                  例子描述                                       CSS
    
    .class                   .intro                选择class='intro'的所有元素                      1


例子：选择所有class='intro'的元素

     

      01.html

     <style type='text/css'>
        .intro{width:200px;height:200px;border:1px solid red;}
     </style>

     <div class='intro'>box</div>

No·2

     选择器                    例子                  例子描述                                       CSS
    
     #id                      #firstname           选择id='firstname'的所有元素                      1


例子：选择id='firstname'的所有元素 (id只能选最先出现的一个)


      02.html

     <style type='text/css'>
        #firstname{width:200px;height:200px;background-color:green;}
     </style>

     <div id='firstname'>box</div>


No·3

    选择器                    例子                  例子描述                                       CSS
    
    *                         *                   选择所有元素                                     2


例子：选择所有的元素

     

      03.html

     <style type='text/css'>
        *{margin:0;padding:0;}
        .div1{position:absoulte;top:0;left:0;bottom:0;right:0;width:100%;height:100%;border:1px solid red;}
     </style>
        <div class='div1'></div>

     