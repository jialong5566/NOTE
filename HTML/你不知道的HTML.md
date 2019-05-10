sublime 设置 font_face:comic sans ms
文件夹命名：全小写，混合写会导致cmd命令框找不到文件
============================================
同源策略：
协议—HTTP/HTTPS
域名—必须一样
端口—80/443
------------------------------------
1.浏览器不同的域名不能访问对应的cookie，但是内部的表单没有限制。
   示例<form action="http://www.diffrentorigin.com/a.php">
   action所提交的网址域名 不受 该网页所在域名限制。
2.同源策略限制的行为
    a)无法读取以下3种：
    cookie
    localStorage 超过2.5M影响性能
    IndexedDB
    b)  DOM无法获得
    c)  ajax不能发送请求
--------------------------------------------
Cookie 和 iframe 窗口在以下情况可以共享：
在浏览器设置document.domain = "相同的一级域名"
tianjin.58.com 与 beijing.58.com
设置 document.domain = "58.com"

服务器设置Cookie，指定一级域名
Set-Cookie:key=val;domain=.58.com;path=/
--------------------------------------------
跨域方式
script（jsonp） 、img 、iframe 的src不受同源策略的限制
link(background的url属性)
CORS 可以使用任何请求方式进行跨域

jsonp使用方式
和后端商量好函数，函数名放在src末尾，当请求回来数据，将数据直接传入函数执行。

var s = new Image();
var start = Date.now();
s.onload= function(){
    var duration = Date.now()-start;
    var v = s.size/duration;
	"测试网速，匹配版本"
}

postMessage 使用
var popup = window.open("http://bbb.com");
popup.postMessage("the message","http://aaa.com");
监听信息
window.addEventListener('message',function(e){
    console.log(e.data);
},false)
=========================================
HTML 语义化（有利于爬虫搜索）

不用div进行无意义包裹
span只是常见的元素
p标签可以明显分段
h1-h6标签写标题
strong与em标签的使用
input标签与label配合使用
尽量少写html，减少dom渲染时间
对应名词的解释用dl、dt、dd
----------------------------
H5标签
<header>
    <nav></nav>
</header>
<article>
    <aside></aside>
    <section></section>
    <section></section>
    ...
</article>
<footer></footer>
===============================
高阶 websocket postmessage