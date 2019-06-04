# JavaScript技术

## 一、 使用DHtml

**定义：使用JavaScript和CSS级联样式表操作HTML创造出各种动态视觉效果统称为DHTML**  
DHTML = CSS + Html + JS  
是一种浏览器端的动态网页技术  
DHTML对象模型\(DOM\)  
将HTML标记、属性和CSS样式都对象化  
可以动态存取HTML文档中的所有元素  
可以使用属性name或id来存取或标记对象  
改变元素内容或样式后浏览器中显示效果即时更新  
DHTML对象模型包括浏览器对象模型和Document对象模型

### Window对象的常用属性：

* **\* document 对象，**代表窗口中显示的HTML文档
* **frames 窗口**中框架对象的数组
* **\* history 对象**，代表浏览过窗口的历史记录
* **\* location 对象**，代表窗口文件地址，修改属性可以调入新的网页
* **\* status \(**defaultStatus\)窗口的状态栏信息
* **closed** 窗口是否关闭，关闭时该值为true
* **\* name** 窗口名称，用于标识该窗口对象
* **opener** 对象，是指打开当前窗口的window对象，如果当前窗口被用户打开，则它的值为null
* **parent** 对象，当前窗口是框架页时指的是包含该框架页的上一级框架窗口
* **top** 对象，当前窗口是框架页时指的是包含该框架页的最外部的框架窗口
* **self** 对象，指当前Window对象
* **window** 对象，指当前Window对象，同self

### Window对象的常用方法：

\(使用这些方法时，通常不加window也没区别；但在特定情况下必须加，如在内嵌页面用open\(\);\)

* **\* alert\(sMsg\);** 弹出简单对话框
* **confirm\(sMsg\);** 选择对话框
* **prompt\(sMsg, sInit\);** 弹出输入对话框
* **\* close\(\);** 关闭窗口
* **open\(sURL, sName, sFeatures, bReplace\);** 打开窗口
* **print\(\);** 打印窗口中网页的内容
* **focus\(\);** 设置焦点并执行 onfocus 事件的代码。
* **blur\(\);** 失去焦点并触发 onblur 事件。
* **moveBy\(iX, iY\);** 将窗口的位置移动指定 x 和 y 偏移值。
* **moveTo\(iX, iY\);** 将窗口左上角的屏幕位置移动到指定的 x 和 y 位置。
* **resizeBy\(iX, iY\);** 更改窗口的当前位置缩放指定的 x 和 y 偏移量。
* **resizeTo\(iWidth, iHeight\);** 将窗口的大小更改为指定的宽度和高度值。
* **scrollBy\(iX, iY\);** 将窗口滚动 x 和 y 偏移量。
* **scrollTo\(iX, iY\);** 将窗口滚动到指定的 x 和 y 偏移量。
* **\* setInterval\(vCode,iMilliSeconds,sLanguage\);** 每经过指定毫秒值后执行一段代码。
* **clearInterval\(iIntervalID\);** 取消 setInterval 方法的事件。
* **\* setTimeout\(vCode,iMilliSeconds,sLanguage\);** 经过指定毫秒值后执行一段代码。\(一次性\)
* **clearTimeout\(iTimeoutID\);** 取消 setTimeout 方法设置的超时事件。

### window主要功能：

#### 1.窗口的打开和关闭

* **window.open\(url,name,config\)** 打开新窗口；
* **url:**打开的超链接
* **name**:窗口的名称，返回新窗口对象
* **config**为窗口的配置参数：menubar 菜单条、toolbar 工具条、location 地址栏、directories 链接、
* **status** 状态栏、scrollbars 滚动条、resizeable 可调整大小\(以上参数值为yes或no，默认yes\)
* **width** 窗口宽，以像素为单位；height 窗口高，以像素为单位\(参数值为数值\)
* **\* window.close\(\)** 关闭窗口

#### 2.对话框

**简单对话框**：

* **alert\(str\)** 提示框，显示str字符串的内容；按\[确定\]关闭对话框
* **confirm\(str\)** 确认对话框，显示str字符串的内容；按\[确定\]按钮返回true，\[取消\]返回false
* **prompt\(str,value\)** 输入对话框，显示str的内容；按\[确定\]按钮返回输入值，\[取消\]关闭，返回null

**窗口对话框**：

* **showModalDialog\(url,arguments,config\)** IE4或更高版本支持该方法
* **showModelessDialog\(url,arguments,config\)** IE5或更高版本支持该方法           参数:url 打开链接，arguments 传入参数名，config 窗口配置参数
* **config** 外观配置参数：status、resizable、help 是否显示标题栏中的问号按钮、center 是否在桌面中间
* **dialogWidth** 对话框宽、dialogHeight 对话框高、\(上一行参数值为yes或no，这两行参数为多少像素\)
* **dialogTop** 对话框左上角的y坐标、dialogLeft 对话框左上角的x坐标

### 3.状态栏

* **window.status** 状态栏中的字符串信息允许进行设置或读取

#### 4.定时器

* **tID1=setInterval\(exp,time\)** 周期性执行exp代码；exp 代码块名，time 周期\(毫秒\)，返回启动的定时器
* **clearInterval\(tID1\)** 停止周期性的定时器
* **tID2=setTimeout\(exp,time\)** 一次性触发执行代码exp；返回已经启动的定时
* **clearTimeout\(tID2\)** 停止一次性触发的定时器

#### 5.内容滚动

* **window.scroll\(x,y\)** 滚动窗口到指定位置；单位为像素
* **window.scrollTo\(x,y\)** 同scroll方法
* **window.scrollBy\(ax,ay\)** 从当前位置开始，向右滚动ax像素，向下滚动ay像素

#### 6.调整窗口大小和位置

* **window.moveTo\(x,y\)** 移动窗口到指定位置；单位为像素
* **window.moveBy\(ax,ay\)** 向右移动ax像素，向下移动ay像素，参数为负数表示反方向移动
* **window.resizeTo\(width,height\)** 调整窗口大小为指定大小
* **window.resizeBy\(ax,ay\)** 放大或缩小窗口；参数为负数表示缩小

#### 7.Screen对象 

// 屏幕信息\(属于window的子对象；常用于获取屏幕的分辨率和色彩\)

* screen.width 屏幕分辨率的宽度，例如1024\*768分辨率下宽度为1024
* screen.height 类似上面，屏幕分辨率的高度
* screen.availWidth 屏幕中可用的宽 //排除 Windows 任务栏
* screen.availHeight 屏幕中可用的高 //排除 Windows 任务栏
* screen.colorDepth 屏幕的色彩数

#### 8.History对象

 // 窗口的访问历史信息\(属于window的子对象,常用于返回到已经访问过的页面\)

* history.length 历史记录数
* history.foward\(\) 向下一页
* history.back\(\) 返回上一页
* history.go\(0\) 刷新。括号里填"-1"就是返回上一页，填"1"就是下一页；其它数字类推

#### 9.Navigator对象 -浏览器和OS\(系统\)的信息 数组

#### 10.Location对象- 浏览器地址栏的信息 

**如： location.href="http://www.google.com/";**

* location.assign\(href\); 前往新地址，在历史记录中，用 Back 和 Forward 按钮可回到之前的地址
* location.replace\(href\); 替代当前文文件，在历史记录中也回不到之前的地址
* location.reload\(true\); 类似刷新，默认 false

 **location 各属性的用途**

* location.href 整个URl字符串\(在浏览器中就是完整的地址栏\),如: "http://www.test.com:8080/test/view.htm?id=209&dd=5\#cmt1323"
* location.protocol 返回scheme\(通信协议\)，如: "http:", "https:", "ftp:", "maito:" 等等\(后面带有冒号的\)
* location.host 主机部分\(域名+端口号\)，端口号是80时不显示，返回值如："www.test.com:8080", "www.test.com"
* location.port 端口部分\(字符串类型\)。如果采用默认的80端口\(即使添加了:80\)，那么返回值并不是默认的80而是空字符。
* location.pathname 路径部分\(就是文件地址\)，如: "/test/view.htm"
* location.search 查询\(参数\)部分。如: "?id=209&dd=5"
* location.hash 锚点，如: "\#cmt1323" 不包含参数的地址： location.protocol + '//' + location.host + location.pathname;

#### **11.**应用例子：窗口最大化

```javascript
window.moveTo(0,0); 
window.resizeTo(screen.availWidth,screen.availHeight);
// 或者 moveTo(0,0); resizeTo(screen.width, screen.height);
//采用screen对象的分辨率属性和resizeTo方法来动态确定窗口最大长度和宽度
```

## 二、 Dom 元素

### 处理 XML 文件的 DOM 元素属性：

* **&lt;element&gt;.childNodes** 返回目前元素所有子元素的数组
* **&lt;element&gt;.children** 返回目前元素所有子元素的数组\(这个在IE、火狐上也可以用\)
* **&lt;element&gt;.firstChild** 返回目前元素的第一个子元素
* **&lt;element&gt;.lastChild** 返回目前元素的最后一个子元素
* **&lt;element&gt;.nodeValue** 指定表示元素值的读/写属性
* **&lt;element&gt;.parentNode** 返回元素的父节点
* **&lt;element&gt;.previousSibling** 返回紧邻目前元素之前的元素
* **&lt;element&gt;.nextSibling** 返回目前元素的后面的元素
* **&lt;element&gt;.tagName** 返回目前元素的标签名\(大写\)

### 沿 XML 文件来回移动的 DOM 元素方法：

* **document.getElementById\(id\)** 取得有指定唯一ID属性值文件中的元素
* **document.getElementsByTagName\(name\)** 返回目前元素中有指定标签名的子元素的数组
* **&lt;element&gt;.hasChildNodes\(\)** 返回布尔值，表示元素是否有子元素
* **&lt;element&gt;.getAttribute\(name\)** 返回元素的属性值，属性由name指定

