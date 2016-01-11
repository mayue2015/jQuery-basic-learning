# jQuery-basic-learning
a simple jQuery basic learning notes

1.有两个版本的 jQuery 可供下载：
Production version - 用于实际的网站中，已被精简和压缩。
Development version - 用于测试和开发（未压缩，是可读的代码）

2.$(this).hide() - 隐藏当前元素

3.隐藏/显示：
$(selector).hide(speed,callback);
$(selector).show(speed,callback);
可选的 speed 参数规定隐藏/显示的速度，可以取以下值："slow"、"fast" 或毫秒。
可选的 callback 参数是隐藏或显示完成后所执行的函数名称。

4.切换显示和隐藏：
$(selector).toggle(speed,callback);

5.淡入/淡出
$(selector).fadeIn(speed,callback);
$(selector).fadeOut(speed,callback);
$(selector).fadeToggle(speed,callback);
$(selector).fadeTo(speed,opacity,callback);

6.上下滑动：
$(selector).slideDown(speed,callback);
$(selector).slideUp(speed,callback);
$(selector).slideToggle(speed,callback);

7.动画
$(selector).animate({params},speed,callback);
必需的 params 参数定义形成动画的 CSS 属性。
可选的 speed 参数规定效果的时长。它可以取以下值："slow"、"fast" 或毫秒。
可选的 callback 参数是动画完成后所执行的函数名称。
默认地，所有 HTML 元素都有一个静态位置，且无法移动。如需对位置进行操作，要记得首先把元素的 CSS position 属性设置为 relative、fixed 或 absolute！

8.停止动画
$(selector).stop(stopAll,goToEnd); //(false,false) —> (true,true)

Callback 、Chaining …

9.获得内容 - text()、html() 以及 val()
三个简单实用的用于 DOM 操作的 jQuery 方法：
text() - 设置或返回所选元素的文本内容
html() - 设置或返回所选元素的内容（包括 HTML 标记）
val() - 设置或返回表单字段的值
attr() 方法用于获取属性值。

10.添加新的 HTML 内容
我们将学习用于添加新内容的四个 jQuery 方法：
append() - 在被选元素的结尾插入内容
prepend() - 在被选元素的开头插入内容
after() - 在被选元素之后插入内容
before() - 在被选元素之前插入内容

11.删除
jQuery remove() 方法删除被选元素及其子元素。
jQuery empty() 方法删除被选元素的子元素。

12.jQuery 操作 CSS
jQuery 拥有若干进行 CSS 操作的方法。我们将学习下面这些：
addClass() - 向被选元素添加一个或多个类
removeClass() - 从被选元素删除一个或多个类
toggleClass() - 对被选元素进行添加/删除类的切换操作
css() - 设置或返回样式属性

13.jQuery 尺寸 方法
jQuery 提供多个处理尺寸的重要方法：
width()  //.width(200) 设置值
height()
innerWidth()
innerHeight()
outerWidth()   //true:包括内边距、边框和外边距
outerHeight()   //true:包括内边距、边框和外边距

14.向上遍历 DOM 树
这些 jQuery 方法很有用，它们用于向上遍历 DOM 树：
parent() 直接
parents() 所有
parentsUntil() 之间

15.向下遍历 DOM 树
下面是两个用于向下遍历 DOM 树的 jQuery 方法：
children() 直接
find() 所有后代 find() *

16.在 DOM 树中水平遍历
有许多有用的方法让我们在 DOM 树进行水平遍历：
siblings() 方法返回被选元素的所有同胞元素。
next() 方法返回被选元素的下一个同胞元素。
nextAll() 方法返回被选元素的所有跟随的同胞元素。
nextUntil() 方法返回介于两个给定参数之间的所有跟随的同胞元素
prev()
prevAll()
prevUntil()

17.过滤
first() 方法返回被选元素的首个元素。
last() 方法返回被选元素的最后一个元素。
eq() 方法返回被选元素中带有指定索引号的元素。// 0 1 2 …
filter() 方法允许您规定一个标准。不匹配这个标准的元素会被从集合中删除，匹配的元素会被返回。
not() 方法返回不匹配标准的所有元素。提示：not() 方法与 filter() 相反。

18. load() 方法完成后所要允许的回调函数。回调函数可以设置不同的参数：
responseTxt - 包含调用成功时的结果内容
statusTXT - 包含调用的状态
xhr - 包含 XMLHttpRequest 对象

19.
$.get(URL,callback);
$.get() 的第一个参数是我们希望请求的 URL（"demo_test.asp"）。第二个参数是回调函数。第一个回调参数存有被请求页面的内容，第二个回调参数存有请求的状态。

$.post(URL,data,callback);
$.post() 的第一个参数是我们希望请求的 URL ("demo_test_post.asp")。然后我们连同请求（name 和 city）一起发送数据。"demo_test_post.asp" 中的 ASP 脚本读取这些参数，对它们进行处理，然后返回结果。第三个参数是回调函数。第一个回调参数存有被请求页面的内容，而第二个参数存有请求的状态。

20.jQuery noConflict() 方法
如果你的 jQuery 代码块使用 $ 简写，并且您不愿意改变这个快捷方式，那么您可以把 $ 符号作为变量传递给 ready 方法。这样就可以在函数内使用 $ 符号了 - 而在函数外，依旧不得不使用 "jQuery"：
$.noConflict();
jQuery(document).ready(function($){
  $("button").click(function(){
    $("p").text("jQuery 仍在运行！");
  });
});

21.GET	POST
后退按钮/刷新	无害	数据会被重新提交（浏览器应该告知用户数据会被重新提交）。
书签	可收藏为书签	不可收藏为书签
缓存	能被缓存	不能缓存
编码类型	application/x-www-form-urlencoded	application/x-www-form-urlencoded 或 multipart/form-data。为二进制数据使用多重编码。
历史	参数保留在浏览器历史中。	参数不会保存在浏览器历史中。
对数据长度的限制	是的。当发送数据时，GET 方法向 URL 添加数据；URL 的长度是受限制的（URL 的最大长度是 2048 个字符）。	无限制。
对数据类型的限制	只允许 ASCII 字符。	没有限制。也允许二进制数据。
安全性
与 POST 相比，GET 的安全性较差，因为所发送的数据是 URL 的一部分。
在发送密码或其他敏感信息时绝不要使用 GET ！
POST 比 GET 更安全，因为参数不会被保存在浏览器历史或 web 服务器日志中。
可见性	数据在 URL 中对所有人都是可见的。	数据不会显示在 URL 中。

方法	描述
HEAD	与 GET 相同，但只返回 HTTP 报头，不返回文档主体。
PUT	上传指定的 URI 表示。
DELETE	删除指定资源。
OPTIONS	返回服务器支持的 HTTP 方法。
CONNECT	把请求连接转换到透明的 TCP/IP 通道。
