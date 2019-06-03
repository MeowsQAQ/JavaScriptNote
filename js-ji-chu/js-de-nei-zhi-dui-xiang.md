# JS的内置对象

## **Array, Boolean, Date, Math, Number , String，Error, Function, Global , Object, RegExp**

  
在JavaScript中除了null和undefined以外其它的数据类型都被定义成了对象，可以用创建对象的方法定义变量； String、Math、Array、Date、RegExp是JavaScript中常用的对象

### 数据对象:  ****Number数据对象； String字符串对象； Boolean布尔值对象 组合对象:  Array数组对象； Math数学对象； Date日期对象 高级对象:  Object自定义对象；Error错误对象；Function函数对象； RegExp正    则表达式对象；Global全局对象

  
**自动创建对象**:调用字符串的对象属性或方法时自动创建对象，用完就丢弃。 如：

```javascript
 var str1="hello world";
```

  
手工创建对象:采用new创建字符串对象str1，全局有效。 如：

```javascript
var str1= new String("hello word");
```

## 1. String 字符串对象：

格式编排:anchor\(\)锚、blink\(\)闪烁、fixed\(\)固定、bold\(\)粗体、italics\(\)斜体、strike\(\)删除线  
big\(\)字变大、small\(\)字变小、sub\(\)下标、sup\(\)上标；

* **fontcolor\(color\)** 字体颜色
* **fontsize\(size\)** 字体大小
* **link\(url\)** 超链接 大小写转换
* **toLowerCase\(\)**返回小写字符串
* **toUpperCase\(\)**返回大写字符串 获取指定字符:
* **charAt\(index\)**返回指定位置字符
* **charCodeAt\(index\)**返回指定位置字符Unicode编码 用法：
* **str1.bold\(\)**;//字体变粗；相当于“&lt;b&gt;str1&lt;/b&gt;“ str1.anchor\(\); //把str1标识为锚 子字符串处理:                                                                                                                                                截取:
* **str1.substr\(start,length\);** //返回从索引位置start开始长为length的子字符串
* **str1.substring\(start,end\);** //返回start开始end结束的子字符串,不包括最后的一个
* **str1.slice\(start,end\);** //同substring，但允许使用负数表示从后计算位置,不包括最后的一个 替换:
* **str1.replace\(findstr,tostr\);** //返回替换finstr为tostr之后的字符串 分割:
* **str1.split\(bystr\);** //返回由bystr分割成的字符串数组\(通常bystr是连接符号，如逗号或横杆\) 连接:
* **str1.concat\(string2\);** //返回 str1 与 string2 连接后的字符串 查询字符串: 
* **indexOf\(findstr,index\);** //返回正向的索引位置、lastIndexOf\(findstr\)返回反向的索引位置
* **match\(regexp\);** //返回匹配的字符串、search\(regexp\)返回找到字符串的首字符索
* **str1.indexOf\(findstr,index\);**//查找字符串findstr;从index位置开始的索引，省略index则从0开始找;类似下一句
* **str1.lastIndexOf\(findstr\);** //从后面找起;返回findstr在str1中出现的首字符位置下标，没有找到返回-1
* **str1.match\(regexp\);** //regexp代表正则表达式或字符串;返回匹配字符串的数组，如果没有匹配则返回null
* **str1.search\(regexp\);** //返回匹配字符串的首字符位置下标;作用同indexOf方法,但可写正则表达式
* **str1.length;** //获取字符串长度；汉字、字母长度均为1；返回大于或等于0的整数 

## 2. Array 数组对象：

#### 1\) 创建数组：

```javascript
var a = new Array(); a[0] = "元素1"; a[1] = "元素2";
var a = new Array(){"元素1", "元素2"};
var a = new Array("元素1","元素2"); //一维数组，效果同上
var a = new Array(); a[0] = new Array(); //二维数组
var a = ['元素1', '元素2']; // 效果等同于: var a = new Array("元素1","元素2");
```

### 2\) 删除数组： delete 数组名;

### 3\) 数组操作：

* **arr.length;** //获取数组元素的个数；返回大于或等于0的整数 连接数组： \(原数组不变\)
* **arr.join\(bystr\);** //把数组的各元素由bystr连接起来作为字符串；与字符串的split功能刚好相反
* **arr.toString\(\);** //返回由逗号\(,\)连接数组元素组成的字符串
* **document.write\(v.toString\(\)\);**
* **document.write\(v\);** //这两句效果一样
* **arr2 = arr.concat\(元素, ...\);** //把元素添加到数组尾端后，返回另一数组；在参数里填入另一数组，返回合并数组 数组排序： \(返回排序后的数组；改变原数组\)
* **arr.reverse\(\);** //按原顺序倒着排序
* **arr.sort\(\);** //按字典顺序排序 获取子数组： \(返回被删/被截取的元素数组\)
* **arr.slice\(start,end\);** //从start下标开始，截取到end；返回被截取的元素数组；不改变原数组 //start和end可用负数表倒数\(-1代表最后一个元素\)；end&lt;start时不截取；忽略end，截取start后的所有元素
* **arr.splice\(start,n,value, ...\);** //从start下标开始删除n个，再插入value\(可理解为替换\)；改变原数组//start为负数时表倒数；n&lt;1表不删除；可忽略value\(不插入\)；可忽略n，表删除后面所有；返回被删元素数组

### 4\) 栈：\(数组的基础； 改变原数组\)

* **arr.pop\(\);** //删最后的一个元素；返回删除的元素
* **arr.push\(元素, ...\);** //添加元素到最后位置；返回数组长度; 等价于: arr\[length\] = newValue;
* **arr.unshift\(元素, ...\);** //添加元素到最前位置\(多个参数，则按参数顺序同时插入\)；返回数组长度
* **arr.shift\(\);** //删最前的一个元素；返回被删除的元素