### 动态建立内容时所用的 W3C DOM 属性和方法：

* **document.createElement\(tagName\)** 建立由tagName指定的元素。比如以"div"作为参数，则生成一个div元素。
* **document.createTextNode\(text\)** 建立一个包含静态文字的节点。
* **&lt;element&gt;.appendChild\(childNode\)** 将指定节点增加到目前元素的子节点中。例如：select中增加option子节点
* **&lt;element&gt;.getAttribute\(name\)** 取得元素中的name属性的值
* **&lt;element&gt;.setAttribute\(name,value\)** 设定元素中的name属性的值
* **&lt;element&gt;.insertBefore\(Node1,Node2\)** 将节点Node1作为目前元素的子节点插到Node2元素前面。
* **&lt;element&gt;.removeAttribute\(name\)** 从元素中删除属性name
* **&lt;element&gt;.removeChild\(childNode\)** 从元素中删除子元素childNode
* **&lt;element&gt;.replaceChild\(newN,oldN\)** 将节点oldN替换为节点newN
* **&lt;element&gt;.hasChildnodes\(\)** 返回布尔值，表示元素是否有子元素

注意：文字实际上是父元素的一个子节点，所以可以使用firstChild属性来存取元素的文字节点。  
有了文字节点后，可以参考文字节点的nodeValue属性来得到文字。读取XML时，须考虑它的空格和换行符也作为子节点。

### 处理 HTML DOM 元素中3个常用的属性: nodeName、 nodeValue 以及 nodeType

#### nodeName:

 属性\(只读\)含有某个节点的名称:  
元素节点的 nodeName 是标签名称\(永远是大写的\)  
属性节点的 nodeName 是属性名称  
文本节点的 nodeName 永远是 \#text  
文档节点的 nodeName 永远是 \#document

#### nodeValue / data

对于文本节点，nodeValue 属性包含文本。可增删改  
对于属性节点，nodeValue 属性包含属性值。  
nodeValue 属性对于文档节点和元素节点是不可用的。会返回 null  
data同样是文本的内容,这个属性下同样可以增删改。对于文档节点和元素节点不可用,返回 undefine

#### nodeType 属性返回节点的类型。

节点类型是：

```javascript
//元素类型                   节点类型
ELEMENT_NODE :               1 // 元素
ATTRIBUTE_NODE :             2 // 属性
TEXT_NODE :                  3 // 文本
CDATA_SECTION_NODE :         4
ENTITY_REFERENCE_NODE :      5
ENTITY_NODE :                6
PROCESSING_INSTRUCTION_NODE : 7
COMMENT_NODE :                8 // 注释
DOCUMENT_NODE :               9 // 文档,即 document
DOCUMENT_TYPE_NODE :         10
DOCUMENT_FRAGMENT_NODE :     11
NOTATION_NODE :              12
```

注： 对于属性节点，可使用 “attr.nodeName”和“attr.nodeValue”来查看或者赋值, 也可以使用“attr.name”和“attr.value”。只是, attr.nodeValue 会返回真实类型,如 bool,number,string,object 等； 而 attr.value 全是 string 类型\(null 则返回"null"\).**判断是否 dom 元素**，一些特殊节点只有nodeName，没有tagName，比如document的nodeName为“\#document”，tagName为空值。

## 三、跨浏览器

### 1.浏览器判断：

```javascript
//如果是火狐等浏览器则为“true”
var isNav = (navigator.appName.indexOf("Netscape") != -1);
//如果是IE浏览器则为“true”
var isIE = (navigator.appName.indexOf("Microsoft") != -1); 
// navigator.appName == "Microsoft Internet Explorer"
var isIE = (navigator.appVersion.indexOf("MSIE") != -1);
//判断IE6
var isIE6 = (navigator.userAgent && navigator.userAgent.split(";")[1].toLowerCase().indexOf("msie 6.0")!="-1");
//如果是Opera浏览器则为“true”
var isOpera = (navigator.userAgent.indexOf("Opera") != -1);
//浏览器运行的平台，是 windows 则返回 true
var isWin = (navigator.appVersion.toLowerCase().indexOf("win") != -1);
```

### 2.event 事件

在 IE4+ 和 Firefox下的 event

```javascript
function doEventThing(event)
{
//获取不同浏览器的 event
event = event || window.event; // window.event for IE; 参数event for firefox
//获取不同浏览器的键盘输入记录
var currentKey = event.keyCode || event.charCode; // keyCode 目前兼容了
//获取不同浏览器的事件源
var eventSource = event.target || event.srcElement; // srcElement for IE; target for firefox
var target = event.relatedTarget || event.toElement; // 将会去到的元素,像 onmouseout 会触发
//屏蔽Form提交事件
//if ( event.returnValue ) event.returnValue = false; // for IE
//if ( event.preventDefault ) event.preventDefault(); // for firefox
( e.preventDefault ) ? (e.preventDefault()) : (e.returnValue = false);
//添加事件
if ( event.attachEvent ) {
event.attachEvent('onclick', func ); // for IE; 需要加上“on”,如 onmouseover
} else if ( event.addEventListener ) {
event.addEventListener('clcik', func, false); // for firefox; 不需要加上“on”,直接写“click”
}
//改变事件; 但上面的绑定事件方法并不改变原有的onclick事件，而是添加事件
event.onclick = func;
}
//Firefox 下必须手动输入参数,调用时如: <input type="button" onclick="doEventThing(event);"/>
```

### 3. firefox 的 click\(\) 事件

由于 firefox 不支持 click\(\) 事件,代替方式：

```javascript
// 获取需要触发 onclick() 的元素
var element = document.getElementsByTagName('a')[0];
// For IE
if ( document.all ) {
element.click();
// FOR DOM2
} else if ( document.createEvent ) {
var ev = document.createEvent('MouseEvents'); //'MouseEvents' 改成 'HTMLEvents' 的话,firfox2不通过
ev.initEvent('click', false, true);
element.dispatchEvent(ev);
}
```

### 4. 跨浏览器技巧：

**1\) IE不能用setAttribute设定class属性。**

解决方法1: 同时使用 setAttribute\("class","newClassName"\) 和 setAttribute\("className","newClassName"\)  
解决方法2: &lt;element&gt;.className = "newClassName"

#### 2\) IE中不能使用setAttribute设定style属性。

即 &lt;element&gt;.setAttribute\("style","fontweight:bold;"\) 不相容。  
解决方法：使用 &lt;element&gt;.style.cssText = "fontweight:bold;"

#### 3\) 使用appendChild将&lt;tr&gt;元素直接增加到&lt;table&gt;中，则在IE中这一行并不出现，但其它浏览器却会出现。

解决方法：在&lt;table&gt;下增加&lt;tbody&gt;元素，再添加&lt;tr&gt;

#### 4\) IE不能直接添加按钮处理事件。如：addButton.setAttribute\("onclick","addEmployee\('unid'\);"\);不适用。

解决方法：addButton.onclick = function\(\) { addEmployee\('unid'\); };//用匿名函数调用addEmployee\(\)函数。  
此外,onmouseover,onmouseout 等事件也要使用此方法。

#### 5\) firefox 不支持 document.all

解决方法: 用 document.getElementsByTagName\("\*"\) 替代,可以得到得到所有元素的集合

#### 6\) 设置元素的id

同时使用 .id 和 setAttribute 来设置  
var div = document.createElement\('div'\);  
div.id="btc";  
div.setAttribute\("id","btc"\);

### 5.Firefox注册innerText写法

```javascript
if ( (navigator.appName.indexOf("Netscape") != -1) )
{
//注册 Getter
HTMLElement.prototype.__defineGetter__("innerText", function(){
var anyString = "";
var childS = this.childNodes;
for ( var i=0; i < childS.length; i++ ) {
if ( childS[i].nodeType == 1 )
anyString += childS[i].tagName == "BR" ? '\n' : childS[i].innerText;
else if(childS[i].nodeType == 3 ) {
anyString += childS[i].nodeValue;
}
}
return anyString;
});
//注册 Setter
HTMLElement.prototype.__defineSetter__("innerText",
function ( sText ) { this.textContent = sText; }
);
}
//在非IE浏览器中使用 textContent 代替 innerText
```

### 6.长度：FireFox长度必须加“px”，IE无所谓

解决方法：统一使用 obj.style.height = imgObj.height + "px";

### 7.父控件下的子控件：IE是“children”，FireFox是“childNodes”

### 8.XmlHttp

在IE中，XmlHttp.send\(content\)方法的content可以为空，而firefox则不能为空，应该用send\(" "\)，否则会出现411错误

### 9.event.x 与 event.y 问题

问题： 在IE中，event 对象有x,y属性，FF中没有  
解决方法：  
在FF中，与 event.x 等效的是 event.pageX ，但event.pageX IE中没有  
故采用 event.clientX 代替 event.x ，在IE中也有这个变量  
event.clientX 与 event.pageX 有微妙的差别，就是滚动条  
要完全一样，可以这样：  
mX = event.x ? event.x : event.pageX;

### 10.禁止选取网页内容

问题：FF需要用CSS禁止，IE用JS禁止  
解决方法：  
IE: obj.onselectstart = function\(\) {return false;}  
FF: -moz-user-select:none;

### 11.各种浏览器的特征及其userAgent。

#### IE**：**

只有IE支持创建ActiveX控件，因此她有一个其他浏览器没有的东西，就是 window.ActiveXObject 函数。  
IE各个版本典型的userAgent如下\(其中，版本号是MSIE之后的数字\)：  
Mozilla/4.0 \(compatible; MSIE 8.0; Windows NT 6.0\)  
Mozilla/4.0 \(compatible; MSIE 7.0; Windows NT 5.2\)  
Mozilla/4.0 \(compatible; MSIE 6.0; Windows NT 5.1\)  
Mozilla/4.0 \(compatible; MSIE 5.0; Windows NT\)

