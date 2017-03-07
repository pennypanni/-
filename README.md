## 常用命令

### git 常用命令

```bash
//只克隆仓库中的一个分支
git clone -b <branch_name> <repo>

git clone -b v2 http://git.showgold.cn:8081/wabg/download.git
```

## Javascript相关知识

DOM (Document Object Model)（文档对象模型）是用于访问 HTML 元素的正式 W3C 标准。

外部的JavaScript文件不能包含 &lt;script&gt; 标签。

JavaScript 可以通过不同的方式来输出数据：
* 使用 window.alert() 弹出警告框。
* 使用 document.write() 方法将内容写到 HTML 文档中。
* 使用 innerHTML 写入到 HTML 元素。
* 使用 console.log() 写入到浏览器的控制台。

#### JavaScript 变量
* 变量必须以字母开头
* 变量也能以 $ 和 _ 符号开头（不过我们不推荐这么做）
* 变量名称对大小写敏感（y 和 Y 是不同的变量）

#### 变量作用域

![变量作用域](img/bianliangzuoyongyu.png)

如果变量在函数内没有声明（没有使用 var 关键字），该变量为全局变量。<br>
以下实例中 carName 在函数内，但是为全局变量。<br>
```javascript
// 此处可调用 carName 变量

function myFunction() {
    carName = "Volvo";

    // 此处可调用 carName 变量

}
```

#### for···in 循环

for···in 语句循环遍历对象的`属性`，例：
```javascript
function myFunction(){
	var x;
	var txt="";
	var person={fname:"Bill",lname:"Gates",age:56}; 
	for (x in person){
		txt=txt + person[x]+"<br>";
	}
	document.getElementById("demo").innerHTML=txt;
}
```

结果：

![forin](img/forin.png)

#### continue 语句

continue 语句中断循环中的迭代，如果出现了指定的条件，然后继续循环中的下一个迭代。 该例子跳过了值 3：
```javascript
function myFunction(){
	var x="",i=0;
	for (i=0;i<10;i++){
  		if (i==3){
    		continue;
    	}
		x=x + "该数字为 " + i + "<br>";
  	}
	document.getElementById("demo").innerHTML=x;
}
```

结果：

![continue](img/continue.png)

#### constructor 属性

constructor 属性返回所有 JavaScript 变量的构造函数。

![constructor](img/constructor.png)

