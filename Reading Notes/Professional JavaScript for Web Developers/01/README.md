# javaScript简介
javaScript是一种专为网页交互设计的脚本语言，由三个不同的部分组成
## 1. 核心 ECMAScript
由ECMA-262定义，提供核心语言功能，主要规定了
1. 语法
2. 类型
3. 语句
4. 关键字
5. 保留字
6. 操作符
7. 对象
#### 1-1 定义
* ECMAScript就是对实现该标准规定的各个方面内容的语言的描述。
* __web浏览器只是ECMAScript实现的宿主环境之一。__
* 常见宿主环境,web浏览器，Node，Adobe Flash
#### 1-2 ECMAScript 兼容
1. 支持ECMA-262描述的所有"类型、值、对象、属性、函数、程序句法和语义"。
2. 支持Unicode字符标准。
3. 可以新增ECMA-262没有描述的"类型、值、对象、属性、函数"。
4. 支持ECMA-262没有定义的"程序和正则表达式语法"。(也就是说，可以修改和扩展内置的正则表达式语法)  
> 由于各大浏览器对ECMA-262的实现不一，才会有前端的各种兼容问题。

## 2. 文档对象模型(DOM)
* 针对XML但经过扩展用于HTML的应用程序编程接口。
* DOM把整个页面映射为一个多层节点结构。
* HTML或XML页面中的每个组成部分都是某种类型的节点，节点又包含着不同类型的数据。
* DOM提供访问和操作这些节点的方法和接口。
## 2-1 DOM1级
  1. 核心，定义HTML映射规则
  2. DOM HEML 规定了针对HTML的对象和方法
## 2-2 DOM2级
  1. DOM视图
  2. DOM事件
  3. DOM样式（对应CSS对元素应用样式的接口）
  4. DOM遍历和范围
## 2-3 DOM3级
  1. 加载和保存文档的方法
  2. 验证文档的方法
  3. 支持XML1.0规范
## 2-4 web浏览器对DOM的支持
* 支持程度不一也是前端做各浏览器兼容的痛点

## 3. 浏览器对象模型(BOM)
* 提供与浏览器交互的方法和接口

## 4. 浏览器兼容
* javaScript的这三个组成部分，在当前5个主要浏览器(IE、Firefox、Chrome、Safari、Opera)中得到了不同程度的支持。
* 对es3的支持大体不错，es5的支持程度也越来越高，但对DOM的支持则彼此相差很多。
* 对已经正式纳入HTML5标准的BOM来说，尽管各浏览器都实现了某些众所周知的共同特性，但其他特性还是会因浏览器而异。