#### Firefox

Firefox中的DOM元素都有一个getBoxObjectFor函数，用来获取该DOM元素的位置和大小\(IE对应的中是getBoundingClientRect函数\)。这是Firefox独有的，判断它即可知道是当前浏览器是Firefox。  
Firefox几个版本的userAgent大致如下\(其中，版本号是Firefox之后的数字\)：  
Mozilla/5.0 \(Windows; U; Windows NT 5.2\) Gecko/2008070208 Firefox/3.0.1  
Mozilla/5.0 \(Windows; U; Windows NT 5.1\) Gecko/20070309 Firefox/2.0.0.3  
Mozilla/5.0 \(Windows; U; Windows NT 5.1\) Gecko/20070803 Firefox/1.5.0.12

#### Opera

Opera提供了专门的浏览器标志，就是 window.opera 属性。  
Opera典型的userAgent如下\(其中，版本号是Opera之后的数字\)：  
Opera/9.27 \(Windows NT 5.2; U; zh-cn\)  
Opera/8.0 \(Macintosh; PPC Mac OS X; U; en\)  
Mozilla/5.0 \(Macintosh; PPC Mac OS X; U; en\) Opera 8.0

#### Safari

Safari浏览器中有一个其他浏览器没有的openDatabase函数，可做为判断Safari的标志。  
Safari典型的userAgent如下\(其版本号是Version之后的数字\)：  
Mozilla/5.0 \(Windows; U; Windows NT 5.2\) AppleWebKit/525.13 \(KHTML, like Gecko\) Version/3.1 Safari/525.13  
Mozilla/5.0 \(iPhone; U; CPU like Mac OS X\) AppleWebKit/420.1 \(KHTML, like Gecko\) Version/3.0 Mobile/4A93 Safari/419.3

#### Chrome

Chrome有一个 window.MessageEvent 函数，但Firefox也有。不过，好在Chrome并没有Firefox的getBoxObjectFor函数，根据这个条件还是可以准确判断出Chrome浏览器的。  
目前，Chrome的userAgent是\(其中，版本号在Chrome之后的数字\)：  
Mozilla/5.0 \(Windows; U; Windows NT 5.2\) AppleWebKit/525.13 \(KHTML, like Gecko\) Chrome/0.2.149.27 Safari/525.13

#### 下面是判断浏览器的代码：

```javascript
var Sys = {};
var ua = navigator.userAgent.toLowerCase();
if (window.ActiveXObject)
Sys.ie = ua.match(/msie ([\d.]+)/i)[1];
else if (document.getBoxObjectFor) // 火狐判断出错
Sys.firefox = ua.match(/firefox\/([\d.]+)/i)[1];
else if (window.opera)
Sys.opera = ua.match(/opera.([\d.]+)/i)[1];
else if (window.MessageEvent)
Sys.chrome = ua.match(/chrome\/([\d.]+)/i)[1];
else if (window.openDatabase)
Sys.safari = ua.match(/version\/([\d.]+)/i)[1];
//以下进行测试
if(Sys.ie) alert('IE: '+Sys.ie);
if(Sys.firefox) alert('Firefox: '+Sys.firefox);
if(Sys.chrome) alert('Chrome: '+Sys.chrome);
if(Sys.opera) alert('Opera: '+Sys.opera);
if(Sys.safari) alert('Safari: '+Sys.safari);
```

## 四、 摘录：

### 1. 省略对象名称

```javascript
//用 with() 命令。
 document.write(".....<br/>");
document.write(".....<br/>");
//可省略写为：
with (document) {
write(".....<br/>");
write(".....<br/>");
} //把相同的 document 省略掉。
//省略对象名称，变量。
//如： document.myForm.myText.value;
//可省略写为： f = document.myForm; f.myText.value;
```

### 2.页面调试

javascript 加入如下语句，出错时会提示  
注意： chrome、opera 和 safari 等浏览器不支持 window.onerror 事件\(w3c标准没有此事件\),需另外捕获出错信息

```javascript
<script type="text/javascript">
/**
* 这是出错调试代码
* 当页面发生错误时，提示错误信息
* @param msg 出错信息
* @param url 出错文件的地址
* @param sLine 发生错误的行
* @return true 让出错时不显示出错图标
*/
window.onerror = function ( msg, url, sLine ) {
var hostUrl = window.location.href;
// 判断网址,测试时可以提示出错信息;正式发布时不提示
if ( hostUrl.indexOf("http://localhost") === 0 || hostUrl.indexOf("http://127.0.0.1") === 0 ||
hostUrl.indexOf("http://192.168.") === 0 || hostUrl.indexOf("file://") === 0 )
{
var errorMsg = "当前页面的脚本发生错误.\n\n";
errorMsg += "错误: " + msg + "\n";
errorMsg += "URL: " + url + "\n";
errorMsg += "行: " + sLine + "\n\n";
errorMsg += "点击“确定”消去此错误，“取消”保留此错误。\n\n";
return window.confirm( errorMsg );
}
// 返回true,会消去 IE下那个恼人的“网页上有错误”的提示
return true;
};
</script>
```

### 3.把数值变成 奇 \ 偶数\(利用位运算\)

```javascript
n = n | 1 ; //一定得到奇数。如果原本是偶数则加一。
n = (n >> 1) <<1; //一定得到偶数。如果原本是奇数则减一。
n = n ^ 1; //奇偶互换。对偶数加一，对奇数减一。
```

### 4.取出数值的整数部分\(取整\)。

```javascript
// 以下第一种方法不受浏览器和版本的影响，后两种受版本影响。
n = ( n > 0 ) ? Math.floor(n) : Math.ceil(n);
n = Number ( (String(n).split("."))[0]);
n = parseInt(n,10);
// 下面做法更简便高效,用位运算来做(右移0位,或者两次取反),且非数值型的值会转成0
alert(5>>0); alert(~~5); // 值为 5
alert(5.55>>0); alert(~~5.55); // 值为 5
alert(-98.4>>0); alert(~~-98.4); // 值为 -98
alert('absd'>>0); alert(~~'absd'); // 值为 0
alert(null>>0); alert(~~null); // 值为 0
alert('34.5'>>0); alert(~~'34.5'); // 值为 34
```

### 5.取出数值的小数部分。

```javascript
//须先检查小数点是否存在。但有时会发生运算误差。
n = Math.abs(n); if(n>0) n = n - Math.floor(n); else n = 0;
n = parseInt(n,10) - parseFloat(n);
if((""+n).indexOf(".") > -1) n = Number("0."+(String(n).split("."))[1]); else n = 0;
```

### 6.在任意位置插入一行js\(单行程序\)：

```javascript
<script type="text/javascript">alert("中断一下");</script>
<input type="button" onclick="javascript:formName.DataName.value='';formName.DataName.focus();" />
```

7.设置焦点：  
//document.all\["DateID"\].onfocus;  
document.all\["DateID"\].focus\(\);  
formName.DataName.focus\(\);

8.默认参数：  
function show\(\) {  
alert\( arguments\[0\] \);  
}  
这个函数会alert出第一个参数，如调用时： show\("haha"\)，则alert\("haha"\);

9.禁止 confirm 與 alert  
window.confirm = function\(str\){return true;};  
window.alert = function\(str\){};

10.获取下拉菜单的内容  
&lt;select name="seleName" &gt;  
&lt;option value="value1"&gt;Text&lt;/option&gt;  
&lt;/select&gt;  
获取选中的下拉菜单的内容：  
var seleElement = document.formName.seleName;  
var optionText = seleElement.options\[seleElement.selectedIndex\].text;

11.设置默认值:  
edittype = edittype \|\| "text"; //edittype预设为 text  
上面一句: 如果 edittype 之前有值,则取之前的值; 之前没有值,则取默认值

12.数值的截取:  
numObj.toFixed\(\[fractionDigits\]\)  
//numObj:必选项。一个 Number 对象。  
//fractionDigits:可选项。小数点后的数字位数。其值必须在 0 – 20 之间，包括 0 和 20。 预设为0  
toFixed 方法返回一个以定点表示法表示的数字的字符串形式。对数值进行四舍五入截取到指定位数的小数  
如: 55.3654.toFixed\(2\) //返回55.37

13.IE上的关闭窗口时不提示  
window.opener = null; // 关闭IE6不提示  
window.open\("","\_self"\); // 关闭IE7不提示  
//关闭窗口  
window.close\(\);

14.刷新页面的几种方法：  
history.go\(0\);  
window.navigate\(location\);  
document.URL = location.href;  
document.execCommand\('Refresh'\); //火狐不能用  
location.reload\(\);  
location = location;  
location.href = location.href;  
location.assign\(location\);  
location.replace\(location\);

15.页面跳转：  
location.href = "yourURL"  
window.location = 'url'  
window.location.href = "yourURL"  
window.navigate\("top.jsp"\);  
self.location = 'top.htm' //令所在框架页面跳转，大框架不变  
top.location = 'xx.jsp'; //在框架內令整個页面跳转

16.页面跳转/刷新 的注意：  
需要先执行其他代码，然后再页面跳转或者刷新。因为页面跳转或者刷新后不再执行下面的代码。  
如：alert\('请先登录'\); window.location.href = 'index.jsp';

17.改变标题\(即改变&lt;title&gt;标签的内容\)  
document.title = "title\_content";

