# 补第五课作业 

## 区分相同变量名

![](https://o3b126ie1.qnssl.com/avatar/081d10a4-6e49-47a5-8f9b-ca7d48dacb78)

在上图中，第1行代码是定义了output函数，赋值参数name给这个函数。第2行通过日志输出这个参数的值。

第五行声明变量name,赋值'Hello,JS'给name，这时相当于传递一个参数给新的变量。第六行是用户要输出现在这个name变量里的值。
此时特别要注意的是第5、6行的name与前面第1、2行的name已不是同一个变量。这是比较容易混淆的一个地方。
此外，第1行的output是一个函数名；第6行的output是一个输出命令。

此前我曾困惑为什么最后运行输出的结果只有一行'Hello,JS'，而不是两行。

直到后来才开始明白过来：

原来最后第6行输出的只有第5行变量的值。而前面第1行的函数output因为并没有被调用，所有没有输出；且前后的name变量也是不同的。

为了验证我的想法，将代码改写如下：

function output(anyname) {

    console.log(anyname);
    
}

var sayname = 'Hello, JS';

output(sayname);

output(output);

console.log(output);

最后运行输出，结果如下：

Hello, JS

function output(anyname) { ... }

function output(anyname) { ... }

老师，这样理解可对？
