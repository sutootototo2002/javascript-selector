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



No·4

    选择器                    例子                  例子描述                                       CSS
    
    element                  p                     选择所有p元素                                   1


例子：选择所有`<p>`元素

     

      04.html

     <style type='text/css'>
        p{ color:red;}
     </style>

       <p>p元素1</p> 

       <p>p元素2</p>

       <p>p元素3</p>


No·5

    选择器                    例子                  例子描述                                       CSS
    
    element,element          div,p                选择所有div和p元素                                1


例子：选择所有`<div>`和`<p>`元素

     

      05.html

     <style type='text/css'>

       div,p{ color:red;}

     </style>

       <p>p元素1</p> 

       <div>div元素1</div>

       <p>p元素2</p>

       <div>div元素2</div>

       <p>p元素3</p>

No·6

    选择器                    例子                  例子描述                                       CSS
    
    element element          div p                选择所有div元素内部p元素                          1


例子：选择所有`<div>`元素内部`<p>`元素

     

      06.html

     <style type='text/css'>

       p{color:green;}

       div p{ color:red;}

     </style>

       <p>p元素1</p> 

       <div>

         <p>p元素2</p>

       </div>

       
       <div>div元素2</div>

       <p>p元素3</p>


No·7

    选择器                    例子                  例子描述                                       CSS
    
    element>element          div>p                选择父元素为div元素的所有p元素                     2


例子：选择父元素为 `<div>` 元素的所有` <p>` 元素。

     

      07.html

     <style type='text/css'>

       p{color:green;}

       div>p{ color:red;}

     </style>

       <p>p元素1</p> 

       <div>

         <p>p元素2</p>

       </div>

       <div>

         <p>p元素2</p>

       </div>

       
       <div>div元素2</div>

       <p>p元素3</p>


No·8

    选择器                    例子                  例子描述                                       CSS
    
    element+element          div+p                选择紧接在div元素的p元素                          2


例子：选择紧接在`<div>`元素的`<p>`元素 

     

      08.html

     <style type='text/css'>

       p{color:green;}

       div+p{ color:red;}

     </style>

       <p>p元素1</p> 

       <div>

         <p>p元素2</p>

       </div>

       <div>

         <p>p元素2</p>

       </div>

       
       <div>div元素2</div>

       <p>p元素3</p>
  

     

No·9

    选择器                    例子                  例子描述                                       CSS
    
    [attribute]             [target]               选择带有target属性的所有元素                         2


例子：选择带有target属性的所有元素

     

      09.html

     <style type='text/css'>

       a[target]{color:yellow}

     </style>

       <a herf="javascript:;" target='aaa'>p元素1</p> 

       <a herf="javascript:;" target='bbb'>

         p元素2

       </div>

       <div>

         <p>p元素2</p>

       </div>

       
       <div>div元素2</div>

       <p>p元素3</p>




No.10

    选择器                    例子                  例子描述                                       CSS
    
    [attribute~=value]        [target=_blank]       选择target='_blank'的所有元素                    2


例子：选择带有`target='_blank'`属性的所有元素

     

      10.html

     <style type='text/css'>

       [target]{color:yellow}

     </style>

       <p target='aaa'>p元素1</p> 

       <div target='bbb'>

         <p>p元素2</p>

       </div>

       <div>

         <p>p元素2</p>

       </div>

       
       <div>div元素2</div>

       <p>p元素3</p>





No.11

    选择器                    例子                  例子描述                                       CSS
    
    [attribute|=value]        [lang|=en]       选择lang属性值以"en"开头的所有元素                    2


例子：选择lang属性值以"en"开头的所有元素     

     

      11.html

     <style type='text/css'>

       [lang|=en]{color:blue}

     </style>

       <p target='aaa'>p元素1</p> 

       <div target='bbb'>

         <p lang='en'>p元素2</p>

       </div>

       <div>

         <p>p元素2</p>

       </div>

       
       <div>div元素2</div>

       <p>p元素3</p>