18.if 判断对象是否存在  
一般可以用 if 判断对象是否存在,但直接写“ if\(对象名\){...} ”判断时,如果对象不存在则浏览器会抛异常。  
这里建议用“ if\(window\['对象名'\]\){...} ”的写法来判断  
当确认对象已经存在时,用“对象名.变量名”跟“对象名\['变量名'\]”没什么区别。  
如： var c = new Object\(\); // 假如这是写在另一个js文件里的变量,下面用的时候需要判断这对象是否存在  
if \(c\) {alert\('c存在'\);} // 如果这对象确实存在，则没有问题。但对象不存在时会抛异常  
if \(window\['c'\]\){alert\('c存在'\);}; if \(window.c\){alert\('c存在'\);} // 推荐用这两种写法之一,不管对象是否存在,都不会抛异常,且存在时可正常使用。

  
五、JavaScript 技巧  
1.获取表单的内容  
&lt;HTML&gt;  
&lt;HEAD&gt;  
&lt;SCRIPT LANGUAGE="JavaScript"&gt;  
&lt;!--  
function aa\(\){  
//var value=document.all\("td1"\).value; //.innerHTML  
var value=document.getElementById\("td1"\).value;//上句也可行  
document.all\("ta"\).value=value;  
}  
//--&gt;  
&lt;/SCRIPT&gt;  
&lt;/HEAD&gt;  
&lt;BODY&gt;  
&lt;input id="td1" name="haha" type="text" onkeydown="if\(13==event.keyCode\){aa\(\);return false;}"/&gt;&lt;br/&gt;  
&lt;INPUT TYPE="button" NAME="" value="引用" onclick="aa\(\)"&gt;&lt;br/&gt;  
&lt;TEXTAREA id="ta" ROWS="15" COLS="20"&gt;&lt;/TEXTAREA&gt;  
&lt;/BODY&gt;  
&lt;/HTML&gt;

2. IE3.0 和 NN2.0\(Netscape Navigator\)上能同时运作的程序  
为照顾不同的浏览器和版本，只好多作几次判断。看程序中的几个 if 实现的是同一功能就明白。  
&lt;html&gt;  
&lt;head&gt;  
&lt;title&gt;写能同时在IE和NN上运行的程序&lt;/title&gt;  
&lt;script language="JavaScript"&gt;  
&lt;!--  
x = 0;  
function moveLayer\(\) {  
x = x + 2;  
if\(document.all\) {document.all\["myLay"\].style.left = x;} //IE4以上版本可用，IE4之前和NN上都没有 all  
if\(document.layers\) {document.layers\["myLay"\].left = x;} //仅NN4上运行，NN4外没有layers对象  
/\* 下面这句仅NN6以后版本可用。  
因为document.getElementById\(\)在IE5.x上有，所以需 " !document.all " \*/  
if\(!document.all && document.getElementById\) {document.getElementById\("myLay"\).style.left = x;}  
}  
// --&gt;  
&lt;/script&gt;  
&lt;/head&gt;  
&lt;body bgcolor = "white" onLoad="setInterval\('moveLayer\(\)',1000\)"&gt;  
&lt;div id="myLay" style="position:absolute;left:0px"&gt; &lt;img src="btn1.gif"&gt;&lt;/div&gt;  
&lt;/body&gt;  
&lt;/html&gt;

3. 读取 Behavior 文档 \(任意标签都可触发 onclick 事件\) \(IE5.0以上可用\)  
//在 html 文件上写：  
&lt;html&gt;  
&lt;head&gt;  
&lt;title&gt;读取 Behavior 文件&lt;/title&gt;  
&lt;style type="text/css"&gt;  
&lt;!--  
div { behavior:url\(a.htc\); }  
--&gt;  
&lt;/style&gt;  
&lt;script language="JavaScript"&gt;  
&lt;!--  
function testA\(\) { alert\("haha"\); } //&lt;a&gt;标签的 onclick事件  
function check\(\) { //获取 id 和 class 名称  
alert\("id = "+document.all\["myObj"\].id+"; className="+document.all\["myObj"\].className\);  
}  
// --&gt;  
&lt;/script&gt;  
&lt;/head&gt;  
&lt;body bgcolor = "white"&gt;&lt;center&gt;  
&lt;div&gt;点击文字&lt;/div&gt;&lt;br/&gt;&lt;br/&gt;  
&lt;a href="JavaScript:testA\(\)"&gt;sample&lt;/a&gt;&lt;br/&gt;&lt;br/&gt;&lt;br/&gt;  
&lt;input id="myObj" class="mz" type=button value="test" onclick="check\(\)" /&gt;  
&lt;/center&gt;&lt;/body&gt;  
&lt;/html&gt;

//在此 html 文件的同一目录下的 a.htc 文件里写：  
&lt;script language="JavaScript"&gt;  
&lt;!--  
attachEvent\("onclick",msg\);  
function msg\(\) { alert\("oh!"\);}  
// --&gt;  
&lt;/script&gt;

4.定时器，每隔一段时间进行处理\(IE3.0以上，NN2.0以上可用\)  
&lt;html&gt;  
&lt;head&gt;  
&lt;title&gt;定时器&lt;/title&gt;  
&lt;script language="JavaScript"&gt;  
&lt;!--  
var timerId;  
var n = 0;  
function timerUpdate\(\){  
window.document.myForm.result.value = n++ ;  
//这是个一次性触发的方法，这里以反复调用来实现周期性触发  
timerId = setTimeout\("timerUpdate\(\)",100\); //第一个参数是要执行的函数,也可以直接写匿名函数而不用字符串  
}  
function timerStart\(\) {  
//防止连续多次点击，导致计数器速度迭加  
document.getElementById\("StartCount"\).onclick = "";  
setTimeout\("timerUpdate\(\)",1\);  
}  
function timerEnd\(\) {  
clearTimeout\(timerId\);  
//这两句的效果一样。  
//clearInterval\(timerId\);  
//还原 "StartTime"按钮 的点击能力  
document.getElementById\("StartCount"\).onclick = timerStart;  
}  
// --&gt;  
&lt;/script&gt;  
&lt;/head&gt;  
&lt;body&gt;  
&lt;form name="myForm"&gt;  
&lt;input type="text" name="result"/&gt;&lt;br/&gt;&lt;br/&gt;  
&lt;/form&gt;  
&lt;input type="button" id="StartCount" value="StartTime" onclick="timerStart\(\)"/&gt;  
&lt;input type="button" value="EndTime" onclick="timerEnd\(\)"/&gt;  
&lt;/body&gt;  
&lt;/html&gt;

5.根据 javaScript 的开闭状态来显示网页\(适用IE3.0和NN2.0以上版本\)  
以 &lt;meta&gt; 配合 location.href 来实现。  
下面的 &lt;meta&gt; 里的content的5表示当javascript关闭时，5秒后跳转到closeJavaScript.html 页面。  
location.href="openJavaScript.html"; 表示当javascript可用时，跳转到 openJavaScript.html 页面。  
在 html 里加入"&lt;noscript&gt;您使用的浏览器不支持或者禁止了Javascript&lt;/noscript&gt;"则在本页面提示。

&lt;meta http-equiv="refresh" content="5; url=closeJavaScript.html"&gt;  
&lt;script language="JavaScript"&gt;  
&lt;!--  
location.href="openJavaScript.html";  
// --&gt;  
&lt;/script&gt;

7.淡入/淡出效果\(背景色适用IE3.0和NN2.0以上版本，文字色适用IE4以上版本\)  
&lt;body bgcolor="black" onLoad="newCount\('bgColor'\); fade\('0123456789ABCDEF'\)"&gt;  
&lt;script language="JavaScript"&gt;  
var count = 0 ;  
var obj = null ;  
function fade\(str\){  
c = str.charAt\(count++\);  
if \(obj=='bgColor'\) {document.bgColor = "\#"+c+c+c+c+c+c+c+c;} //改变背景颜色，颜色码8位  
if \(obj=='word'\) {document.all\["strId"\].style.color = "\#"+c+c+"0000";} //改变文字颜色，颜色码6位  
if\(count &lt; str.length\) setTimeout\("fade\('"+str+"'\)",250\);  
}  
function newCount\(object\){ count = 0 ; obj = object ; }  
&lt;/script&gt;  
&lt;input type="button" value="toWhite" onclick="newCount\('bgColor'\); fade\('0123456789ABCDEF'\)"/&gt;  
&lt;input type="button" value="toBlack" onclick="newCount\('bgColor'\); fade\('fedcba9876543210'\)"/&gt;&lt;br/&gt;&lt;br/&gt;  
&lt;span id="strId" onMouseover="newCount\('word'\); fade\('fedcba9876543210'\)"&gt;点击淡入淡出的文字&lt;/span&gt;  
&lt;/body&gt;

8.窗口的振动效果\(适用IE4.0和NN4.0以上版本\)  
&lt;script language="JavaScript"&gt;  
//指定窗口的错位。  
x = new Array\( 10, 3, -6, 8, -10, -7, 5, -3, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0\);  
y = new Array\(-12, 6, -3, 10, -9, -2, 8, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0\);  
count = 0;  
function purupuruWin\(\) {  
if\(x\[count\] != 0\) moveBy\(x\[count\], y\[count\]\); //窗口的振动  
count++;  
if\(count &gt;= x.length \)count = 0;  
setTimeout\("purupuruWin\(\)",100\);  
}  
&lt;/script&gt;  
&lt;input type="button" name="" value="StartPuru" onclick="purupuruWin\(\)"&gt;

9.检查电子邮件地址是否正确\(适用IE4.0和NN3.0以上版本\)  
&lt;script language="JavaScript"&gt;  
function checkMailAddr\(dstText\){  
var data = dstText.match\(/^\S+@\S+\.\S+$/\); //检查是否邮件的表达式  
if\(!data \|\| !dstText \) alert\('电子邮件地址不正确！'\); else alert\('电子邮件地址正确！'\);  
}  
&lt;/script&gt;  
&lt;form&gt;  
电子邮件：&lt;input type="text" name="address" /&gt;  
&lt;input type="button" value="check" onclick="checkMailAddr\(this.form.address.value\)"/&gt;  
&lt;/form&gt;