### 5\) toString 和 valueOf

把每一项都调用 toString 方法，然后用半角逗号\(,\)连接每一项。

```javascript
var arr = [1,2,3,4,5]; alert(arr); //output:1,2,3,4,5
```

toLocaleString 方法在这里不做详细说明了，他的效果与 toString 方法类似，只是每项调用 toLocateString 方法。

## 4. Math 数学对象：

**数学常数**\(可直接用\)  
**Math.E \(自然数\)**

1. Math.LN2 \(ln2\) 
2. Math.LN10 \(ln10\) 
3. Math.LOG2E \(log 2e\)
4. Math.LOG10E \(log e\)
5. Math.PI \(圆周率\)
6. Math.SQRT1\_2 \(根号1/2\) 
7. Math.SQRT2 \(根号2\)

**三角函数**：

1. Math.sin\(x\) 计算正弦值； \(x在0~2π之间，返回值-1~1\)
2. Math.cos\(x\) 计算余弦值； \(x在0~2π之间，返回值-1~1\)
3. Math.tan\(x\) 计算正切值； \(x在0~2π之间，返回正切值\)

**反三角函数**：

1. Math.asin\(x\) 计算反正弦值；\(x在 -1与1之间，返回0~2π\)
2. Math.acos\(x\) 计算反余弦值；\(x在 -1与1之间，返回0~2π\)
3. Math.atan\(x\) 计算反正切值；\(x可以为任意值，返回 -π/2 ~π/2\)
4. Math.atan2\(y,x\) 计算从X轴到一个点的角度；\(y,x分别为点的纵坐标和横坐标，返回-π ~π\)

**计算函数**：

1. Math.sqrt\(x\) 计算平方根
2. Math.pow\(x,y\) 计算x^y
3. Math.exp\(x\) 计算e的指数 e^x
4. Math.log\(x\) 计算自然对数 \(x为大于0的整数\)

**数值比较函数**：

1. Math.abs\(x\) 计算绝对值
2. Math.max\(x,y,...\) 返回参数中最大的一个
3. Math.min\(x,y,...\) 返回参数中最小的一个
4. \* Math.random\(\) 返回0~1之间的一个随机数 //若要整数时，如0~99的随机数： `n=parseInt(Math.random()*100);`
5. Math.round\(x\) 返回舍入为最接近的整数\(四舍五入，负数时五舍六入\)
6. \* Math.floor\(x\) 返回下舍入整数 \(结果不大于x；正数时直接舍去小数，负数时 -1.1==-2 
7. Math.ceil\(x\) 返回上舍入整数 \(结果大于等于x\)

## 5. Date 时间对象：

### 创建日期对象：

#### a.不指定参数时：

```javascript
var nowd1=new Date();
document.write(nowd1.toLocaleString( ));
//显示当前时间，如：2019年5月24日 星期五 19时23分21秒
//不用"toLocaleString()"则显示： Mon Nov 24 2008 19:23:21 GMT+0800 (CST)
```

####  b.参数为日期字符串： 

```javascript
var nowd2=new Date("2008/3/20 11:12");
alert(nowd2.toLocaleString());
//显示： 2008年03月20日 星期六 11时12分00秒
var nowd2=new Date("2008/3/20 11:12");
alert(nowd2.toLocaleString());
//显示： 2008年03月20日 星期六 11时12分00秒
```

#### c.参数为毫秒数：

```javascript
var nowd3=new Date(5000); 
alert(nowd3.toLocaleString( ));
//显示： 1970年01月01日 星期四 08时00分05秒 //显示本国的时间
alert(nowd3.toUTCString()); 
//显示西方的时间： Thu, 01 Jan 1970 00:00:05 GMT
```

#### d.参数为年月日小时分钟秒毫秒：

```javascript
var nowd4=new Date(2008,10,24,11,12,0,300);
alert(nowd4.toLocaleString( )); 
//毫秒并不直接显示；月份参数从0~11，所以这里10对应11月份
//显示： 2008年11月24日 星期一 11时12分00秒
```

### 获取和设置日期、时间的方法：

* **getDate\(\) setDate\(day\_of\_month\)** 日期 \(1~31\)
* **getDay\(\)** 星期 \(1~7; 没set方法\)
* **getMonth\(\) setMonth \(month\)** 月份 \(0~11; 别忘加1\)
* **getFullYear\(\) setFullYear \(year\)** 完整年份\(-271820~275760\)
* **getYear\(\) setYear\(year\)** 年 \(范围同上； 1900年计算为0\)
* g**etHours\(\) setHours \(hour\)** 小时 \(0~23\)
* **getMinutes\(\) setMinutes \(minute\)** 分钟 \(0~59\)
* **getSeconds\(\) setSeconds \(second\)** 秒 \(0~59\)
* **getMilliseconds\(\) setMillliseconds \(ms\)** 毫秒\(0-999\)
* **getTime\(\) setTime \(allms\)** 累计毫秒数\(从1970/1/1 00:00:00开始\) 注意：set方法对任意整数有效，影响上一级的数；如setDate\(-1\)设为上个月30号。 但对小数没效。

### 日期和时间的转换：

* **getTimezoneOffset\(\)** 返回本地时间与GMT的时间差，以分钟为单位\(中国为-480；差8小时\)
* **toUTCString\(\)** 返回国际标准时间字符串\(默认\)
* **toLocalString\(\)** 返回本地格式时间字符串
* **Date.parse\(x\)** 返回累计毫秒数\(从1970/1/1 00:00:00到x的本地时间，忽略秒以下的数字\)
* **Date.UTC\(x\)** 返回累计毫秒数\(从1970/1/1 00:00:00到x的UTC时间\) 不明UTC是什么