No.12

    选择器                    例子                  例子描述                                       CSS
    
    :link                    a:link                选择所有未被访问的链接                            1


例子： 选择所有未被访问的链接  

     

      12.html

     <style type='text/css'>

       a:link{color:yellow;}

     </style>

       <a href="javascript:;"> 选择所有未被访问的链接 </a>



No.13

    选择器                    例子                  例子描述                                       CSS
    
    :visited                 a:visited             选择所有被访问过的链接                            1


例子： 选择所有被访问过的链接  


      13.html

     <style type='text/css'>

       a:visited{color:red;}

     </style>

       <a href="javascript:;">  选择所有被访问过的链接 为红色 </a>




No.14

    选择器                    例子                  例子描述                                       CSS
    
    :active                 a:active             选择活动链接                                      1


例子： 选择活动链接


      14.html

     <style type='text/css'>

       a:active{color:blue;}

     </style>

       <a href="javascript:;">  选择活动链接 </a>



No.15

    选择器                    例子                  例子描述                                       CSS
    
    :hover                   a:hover               选择鼠标指针位于其上的链接                        1


例子： 选择鼠标指针位于其上的链接


      15.html

     <style type='text/css'>

       a:hover{color:blue;}

     </style>

       <a href="javascript:;">  选择鼠标指针位于其上的链接 </a>


No.16

    选择器                    例子                  例子描述                                       CSS
    
    :focus                   input:focus           选择获得焦点的input元素                          2


例子： 选择获得焦点的`input`元素


      16.html

     <style type='text/css'>

       input:focus{color:green;} //当input 输入文字时，文字颜色为绿色

     </style>

       <input type='text'>


No.17

    选择器                    例子                  例子描述                                       CSS
    
    :first-letter            p:first-letter       选择每个 <p> 元素的首字母，并为其设置样式：         1