10. cookie 的使用。显示访问次数。\(适用IE3.0和NN2.0以上版本\)  
&lt;script language="JavaScript"&gt;  
if \( !navigator.cookieEnabled \) alert\("can not use cookie"\);  
//在 cookie 中存储访问次数。  
function setCount\(n\){  
var theDay = 30;  
var setDay = new Date\(\);  
setDay.setTime\(setDay.getTime\(\)+\(theDay\*1000\*60\*60\*24\)\);  
document.cookie = "count=" + n + ";expires=" + setDay.toGMTString\(\);  
}  
function getCount\(\) {  
var theName = "count=";  
var theCookie = document.cookie + ";" ;  
var start = theCookie.indexOf\(theName\); //没有cookie时返回“-1”  
if \(start != -1\) { //这是对第2次以后的访问的处理  
var end = theCookie.indexOf\(";",start\);  
var count = eval\(unescape\(theCookie.substring\(start+theName.length,end\)\)\);  
document.write\("这是第 "+count+" 次访问本页面"\);  
setCount\(count+1\);  
} else { //这是对第1次访问的处理  
document.write\("这是第1次访问本页面"\);  
setCount\(2\);  
}  
}  
getCount\(\);  
&lt;/script&gt;

11.简单的预防二次提交 \(适用IE3.0和NN3.0以上版本\)  
&lt;script language="JavaScript"&gt;  
var flag = false;  
function send\(\) {  
if \(flag\) { alert\("提交完毕！"\); return false; }  
flag = true ; return true;  
}  
function send2\(form\) {  
if \( !flag \){ form.submit\(\); }  
}  
&lt;/script&gt;  
&lt;form name="myForm" method="post" action="send.html" enctype="text/plain" onSubmit="return send\(\)"&gt;  
&lt;input type="submit" value="提交" /&gt;  
&lt;!-- onclick里的函数要用双引号括起来，form表单的名称不能加引号，字符则须用单引号括起来--&gt;  
&lt;input type="button" value="按钮" onclick="send2\(myform\);" &gt;  
&lt;/form&gt;

  
12.解决中文乱码问题。  
用以下三个方法进行转码就行了：  
escape\('你好'\) == %u4F60%u597D //转成 Unicode 编码  
encodeURI\('你好/p'\) == %E4%BD%A0%E5%A5%BD/p //转换为UTF-8；URL需要传递中文时使用  
encodeURIComponent\('你好/p'\) == %E4%BD%A0%E5%A5%BD%2Fp

三种方法都能对字符进行过滤。后两者是将字符串转换为UTF-8的方式。  
escape\(\) 不会编码的字符有69个: \* + - . / @ \_ 0-9 a-z A-Z  
所有空格、标点符号以及任何其它非 ASCII 字符都用 %xx 编码替换  
其中 xx 表示该字符的16进制数。例如，空格返回为“%20”。  
\(字符值大于 255 的字符以 %uxxxx 格式存储。\)  
注意：escape 方法不能用来对“统一资源标识符”\(URI\) 进行编码。  
unescape\(\) 从用 escape\(\) 编码的 String 对象中返回已解码的字符串。同样不能用于 URI  
encodeURI\(\)返回编码为有效的 URI 字符串。  
不会编码的字符有82个: ! \# $ & ' \( \) \* + , - . / : ; = ? @ \_ ~ 0-9 a-z A-Z  
此方法返回一个已编码的 URI。将编码结果传递给 decodeURI\(\)，则返回初始的字符串。  
decodeURI\(\) 不对下列字符进行编码： : / ; ?  
encodeURIComponent\(\) 返回编码为 URI 的有效组件的字符串。  
不会编码的字符有71个: ! ' \( \) \* - . \_ ~ 0-9 a-z A-Z  
注意，它会编译“/”，所以不能包含路径，否则无效。  
decodeURIComponent\(\) 将编码结果解码回初始字符串。

//把任意编码转成 java 的 ascii 编码\(Unicode native2ascii \)  
//注意：html的ascii码是“%”开头的，但java的却是“\”开头，所以这里替换了  
function change1\( str \) {  
var tem = "";  
for\( var j = 0; j &lt; str.length; j=j+1 \) {  
if \( escape\(str.charAt\(j\)\).length &gt;= 6\) {  
tem += escape\(str.charAt\(j\)\).replace\("%", "\\"\);  
} else { tem += str.charAt\(j\); }  
}  
return tem;  
}

// ascii2nactive 解码  
function change2\( str \) {  
for\( var j = str.length/3; j &gt; 0; j=j-1 \) {  
str = str.replace\("\\", "%"\);  
}  
return unescape\(str\);  
}

12.1 &lt;a&gt; \(A标签\) 传参时的中文乱码解决方案  
利用js的escape函数,转码即可  
&lt;script language="javascript" type="text/javascript"&gt;  
/\*\*  
\* 打开小视窗  
\* @param url 需要打开视窗的网址  
\* @param name 视窗名称  
\* @param param 视窗显示的参数  
\*/  
function openWin\(url, name, param\) {  
var newurl,arrurl;  
if \( typeof\(url\) === "undefined" \|\| url === "" \) {  
return ;  
}  
else {  
//没有参数时  
if \( url.indexOf\("?"\) == -1 \) {  
newurl = url;  
}  
//分解参数,并逐个转码  
else {  
newurl = url.substring\(0,url.indexOf\("?"\)+1\);  
arrurl = url.substring\(url.indexOf\("?"\)+1\).split\("&"\);  
for \( var i =0; i&lt;arrurl.length; i++ \) {  
newurl += arrurl\[i\].split\("="\)\[0\] + "=" + escape\(arrurl\[i\].split\("="\)\[1\]\) + "&";  
}  
newurl = newurl.substring\(0,newurl.length-1\);  
}  
}  
window.open\(newurl, name, param\);  
}  
&lt;/script&gt;

//使用如下 \(下面第二句会更好,测试火狐时第一句会延迟或者没反应\)  
&lt;a href="\#" onclick="openWin\('test.html','test','width=300,height=400'\);"&gt;Links&lt;/a&gt;  
&lt;a href="javascript:openWin\('test.html','test','width=300,height=400'\);"&gt;Links&lt;/a&gt;

A标签的 href="\#" 时，IE浏览器会跳转到页面顶部, 解决方法是把“&lt;A href="\#"&gt;”改写成“&lt;A href="javascript:void\(0\);"&gt;”或者“&lt;A href="javascript:;"&gt;”  
A标签的 onclick 事件，如果返回 false, 可以阻止页面跳转,如: &lt;A href="/index.html" onclick="alert\(8\);return false;"&gt;test&lt;/a&gt;

注意：使用A标签的 href="javascript:xxx代码" 时，里面的js代码不能使用 this, event 对象, 因为这相当于浏览器地址栏, this 不代表 A 标签。  
如果需要使用 this 或者 event 来获取此A标签,建议改用 onclick 事件。  
另外 A 标签里面的 onclick 事件返回 false,则不会跳转\(即 href 的内容不会触发, href 里面的js也不会执行\)。

  
13.正则表达式：  
产生正则表达式的方式  
1. var re = new RegExp\("pattern",\["flags"\]\); // 这种方式比较好  
pattern :正则表达式字符串 // 注意这是字符串,里面的反斜杠\("\"\)需要连写两个来表示一个,因为会转义,如 new RegExp\("\\d"\) 匹配一个数字  
flags: // flags 可以多个一起使用, 如 new RegExp\("\\w", 'gm'\)  
g global \(全文查找出现的所有 pattern\)  
i ignoreCase \(忽略大小写\)  
m multiLine \(多行查找\)

