# 自定义对象

## 1. 基本语法：

使用 function 指令定义。其属性用“this.属性名”定义。  
如：

```javascript
function ObjectName(yName,yAge) {
this.name = yName;
this.age = yAge;
}
//调用时：
var myObject = new ObjectName("kk",80); // ObjectName 里面的函数会被执行
document.write("name = " + myObject.name + "<br> age = " + myObject.age);
```

## 2. 使用简略语句快速创建对象

### 1\) 类

```javascript
//正常写法
var car = new Object();
car.color = "red";
car.wheels = 4;
car.hubcaps = "spinning";
简略写法：
var car = {
color: "red",
wheels:4,
hubcaps:"spinning"
}
//对象 car 就此创建，不过需要特别注意，结束花括号前一定不要加 ";" 否则在 IE 会遇到很大麻烦。
```

### 2\) 数组

```javascript
//正常数组是这样写的： 
var movies = new Array('Transformers','Transformers2','Avatar','Indiana Jones 4');
//更简洁的写法是： 
var movies = ['Transformers', 'Transformers2', 'Avatar', 'Indiana Jones 4'];
```

### 3\)关联数组

这样一个特别的东西。 你会发现很多代码是这样定义对象的：

```javascript
var car = new Array();
car['colour'] = 'red';
car['wheels'] = 4;
car['hubcaps'] = 'spinning';
//遍历的时候
for ( var key in car ) { alert(key + " : " + car[key]); }
```

## 3.匿名函数

```javascript
var myFun = function(args1, args2){ alert('haha'); }
//变量 myFun 指向一个匿名函数,这相当于创建函数
function myFun(args1, args2){ alert('haha'); }
```

由于 javascript 没有类型,所以变量可以指向任意类型,也可以指向一个函数,对它来说都只是一片内存空间而已  
匿名函数一般用在只有一次使用的情况下,也是可以传递参数的  
如: `element.onclick = function(){ alert(0); }`

## 4.JavaScript原生函数

```javascript
//要找一组数字中的最大数,如下，可以用一个循环
var numbers = [3,342,23,22,124];
var max = 0;
for(var i=0;i<numbers.length;i++){ 
    if(numbers[i] > max){max = numbers[i];} 
    }
alert(max);
//也可以用排序实现同样的功能：
var numbers = [3,342,23,22,124];
numbers.sort(function(a,b){return b - a});
alert(numbers[0]);
//而最简洁的写法是：
Math.max(12,123,3,2,433,4); // returns 433
//你甚至可以使用Math.max来检测浏览器支持哪个属性：
var scrollTop = Math.max( document.documentElement.scrollTop, 
                          document.body.scrollTop );
```

## 5.增加class样式

```javascript
//可能原始的写法是这样的：
function addclass(elm,newclass) {
var c = elm.className;
elm.className = (c === '') ? newclass : c+' '+newclass;
}
//而更优雅的写法是：
function addclass(elm,newclass){
var classes = elm.className.split(' ');
classes.push(newclass);
elm.className = classes.join(' ');
}
```

## 6.对象的继承

一般的做法是复制所有属性，但还有种方法，就是: Function.apply  
函数的 apply 方法能劫持另外一个对象的方法，继承另外一个对象的属性  
Function.apply\(obj,args\) 方法接收两个参数  
obj：这个对象将代替Function类里this对象  
args：这个是数组，它将作为参数传给Function（args--&gt;arguments）：

```javascript
function Person(name,age){ // 定义一个类，人类
this.name=name; //名字
this.age=age; //年龄
this.sayhello=function(){alert("hello " + this.name);};
}
function Print(){ // 显示类的属性
this.show=function(){
var msg=[];
for(var key in this){
if(typeof(this[key])!="function"){
msg.push([key,":",this[key]].join(""));}
}
alert(msg.join(" "));
};
}
function Student(name,age,grade,school){ //学生类
Person.apply(this,arguments); // this 继承 Person,具备了它的所有方法和属性
Print.apply(this,arguments); // this 继承 Print,具备了它的所有方法和属性
this.grade=grade; //年级
this.school=school; //学校
}
var p1=new Person("jake",10);
p1.sayhello();
var s1=new Student("tom",13,6,"清华小学");
s1.show();
s1.sayhello();
```