例子： 选择每个` <p> `元素的首字母，并为其设置样式：


      17.html

     <style type='text/css'>

      p:first-letter{font-size:200%;color:#8A2BE2}

     </style>

      <p> 选择每个p元素的首字母，并为其设置样式</p>  



No.18

    选择器                    例子                  例子描述                                       CSS
    
    :first-line              p:first-line          选择每个 <p> 元素的首行。                        1


例子： 选择每个 `<p>` 元素的首行，并为其设置样式：


      18.html

     <style type='text/css'>

      p:first-line{background-color:yellow;}

     </style>

      <p> 选择每个p元素的首行，并为其设置样式</p>  



No.18

    选择器                    例子                  例子描述                                       CSS
    
    :first-line              p:first-line          选择每个 <p> 元素的首行。                        1


例子： 选择每个 `<p> `元素的首行，并为其设置样式：


      18.html

     <style type='text/css'>

      p:first-line{background-color:yellow;}

     </style>

      <p> 选择每个p元素的首行，并为其设置样式</p>  



No.19

    选择器                    例子                  例子描述                                       CSS
    
    :first-child              p:first-child        选择属于父元素的第一个子元素的每个 <p> 元素。       2


例子： 选择每个 `<p>` 元素的首行，并为其设置样式：


      19.html

     <style type='text/css'>

      p:first-child{background-color:yellow;}

     </style>

      <p> 选择每个p元素的首行，并为其设置样式</p>  


      <div>
       <p> 选择每个p元素的首行，并为其设置样式</p>  
      </div>




No.20

    选择器                    例子                  例子描述                                       CSS
    
    :before                  p:before              在每个 <p> 元素的内容之前插入内容。                2


例子：  在每个 <p> 元素的内容之前插入内容。


      20.html

     <style type='text/css'>

      p:before{content:'台词：'}

     </style>

      <p>在每个 <p> 元素的内容之前插入内容。</p>  


No.21

    选择器                    例子                  例子描述                                       CSS
    
    :after                   p:after               在每个 <p> 元素的内容之后插入内容。                2


例子：  在每个 <p> 元素的内容之后插入内容。


      21.html

     <style type='text/css'>

      p:after{content:'台词：'}

     </style>

      <p>在每个 <p> 元素的内容之后插入内容。</p>  



No.22

    选择器                    例子                  例子描述                                            CSS
    
    :lang(language)          p:lang(it)            选择带有以 "it" 开头的 lang 属性值的每个 <p> 元素。     2


例子：  选择带有以 "it" 开头的 lang 属性值的每个 <p> 元素。


      22.html

     <style type='text/css'>

      p:lang(en){background:yellow}

     </style>

      <p lang='en'>在每个 <p> 元素的内容之后插入内容。</p>  


No.23

    选择器                    例子                  例子描述                                            CSS
    
    element1~element2        p~ul                  选择前面有 <p> 元素的每个 <ul> 元素。                  3


例子：   选择前面有 <p> 元素的每个 <ul> 元素。


      23.html

     <style type='text/css'>

      <style> 
		p~ul
		 {
		  background:#ff0000;
	     }
     </style>

      <div>一个 div 元素。</div>
		<ul>
		  <li>咖啡</li>
		  <li>牛奶</li>
		  <li>茶</li>
		</ul>
		
		<p>第一段。</p>
		<ul>
		  <li>咖啡</li>
		  <li>牛奶</li>
		  <li>茶</li>
		</ul>
		
		<h2>另一个列表</h2>
		<ul>
		  <li>咖啡</li>
		  <li>牛奶</li>
		  <li>茶</li>
		</ul>



No.24

    选择器                    例子                  例子描述                                            CSS
    
    [attribute^=value]       a[src^='https']       选择其 src 属性值以 "https" 开头的每个 <a> 元素。       3


例子：   选择前面有 <p> 元素的每个 <ul> 元素。


      24.html

     <style type='text/css'>

      <style> 
		a[src^='https']{

         background:#ffff00;

        }
     </style>

       <a href="https://www.floweryan.com">选择其 src 属性值以 "https" 开头的每个a 元素。</a>



No.25

    选择器                    例子                  例子描述                                            CSS
    
    [attribute$=value]       a[href$='.pdf']       选择其 href 属性以 ".pdf" 结尾的所有 <a> 元素。          3


例子：   选择前面有 <p> 元素的每个 <ul> 元素。


      25.html

     <style type='text/css'>
 
		a[href$='.com']{

         background:#ffff00;

        }
     </style>

       <a href="https://www.floweryan.com">选择其 href 属性值以 "https" 开头的每个a 元素。</a>



No.26

    选择器                    例子                  例子描述                                            CSS
    
    [attribute*=value]       a[href*='.pdf']      选择其 href 属性中包含 "abc" 子串的每个 <a> 元素。          3


例子：   选择前面有 <p> 元素的每个 <ul> 元素。


      26.html

     <style type='text/css'>
 
		a[href*='com']{

         background:#ffff00;

        }
     </style>

       <a href="com">选择其 href 属性值以 "https" 开头的每个a 元素。</a> 

       <a href="a_com">选择其 href 属性值以 "https" 开头的每个a 元素。</a>


No.27

    选择器                    例子                  例子描述                                            CSS
    
    :first-of-type            P:first-of-type       选择属于其父元素的首个 <p> 元素的每个 <p> 元素。        3


例子：   选择属于其父元素的首个 <p> 元素的每个 <p> 元素。


      27.html

     <style type='text/css'>
 
		p:first-of-type{

          background:#ffff00;

          }
     </style>

       <h1>这是标题</h1>

       <p>这是第一个段落。</p>
       <p>这是第二个段落。</p>
       <p>这是第三个段落。</p>
       <p>这是第四个段落。</p>


No.28

    选择器                    例子                  例子描述                                            CSS
    
    :last-of-type            P:last-of-type       选择属于其父元素的最后 <p> 元素的每个 <p> 元素。        3


例子：   选择属于其父元素的首个 <p> 元素的每个 <p> 元素。


      28.html

     <style type='text/css'>
 
		p:first-of-type{

          background:#ffff00;

          }
     </style>

       <h1>这是标题</h1>

       <p>这是第一个段落。</p>
       <p>这是第二个段落。</p>
       <p>这是第三个段落。</p>
       <p>这是第四个段落。</p>


No.29

    选择器                    例子                  例子描述                                            CSS
    
    :only-of-type            P:only-of-type       选择属于其父元素唯一的 <p> 元素的每个 <p> 元素。          3


例子：   选择属于其父元素唯一的 <p> 元素的每个 <p> 元素。


      29.html

     <style type='text/css'>
 
		p:only-of-type{

          background:#ffff00;

          }
     </style>

       <div>
       <p>这是第一个段落。</p>
       </div>
       <div>
       <p>这是第一个段落。</p>
       <p>这是第二个段落。</p>
       <p>这是第三个段落。</p>
       <p>这是第四个段落。</p>
       </div>




No.30

    选择器                    例子                  例子描述                                            CSS
    
    :only-child            P:only-child            选择属于其父元素的唯一子元素的每个 <p> 元素。            3


例子：   选择属于其父元素的唯一子元素的每个 <p> 元素。


      30.html

     <style type='text/css'>
 
		p:only-child{

          background:#ffff00;

          }
     </style>

       <div>
       <p>这是第一个段落。</p>
       </div>
       
       <div>
       <p>这是第一个段落。</p>
       <p>这是第二个段落。</p>
       <p>这是第三个段落。</p>
       <p>这是第四个段落。</p>
       </div>



No.31

    选择器                    例子                  例子描述                                            CSS
    
    :nth-child(n)            P:nth-child(n)        选择属于其父元素的第二个子元素的每个 <p> 元素。            3


例子：   选择属于其父元素的第二个子元素的每个 <p> 元素。


      31.html

     <style type='text/css'>
 
		p:nth-child(2){

          background:#ffff00;

          }
     </style>

       <div>
       <p>这是第一个段落。</p>
       </div>
       
       <div>
       <p>这是第一个段落。</p>
       <p>这是第二个段落。</p>
       <p>这是第三个段落。</p>
       <p>这是第四个段落。</p>
       </div>


No.32

    选择器                    例子                  例子描述                                            CSS
    
    :nth-last-child(n)            P:nth-last-child(n)        同上，从最后一个子元素开始计数。            3


例子：   同上，从最后一个子元素开始计数。


      32.html

     <style type='text/css'>
 
		p:nth-last-child(2){

          background:#ffff00;

          }
     </style>

       <div>
       <p>这是第一个段落。</p>
       </div>
       
       <div>
       <p>这是第一个段落。</p>
       <p>这是第二个段落。</p>
       <p>这是第三个段落。</p>
       <p>这是第四个段落。</p>
       </div>



No.33

    选择器                    例子                  例子描述                                            CSS
    
    :nth-of-type(n)       P:nth-of-type(n)        选择属于其父元素第二个 <p> 元素的每个 <p> 元素。            3


例子：   选择属于其父元素第二个 <p> 元素的每个 <p> 元素。 


      33.html

     <style type='text/css'>
 
		p:nth-of-type(2){

          background:#ffff00;

          }
     </style>

       <p>ssss</p>
       <p>sssss</p>
       
       <div>
       <p>susususu</p>
       <p>susususus</p>


No.34

    选择器                    例子                         例子描述                                    CSS
    
    :nth-last-of-type(n)     P:nth-last-of-type(n)        同上，但是从最后一个子元素开始计数。            3


例子：    同上，但是从最后一个子元素开始计数。   


      34.html

     <style type='text/css'>
 
		p:nth-last-of-type(2){

          background:#ffff00;

          }
     </style>

       <p>ssss</p>
       <p>sssss</p>
       
       <div>
       <p>susususu</p>
       <p>susususus</p>
       </div>


No.35

    选择器                    例子                         例子描述                                    CSS
    
    :last-child              P:last-child                 选择属于其父元素最后一个子元素每个 <p> 元素。    3


例子：    同上，但是从最后一个子元素开始计数。   


      35.html

     <style type='text/css'>
 
		p:last-child{

          background:#ffff00;

          }
     </style>

       <p>ssss</p>
       <p>sssss</p>
       
       <div>
       <p>susususu</p>
       <p>susususus</p>
       </div>



No.36

    选择器                    例子                         例子描述                                    CSS
    
    :root                    :root                        选择文档的根元素。                             3


例子：    选择文档的根元素。  


      36.html

     <style type='text/css'>
 
		:root{

          background:#ffff00;

          }
     </style>

       <p>ssss</p>
       <p>sssss</p>
       
       <div>
       <p>susususu</p>
       <p>susususus</p>
       </div>



No.37

    选择器                    例子                         例子描述                                    CSS
    
    :empty                   p:empty                      选择没有子元素的每个 <p> 元素（包括文本节点）。   3


例子： 选择没有子元素的每个 <p> 元素（包括文本节点）。


      37.html

     <style type='text/css'>
 
		p:empty{

          background:#ffff00;

          }
     </style>

       <p><a href='#'>ssss</a></p>
       <p>sssss</p>


No.38

    选择器                    例子                         例子描述                                    CSS
    
    :target                   #new:target                 选择当前活动的 #news 元素。                    3


例子： 选择当前活动的 #news 元素。 


      38.html

     <style type='text/css'>
 
		  :target{

          background:#ffff00;

          }
     </style>

       <p><a href='#news1'>ssss</a></p>
       <p><a href='#news2'>ssss</a></p> 



       <p id='news1'>contents1</p>
       <p id='news2'>contents2</p>
       



No.39

    选择器                    例子                         例子描述                                    CSS
    
    :enabled                 input:enabled                选择每个启用的 <input> 元素。                 3


例子： 选择每个启用的 <input> 元素。


      39.html

     <style type='text/css'>
 
		  input[type='text']:enabled{

          background:#ffff00;

          }
     </style>

      <input type='text'>   






No.40

    选择器                    例子                         例子描述                                    CSS
    
    :disabled                 input:disabled              选择每个禁用的 <input> 元素。                 3


例子： 选择每个禁用的 <input> 元素。 


      40.html

     <style type='text/css'>
 
		  input[type='text']:disabled{

          background:#ccc;

          }
     </style>

      <input type='text' disabled='disabled' value="此项禁用">  



No.41

    选择器                    例子                         例子描述                                    CSS
    
    :checked                 input:checked                选择每个被选中的 <input> 元素。                3


例子： 选择每个禁用的 <input> 元素。 


      41.html

     <style type='text/css'>
 
		  input:checked{

          background:yellow;

          }
     </style>

      <input type='text' checked='checked' value="被选中状态">   



No.42

    选择器                    例子                         例子描述                                    CSS
    
    :not(selector)           :not(p)                      选择非<p>元素的每个元素                       3


例子： 选择非<p>元素的每个元素。 


      42.html

     <style type='text/css'>
 
		  ：not(p){

          background:yellow;

          }
     </style>

      <div>11111111111111111111111111</div> 
      <div>11111111111111111111111111</div>
      <p>22222222222222222222222222</p>
      <a href='#'>333333333333333</a>


No.43

    选择器                    例子                         例子描述                                    CSS
    
    ::selection              ::selection                      选择被用户选取的元素部分。                  3


例子： 选择被用户选取的元素部分。 


      43.html

     <style type='text/css'>
 
		    ::selection
			{
			color:#ff0000;
			}
			
			::-moz-selection
			{
			color:#ff0000;
			}
          
     </style>

      <h1>请试着选取页面上的文本</h1>

      <p>这是一个段落。</p>

      <div>这是 div 元素中的文本。</div>