2. 使用 正斜杠\("/"\) 括起来  
var re = /pattern/flags  
pattern 和 flags 的含义跟 new RegExp 的一样。  
只不过,这里的 pattern 不是字符串,不会转义,所以里面的反斜杠\("\"\)不需要连写两个。如 /\d/ 表示匹配一个数字  
这两种方式产生的正则表达式都是一样的，如 new RegExp\("\(f+\)d+\(s+\)"\) 也可以写成： /\(f+\)d+\(s+\)/

正则表达式的常用函数：  
re.exec\(字符串\); // 返回匹配数组\(下标0是整个匹配到的字符串,下标1是第1个捕获组,下标2是第2个捕获组...\),没有匹配时返回 null  
re.test\(字符串\); // 返回 true, 或者 false,表示是否匹配  
另外,字符串也有可运用正则表达式的：  
字符串.replace\(正则表达式, 要替换的字符串\); // 要替换的字符串里面,也可以使用 $1, $2 作为捕获组  
字符串.match\(正则表达式\); // 同 re.exec,返回匹配数组,无法匹配则返回null,\[0\]是匹配的整个字符串,\[1\]是匹配的第一个捕获组,\[2\]是第二个捕获组...

RegExp 的属性  
$1, ..., $9 捕获组,$1是匹配的第一个捕获组\(即第一个用小括号括起来的内容\),$2是第二个捕获组... 如：  
if \( new RegExp\("\(f+\)d+\(s+\)"\).test\("ddfffdddsss"\) \) {  
alert\(RegExp.$1 + ", " + RegExp.$2\); // 提示出： fff, sss  
}  
$\_, input 返回输入的内容  
如: /^1\(\(3\d\)\|\(5\[036789\]\)\|\(8\[89\]\)\)\d{8}$/.exec\("13595044124"\); alert\(RegExp.$\_\); alert\(RegExp.input\); // 提示出: 13595044124

常用的正则表达式 元字符  
\ 转义符  
. 匹配除换行符以外的任意字符  
\| 或符号  
\w 匹配字母或数字或下划线 \(大写的通常是小写的反义\)  
\W 匹配任意不是字母,数字,下划线的字符  
\s 匹配任意的空白符  
\S 匹配任意不是空白符的字符  
\d 匹配数字  
\D 匹配任意非数字的字符  
\b 匹配单词的开始或结束  
\B 匹配不是单词开头或结束的位置  
^ 匹配字符串的开始  
$ 匹配字符串的结束  
\[^x\] 匹配除了x以外的任意字符  
\[^aeiou\] 匹配除了aeiou这几个字母以外的任意字符  
\数字 表示捕获组,要求与第几个捕获组相同  
常用的限定符  
\* 重复零次或多次  
+ 重复一次或多次  
? 重复零次或一次  
{n} 重复n次  
{n,} 重复n次或更多次  
{n,m} 重复n到m次

常用正则表达式  
/^\[-\]?\d+\(\[.\]?\d\*\)$/ //数字  
/^\[-\]?\d+$/ //整数  
/^\[0-9a-zA-Z\]{5,16}$/ //用户名\(区分大小写，5-16位\)  
/^\[\u4e00-\u9fa5\]+$/ //中文  
/^\(\w\){6,20}$/; //校验密码：只能输入6-20个字母、数字、下划线  
//电话号码\(手機號碼\):像\(010\)88886666，022-22334455，029 1234-5678，010 3523922轉259，3523922。04-36018188/23051418 等  
/^\(\[\(（\]?0\d{1,6}\[）\) -\]?\)?\(\d{5,30}\|\(\(\d{4}\[ -\]\){1,7}\d{1,4}\)\)\(\[ -\#\(（轉转\]?\d{1,6}\[）\)\]?\)?$/;  
/^\#?\(\[a-f0-9\]{6}\|\[a-f0-9\]{3}\)$/ //十六进制值  
/^\(\[a-zA-Z\d\_\.-\]+\)@\(\[a-zA-Z\d\]+\.\)+\[a-zA-Z\d\]{2,6}$/ //电子邮箱  
/^\(https?:\/\/\)?\(\[\da-z\.-\]+\)\.\(\[a-z\.\]{2,6}\)\(\[\/\w \.-\]\*\)\*\/?$/ //URL  
//下句是 IP 地址: 1.0.0.1 到 255.255.255.255,每段不能用“0”打头  
/^\(\[1-9\]\|\(\[1-9\]\d\)\|\(1\d\d\)\|\(2\(\[0-4\]\d\|5\[0-5\]\)\)\)\.\(\(\[\d\]\|\(\[1-9\]\d\)\|\(1\d\d\)\|\(2\(\[0-4\]\d\|5\[0-5\]\)\)\)\.\){2}\(\[1-9\]\|\(\[1-9\]\d\)\|\(1\d\d\)\|\(2\(\[0-4\]\d\|5\[0-5\]\)\)\)$/  
/^&lt;\(\[a-z\]+\)\(\[^&lt;\]+\)\*\(?:&gt;\(.\*\)&lt;\/\1&gt;\|\s+\/&gt;\)$/ //HTML 标签

"str".replace\(/\(^\s\*\)\|\(\s\*$\)/g, ""\); // 去除前后空格

//校验登录名：只能输入5-20个以字母开头、可带数字、“\_”、“.”的字符串  
function isRegisterUserName\(s\) {  
var patrn = /^\[a-zA-Z\]{1}\(\[a-zA-Z0-9\]\|\[.\_\]\){4,19}$/;  
return !!\(patrn.exec\(s\)\); //返回匹配数组,没有匹配时返回null;所以非两次以返回boolean值  
}  
//防止SQL注入，返回true表示通过验证，返回false表示验证不通过  
function IsValid\( oField \) {  
re= /select\|update\|delete\|exec\|count\|'\|"\|=\|;\|&gt;\|&lt;\|%/i;  
$sMsg = "请您不要在参数中输入特殊字符和SQL关键字！";  
if \( re.test\(oField.value\) \) {  
alert\( $sMsg \);  
return false;  
}  
return true;  
}  
// 日期检查  
function strDateTime\(str\)  
{  
var r = str.match\(/^\(\d{1,4}\)\(-\|\/\)?\(\d{1,2}\)\2\(\d{1,2}\)$/\); // 注意里面的“\2”，表示要求与第2个捕获组“\(-\|\/\)?”的值相同  
if \( r == null \) return false;  
var d = new Date\(r\[1\], r\[3\]-1, r\[4\]\);  
return \(d.getFullYear\(\)==r\[1\] && \(d.getMonth\(\)+1\)==r\[3\] && d.getDate\(\)==r\[4\]\);  
}

  
14.修改表单内容  
&lt;html&gt;  
&lt;head&gt;&lt;title&gt;修改表单内容&lt;/title&gt;  
&lt;script language="JavaScript" type="text/javascript" &gt;  
/\*\*  
\* 编辑按钮  
\* @param form 页面提交的&lt;form&gt;的name  
\* @param dataId 要编辑的行的 id  
\* @param number 要编辑的列的数量  
\*/  
var isedit = false;  
function edit \( form, dataId, number \)  
{  
if \( isedit \){ alert\("请编辑完再编辑下一笔！"\);return;}  
isedit = true;  
//获取需编辑的对象\(&lt;tr&gt;卷标对象\)  
var data = document.getElementById\("data\_"+dataId\);  
//获取需编辑的各子对象\(&lt;td&gt;卷标对象\)。注意：各&lt;td&gt;间别换行，换行符也算子元素。  
var dataNodes = data.childNodes;  
//写进去的内容。这将是数组对象  
var dataInput;  
//循环修改须编辑的列的内容  
for \( var i=number-1; i &gt;= 1; i=i-1 \) {  
var editname = "edit\_" + i;  
dataInput = "&lt;input type='text' name='" + editname + "' id='" + editname + "' ";  
dataInput += " size='10' maxlength='15' value='" + dataNodes\[i\].innerHTML + "' \/&gt;"  
dataNodes\[i\].innerHTML = dataInput;  
}  
// 第一栏是学号等 ID字段，不许修改。但提交时需在提交窗体里找到它。  
dataInput = "&lt;input type='hidden' name='edit\_0' value='";  
dataInput += dataNodes\[0\].innerHTML + "' \/&gt;" + dataNodes\[0\].innerHTML;  
dataNodes\[0\].innerHTML = dataInput;  
//性别栏，下拉菜单  
dataInput = "&lt;select name='edit\_2'&gt;"  
//dataNodes\[2\].innerHTML.indexOf\("男"\) 如果相同则传回"0"，不同传回"-1"  
if\(dataNodes\[2\].innerHTML.indexOf\("男"\) === 0\){  
dataInput += "&lt;option value='m' selected&gt;男&lt;\/option&gt;";  
dataInput += "&lt;option value='f' &gt;女&lt;\/option&gt;&lt;\/select&gt;";  
} else {  
dataInput += "&lt;option value='m' &gt;男&lt;\/option&gt;";  
dataInput += "&lt;option value='f' selected&gt;女&lt;\/option&gt;&lt;\/select&gt;";  
}  
dataNodes\[2\].innerHTML = dataInput;  
//按钮栏  
dataInput = "&lt;input type='button' value='确认' onclick=\"updateValue\(";  
dataInput += form.name + ", " + number + ", 'edit\_' \);\"\/&gt;";  
dataNodes\[ \(dataNodes.length -2\) \].innerHTML = dataInput;  
dataNodes\[ \(dataNodes.length -1\) \].innerHTML = ""; //编辑时不给删除  
form.SQLmethod.value = "modify"; //表单提交信息，与这里无关  
form.submitId.value = dataId; //表单提交信息，与这里无关  
}  
/\*\*  
\* 编辑后确认，提交  
\* @param form 页面提交的&lt;form&gt;的name  
\* @param number 要编辑的列的数量  
\* @param str name属性的开始字段  
\*/  
function updateValue \( form , number , str \) {  
var editname;  
//循环处理，主要是 alert\(\) 提醒客户端必须填写某些内容  
for \( var i=1; i &lt; number; i=i+1 \) {  
editname = str + i;  
if\( document.all\[editname\].value.length === 0\) {  
document.all\[editname\].focus\(\);  
alert\("请填写各栏目内容！"\);  
return ;  
}  
}  
form.submit\(\);  
}  
&lt;/script&gt;  
&lt;/head&gt;

&lt;body&gt;  
&lt;form name="pageForm" action="" &gt;  
&lt;table border="1"&gt;  
&lt;TR&gt;&lt;TH&gt;学号&lt;/TH&gt;&lt;TH&gt;姓名&lt;/TH&gt;&lt;TH&gt;性别&lt;/TH&gt;  
&lt;TH style="BORDER-LEFT: black 1px solid; BORDER-BOTTOM: black 1px solid"&gt;&lt;/TH&gt;  
&lt;TH style="BORDER-BOTTOM: \#000000 1px solid"&gt;&lt;/TH&gt;  
&lt;/TR&gt;  
&lt;tr id='data\_1' &gt;&lt;td&gt;101&lt;/td&gt;&lt;td&gt;stu1&lt;/td&gt;&lt;td&gt;男&lt;/td&gt;&lt;td&gt;&lt;INPUT type='button' value='编辑' onclick="edit\(pageForm,1,2 \); " &gt;&lt;/td&gt;&lt;td&gt;&lt;INPUT type='button' value='删除' onclick="del\(pageForm,1, 'del'\);" &gt;&lt;/td&gt;&lt;/tr&gt;  
&lt;tr id='data\_2' &gt;&lt;td&gt;102&lt;/td&gt;&lt;td&gt;stu2&lt;/td&gt;&lt;td&gt;女&lt;/td&gt;&lt;td&gt;&lt;INPUT type='button' value='编辑' onclick="edit\(pageForm,'2',2 \); " &gt;&lt;/td&gt;&lt;td&gt;&lt;INPUT type='button' value='删除' onclick="del\(pageForm,2, 'del'\);" &gt;&lt;/td&gt;&lt;/tr&gt;  
&lt;/table&gt;  
&lt;/form&gt;  
&lt;/body&gt;  
&lt;/html&gt;

  
15.可变长参数 的 动态函数：  
函数是一个对象，一个Function对象  
\(函数参数列表及函数主体事实上只是Function对象的构造函数的参数而已\)  
函数参数是可变的，比如定义函数时的参数列表有3个参数，调用时可以传2个参数，或者5个参数  
arguments.length 是实际参数的个数\(被传递参数的个数\)  
方法名.length 期望参数的个数\(定义函数时的参数列表的参数个数\)

动态函数：  
var square = new Function\("x", "y", "var sum;sum=x\*x+y\*y;return sum;"\);  
alert\(square\(2,3\)\); //值为13  
动态函数的作用：函数体是由一个字符串构成的，故函数体可动态生成。

  
16.页面刷新的方法：  
history.go\(0\);  
location.reload\(\);  
location=location;  
location.assign\(location\);  
document.execCommand\('Refresh'\);  
window.navigate\(location\);  
location.replace\(location\);  
document.URL=location.href;

自动刷新的方法：  
1\) &lt;head&gt; 里使用标签：&lt;meta http-equiv="refresh" content="20"&gt; //其中20指每隔20秒刷新一次页面  
2\) 使用javascript：  
&lt;script language="JavaScript"&gt;  
function myrefresh\(\) {  
window.location.reload\(\);  
}  
setTimeout\('myrefresh\(\)',1000\); //指定1秒刷新一次  
&lt;/script&gt;

页面自动跳转：  
&lt;meta http-equiv="refresh" content="20;url=http://www.wyxg.com"&gt; //20秒后跳转到url指定的页面

刷新框架的js:  
//刷新包含该框架的页面用  
parent.location.reload\(\);  
//子窗口刷新父窗口  
self.opener.location.reload\(\); \( 或 &lt;a href="javascript:opener.location.reload\(\)"&gt;刷新&lt;/a&gt; \)  
//刷新另一个框架的页面用  
parent.otherFrameID.location.reload\(\);

关闭或者打开窗口时刷新，在&lt;body&gt;中用 onload 或 onUnload 即可。  
&lt;body onload="opener.location.reload\(\)"&gt; //打开窗口时刷新  
&lt;body onUnload="opener.location.reload\(\)"&gt; //关闭窗口时刷新  
window.opener.document.location.reload\(\); // ?

  
17.用 javascript 处理 JSON：  
JSON 是 javascript 的一个子集，所以，在javascript 中使用JSON是非常简单的。  
JSON的规则很简单： 对象是一个无序的“‘名称/值’对”集合。一个对象以“{”（左括号）开始，“}”（右括号）结束。  
每个“名称”后跟一个“:”（冒号）；“‘名称/值’ 对”之间使用“,”（逗号）分隔。  
1\) 创建 JSON 对象，如下创建了只包含一个成员 "bindings" 的一个对象，bindings 则包含了一个由3个对象组成的数组。  
var myJSONObject = {"bindings": \[  
{"ircEvent": "PRIVMSG", "method": "newURI", "regex": "^http://.\*"},  
{"ircEvent": "PRIUUCG", "method": "deleteURI", "regex": "^delete.\*"},  
{"ircEvent": "PRIIPKD", "method": "randomURI", "regex": "^random.\*"}  
\]  
};  
2\) 获取对象： 在javascript 中， 成员可以通过“点号”来获取。  
如： myJSONObject.bindings\[0\].method // 结果： newURI  
alert\(myJSONObject.bindings\[1\].method\); //alert信息: deleteURI  
3\) 通过eval\(\) 函数可以将JSON字符串转化为对象。  
如： var myJSONtext = '{"ircEvent": "PRIUUCG", "method": "deleteURI", "regex": "^delete.\*"}';  
var myObject = eval\('\(' + myJSONtext + '\)'\);  
alert\(myObject.ircEvent\); //alert信息: PRIUUCG  
如： var myObject2 = eval\('\({ircEvent: "PRIUUCG", method: "delete"}\)'\); //名称也可以不用引號括起來  
alert\(myObject2.ircEvent\); //alert信息: PRIUUCG  
4\) 基于安全的考虑的 JSON 解析器。  
eval 函数非常快，但是它可以编译任何 javascirpt 代码，这样的话就可能产生安全的问题。  
eval 的使用是基于传入的代码参数是可靠的假设的，有一些情况下，可能客户端是不可信任的。  
一个 JSON 解析器将只接受 JSON 文本。所以是更安全的。  
如： var myObject = JSON.parse\(myJSONtext, filter\);  
可选的 filter 参数将遍历每一个 value key 值对， 并进行相关的处理。  
如： myData = JSON.parse\(text, function \(key, value\) {  
return key.indexOf\('date'\) &gt;= 0 ? new Date\(value\) : value;  
}\);

  
18.匿名函数与 Module 模式  
JavaScript 的任何变量，函数或是对象，除非是在某个函数内部定义，否则，就是全局的。  
意味着同一网页的别的代码可以访问并改写这个变量\(ECMA 的 JavaScript 5 已经改变了这一状况 - 译者\)  
使用匿名函数，你可以绕过这一问题。  
比如，你有这样一段代码，很显然，变量 name, age, status 将成为全局变量:  
var name = 'Chris';  
var age = 18;  
function createMenber\(\) {  
// ...  
}  
function getMenber\(\) {  
// ...  
}  
为了避免这一问题，你可以使用匿名函数:  
var myApp = function\(\) {  
var name = 'Chris';  
var age = 18;  
// 如果在函数里面再定义函数,建议如下写法,如果写“function createMenber\(\){...}”则IE7会报错  
var createMenber = function\(\) {  
// ...  
}  
var getMenber = function\(\) {  
// ...  
}  
}\(\);  
如果这个函数不会被再次调用，可以连这个函数的名称也省了，更直接写为:  
\(function\(\) {  
var name = 'Chris';  
var age = 18;  
var createMenber = function\(\) {  
// ...  
}  
var getMenber = function\(\) {  
// ...  
}  
}\) \(\);  
如果要访问其中的对象或函数，可以:  
var myApp = function\(\) {  
var name = 'Chris';  
var age = 18;  
return {  
createMenber: function\(\) {  
// ...  
}  
getMenber: function \(\) {  
// ...  
}  
}  
} \(\);  
// myApp.createMenber\(\) 和 myApp.getMenber\(\) 可以使用  
所谓 Module 模式或单例模式\(Singleton\)，假如你想在别的地方调用里面的方法，可以在匿名函数中返回这些方法，甚至用简称返回：  
var myApp = function\(\) {  
var name = 'Chris';  
var age = 18;  
var createMenber = function \(\) {  
// ...  
}  
var getMenber = function \(\) {  
// ...  
}  
return {  
create:createMenber,  
get:getMenber  
}  
} \(\);  
// myApp.create\(\) 和 myApp.get\(\) 可以使用

  
19.事件委托  
事件是JavaScript非常重要的一部分。  
我们想给一个列表中的链接绑定点击事件，一般的做法是写一个循环，给每个链接对象绑定事件，HTML代码如下：

