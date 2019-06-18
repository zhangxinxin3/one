JSX

JSX就是js的对象

React 使用 JSX 来替代常规的 JavaScript。

JSX 是一个看起来很像 XML 的 JavaScript 语法扩展。

我们不需要一定使用 JSX，但它有以下优点：

JSX 执行更快，因为它在编译为 JavaScript 代码后进行了优化。
它是类型安全的，在编译过程中就能发现错误。
使用 JSX 编写模板更加简单快速。
JSX 是在 JavaScript 内部实现的。

我们知道元素是构成 React 应用的最小单位，JSX 就是用来声明 React 当中的元素。

与浏览器的 DOM 元素不同，React 当中的元素事实上是普通的对象，React DOM 可以确保 浏览器 DOM 的数据内容与 React 元素保持一致。

要将 React 元素渲染到根 DOM 节点中，我们通过把它们都传递给 ReactDOM.render() 的方法来将其渲染到页面上

var myDivElement = <div className="foo" />;
ReactDOM.render(myDivElement, document.getElementById('example'));
JavaScript 表达式

我们可以在 JSX 中使用 JavaScript 表达式。表达式写在花括号 {} 中

ReactDOM.render(
    <div>
      <h1>{1+1}</h1>
    </div>
    ,
    document.getElementById('example')
);
样式

React 推荐使用内联样式。我们可以使用 camelCase 语法来设置内联样式. React 会在指定元素数字后自动添加 px 。

var myStyle = {
    fontSize: 100,
    color: '#FF0000'
};
ReactDOM.render(
    <h1 style = {myStyle}>菜鸟教程</h1>,
    document.getElementById('example')
);
在 JSX 中不能使用 if else 语句，但可以使用 conditional (三元运算) 表达式来替代。

ReactDOM.render(
    <div>
      <h1>{i == 1 ? 'True!' : 'False'}</h1>
    </div>
    ,
    document.getElementById('example')
);

注意:

由于 JSX 就是 JavaScript，一些标识符像 class 和 for 不建议作为 XML 属性名。作为替代，React DOM 使用 className 和 htmlFor 来做对应的属性。

虚拟DOM

什么是虚拟DOM

vdom可以看作是一个使用javascript模拟了DOM结构的树形结构，这个树结构包含整个DOM结构的信息

pure:true 纯函数 1.无副作用，2.结果可预测，随机函数

大前端

1web 1.pc端/m端 2.webApp 3.hybird App 4.web+native

区别：只有web有进度条

2.客户端(原生/native) 产物：app安装包

1.android java 

2.iOS object-c






代表generator
generator函数低依次调用，返回的是一个迭代器

yield返回值

next()向下执行 {value:,done:表示generator函数的状态}

后一次调用next传入的表达式会作为前一次yield表达式的返回值

yield配合promise