&lt;h2&gt;Great Web resources&lt;/h2&gt;  
&lt;ul id="resources"&gt;  
&lt;li&gt;&lt;a href="http://opera.com/wsc"&gt;Opera Web Standards Curriculum&lt;/a&gt;&lt;/li&gt;  
&lt;li&gt;&lt;a href="http://sitepoint.com"&gt;Sitepoint&lt;/a&gt;&lt;/li&gt;  
&lt;li&gt;&lt;a href="http://alistapart.com"&gt;A List Apart&lt;/a&gt;&lt;/li&gt;  
&lt;li&gt;&lt;a href="http://yuiblog.com"&gt;YUI Blog&lt;/a&gt;&lt;/li&gt;  
&lt;li&gt;&lt;a href="http://blameitonthevoices.com"&gt;Blame it on the voices&lt;/a&gt;&lt;/li&gt;  
&lt;li&gt;&lt;a href="http://oddlyspecific.com"&gt;Oddly specific&lt;/a&gt;&lt;/li&gt;  
&lt;/ul&gt;

代码如下：  
// 典型事件绑定示例  
\(function\(\){  
//回调函数  
var handler = function \(e\){  
e = e \|\| window.event;  
//获取事件源\(被点击的元素对象\)  
var x = e.target \|\| e.srcElement;  
alert\('Event delegation:' + x\);  
//屏蔽Form提交事件  
if \( e.returnValue \) e.returnValue = false; //for IE  
if \( e.preventDefault \) e.preventDefault\(\); //for Firefox  
};  
var resources = document.getElementById\('resources'\);  
var links = resources.getElementsByTagName\('a'\); // Dom 对象下获取子对象  
var all = links.length;  
// 给每个链接绑定点击事件  
for\(var i=0;i&lt;all;i++\){  
var link = links\[i\];  
if \( link.attachEvent \) {  
link.attachEvent\('onclick',handler\);  
}  
else if \( link.addEventListener \) {  
link.addEventListener\('click',handler,false\);  
}  
};  
}\)\(\);

更合理的写法是只给列表的父对象绑定事件，代码如下：  
\(function\(\){  
var handler = function \(e\) {  
e = e \|\| window.event;  
var x = e.target \|\| e.srcElement;  
// 确认被点击的对象是 A标签  
if \( x.nodeName.toLowerCase\(\) === 'a' \) {  
alert\('Event delegation:' + x\);  
//屏蔽Form提交事件  
\( e.preventDefault \) ? \(e.preventDefault\(\)\) : \(e.returnValue = false\);  
}  
};  
var resources = document.getElementById\('resources'\);  
resources.onclick = handler; //也可以像上面用 addEventListener 和 attachEvent 添加 onclick 事件  
}\)\(\);

  
20.window.open\(\) 子窗口控制  
// 窗口参数,控制位置和大小、显示等  
var param = 'top='+\(screen.height-pHeight\)/2+',left='+\(screen.width-pWidth\)/2+',width='+ pWidth +',height=' + pHeight + ',resizable=yes,scrollbars=yes,location=no, status=no';  
// 参数解释:  
height=100 窗口高度； // 这里 pHeight 需要先设定参数值  
width=400 窗口宽度； // 这里 pWidth 需要先设定参数值  
top=0 窗口距离屏幕上方的象素值； //top=\(screen.height-pHeight\)/2 和 left=\(screen.width-pWidth\)/2 让窗口居中显示  
left=0 窗口距离屏幕左侧的象素值；  
toolbar=no 是否显示工具栏，yes为显示；  
menubar，scrollbars 表示菜单栏和滚动栏。  
resizable=no 是否允许改变窗口大小，yes为允许；  
location=no 是否显示地址栏，yes为允许；  
status=no 是否显示状态栏内的信息（通常是文件已经打开），yes为允许；  
// 子窗口网址  
var url = "test.html";  
var pName = "windowsName" // 子窗口的名称: 如果子窗口名称相同,会覆盖旧的窗口  
// 打开窗口,返回子窗口对象  
var win = window.open\(url,pName,param\);  
// 父窗口控制子窗口的对象  
win.window.document.getElementById\("productName"\).innerHTML = "&lt;%=prod.Name%&gt;";  
// 父窗口调用子窗口的函数  
win.testFun\(\);

// 子窗口控制父窗口  
window.opener.window.document.getElementById\("bnt"\).value = "重新查看";  
// 子窗口调用父窗口的函数  
window.opener.testfun\(\);

注意:父窗口刚打开子窗口时马上对它进行赋值或者调用其函数等操作可能会失败,因为子窗口未完全加载  
需要这样做时,最好在子窗口写加载的js,再调用父窗口; 以免操作失败。

  
21.URL编程  
javascript允许直接在URL地址栏写程序，这令js做的验证全部都是不安全，必须后台在验证一次。  
如，在一个页面的地址栏输入：“javascript:alert\(55\);”，那页面即可执行 alert 函数，同理也可执行任意的js函数。  
利用这点，&lt;A&gt;标签的地址也可以编程，如：“&lt;A href='javascript:alert\(5\);testFun\(\);'&gt;&lt;/A&gt;”

  
22.页面的script结束符问题  
如下写法，html页面不会alert,反而会在页面上显示“'\);”的内容  
&lt;script&gt;  
alert\('&lt;/script&gt;'\);  
&lt;/script&gt;

因为浏览器把alert的字符串中的“&lt;/script&gt;”解析成结束符了，需要“\”转换一下，如下写成能正常：  
&lt;script&gt;  
alert\('&lt;\/script&gt;'\);  
&lt;/script&gt;

  
23.z-index\(zIndex\)涂层使用  
在css里面用 z-index, 而javascript里面用 zIndex, 如：  
&lt;div id='fl' style="Z-INDEX: 9999999;"&gt;...&lt;/div&gt;  
&lt;script&gt;  
var element = document.getElementById\('fl'\);  
element.style.zIndex = 9;  
&lt;/script&gt;

z-index\(zIndex\) 默认为0,\(其实打印的时候为空\),涂层的数值越大越往上，也就是显示时覆盖涂层低的。  
注意：IE6上，层级会影响涂层，按先后出现的顺序来绝定层的堆叠顺序，不同层级的元素需要设置祖先元素\(上溯到同层级为止\)的z-index才生效。

24. iframe 的操作  
1\) 获得 iframe 的 window 对象。存在跨域访问限制。  
chrome: iframeElement. contentWindow  
firefox: iframeElement.contentWindow  
ie6: iframeElement.contentWindow

function getIframeWindow\(element\){  
return element.contentWindow;  
//return element.contentWindow \|\| element.contentDocument.parentWindow;  
}

2\) 获得 iframe 的 document 对象。存在跨域访问限制。  
chrome: iframeElement.contentDocument  
firefox: iframeElement.contentDocument  
ie: iframeElement.contentWindow.document // ie没有 iframeElement.contentDocument 属性。

function getIframeDocument\(element\) {  
return element.contentDocument \|\| element.contentWindow.document;  
}

3\) iframe 中获得父页面的 window 对象。存在跨域访问限制。  
父页面：window.parent  
顶层页面：window.top  
适用于所有浏览器

4\) 获得 iframe 的内容。存在跨域访问限制。  
firefox: iframeElement.contentDocument.documentElement.textContent  
ie: iframeElement.contentWindow.document.documentElement.innerText

function getIframeText\(element\) {  
var iframeDocument = element.contentDocument \|\| element.contentWindow.document;  
var documentElement = iframeDocument.documentElement \|\| iframeDocument.body;  
return documentElement.textContent \|\| documentElement.innerText;  
}

5\) iframe的 onload 事件  
非ie浏览器都提供了 onload 事件。例如下面代码在ie中是不会有弹出框的。  
var ifr = document.createElement\('iframe'\);  
ifr.src = 'http://www.b.com/index.html';  
ifr.onload = function\(\) {  
alert\('loaded'\);  
};  
document.body.appendChild\(ifr\);

但是ie却又似乎提供了onload事件，下面两种方法都会触发onload  
//方法一：  
&lt;iframe onload="alert\('loaded'\);" src="http://www.b.com/index.html"&gt;&lt;/iframe&gt;

//只有ie才支持为createElement传递这样的参数  
var ifr = document.createElement\('&lt;iframe onload="alert\(\'loaded\'\);" src="http://www.b.com/index.html"&gt;&lt;/iframe&gt;'\);  
document.body.appendChild\(ifr\);由于iframe元素包含于父级页面中，因此以上方法均不存在跨域问题。

实际上IE提供了 onload 事件，但必须使用attachEvent进行绑定。所以最好的 onload事件写法如下：

var ifr = document.createElement\('iframe'\);  
ifr.src = 'http://b.a.com/b.html';  
var loaded\_fun = function\(\){ alert\('loaded'\); }; // 要执行的 onload 事件  
if \(ifr.attachEvent\) {  
ifr.attachEvent\('onload', loaded\_fun \);  
} else {  
ifr.onload = loaded\_fun;  
}  
document.body.appendChild\(ifr\);

6\) frames  
window.frames 可以取到页面中的帧\( iframe, frame 等\)，需要注意的是取到的是 window 对象，而不是 HTMLElement 。  
var ifr1 = document.getElementById\('ifr1'\);  
var ifr1win = window.frames\[0\];  
ifr1win.frameElement === ifr1; // true  
ifr1win === ifr1; // false

  
25. 反射  
在JavaScript中能利用 for in 语句实现反射,如：  
// 下面这段语句遍历obj对象的所有属性和方法  
for \(var p in obj\) {  
if \(typeof\(obj\[p\]=="function"\) {  
obj\[p\]\(\); // 执行函数,也还可以传参数  
} else {  
alert\(obj\[p\]\);  
}  
}

obj.函数名\(参数列表\); // 这样执行函数，可以使用下面的反射形式来代替  
obj\["函数名"\]\(参数列表\);

  
26. 过滤数组的重复值  
/\*\*  
\* 返回没有重复值的新数组,原数组不改变  
\* @return 返回过滤重复值后的新数组  
\*  
\* @example  
\* var arr = \['a', 'b', 'c', 'd', 'c', null\];  
\* var arr2 = arr.unique\(\); // arr2 为: \['a', 'b', 'd', 'c', null\]  
\*/  
Array.prototype.unique = function\(\) {  
var result = \[\];  
// 注意学习此算法  
for \(var i=0,l=this.length; i&lt;l; i++\) {  
for \(var j=i+1; j&lt;l; j++\) {  
if \(this\[i\] === this\[j\]\) j = ++i;  
}  
result.push\(this\[i\]\);  
}  
return result;  
};

  
27. 巧用“\|\|”、“&&”和“!”  
松散性语言的特性, if 判断时可以用任意值, false、 null、 undefine、 ''、 0、 NaN 都会被当成 false  
利用js的松散性和没类型特性, 可简化一些代码:

function fun1\(name, fun2, obj, add\_step\) {

// 设预设值  
name = name \|\| '匿名';  
// 上面一句相当于下面这一句  
if \( !name \) name = '匿名';

// 假如传入的 fun2 是个函数, 当有此值传入时执行, 没有则不执行  
fun2 && fun2\(\);  
// 上面一句相当于下面这一句  
if \( fun2 \) fun2\(\);

// 转成布尔值,不管传入的 obj 是什么类型的值, 都会返回布尔类型的值  
return !!obj;  
// 上面一句相当于下面这几句  
if \( obj \) {  
return true;  
} else {  
return false;  
}

// && 多重的if判断,或者swith判断,可以这样简写  
var add\_level = \(add\_step&gt;10 && 3\) \|\| \(add\_step&gt;5 && 2\) \|\| \(add\_step&gt;0 && 1\) \|\| 0;  
// 上面一句相当于下面这几句  
var add\_level;  
if \(add\_step &gt; 10\) {  
add\_level = 3;  
} else if \(add\_step &gt; 5\) {  
add\_level = 2;  
} else if \(add\_step &gt; 0\) {  
add\_level = 1;  
} else {  
add\_level = 0;  
}

}  
// “\|\|”、“&&”和“!”的特性帮我们精简了代码,同时也降低了代码的可读性。 这就需要我们自己来权衡了。  
// 不一定非得用这些精简写法,但得读得懂,因为很多框架用上了这类写法。  
// 之所以会牺牲可读性来用这些简便写法,是为了压缩代码量,减少访问时间。

