<span style="display: flex; justify-content: center"><span>[html](#html) | [css](#css) | [javascript](#javascript) | [angular](#angular) | [错误总结](#错误总结) | [live组件](#live组件) | [软件使用](#软件使用) | [其他](#其他)</span></span>  

# html
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * 



# css
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * 
#### 隐藏
```css
dispaly: none;
visibility: hidden;
```
#### :host :ng-deep
对组件中没有暴露的元素设置样式



# javascript
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * 
#### canvas图片格式转jpg
```javascript
canvas = doucument.querySelector('canvas');
url = canvas.toDataURL();
```
#### 下载图片
```javascript
<a href="url" download></a>
```
#### includes
查找一个数组中是否包含某个元素
#### join
将数组组合成字符串
#### 新建对象
```js
Array.from({ length: 7 }).map(e => {
return { name: 0, id: '' };
})
```
#### 解构赋值
`a=b`，即将b的值给了a，当a改变时b也会改变；   
将`a={...b}`,a改变时b不会变化，这样就有两个空间了  
#### _cloneDeep(value)
改变地址，当只想要值，不想要地址时使用
#### this
#### map
抽象，将f(x)作用在数组的每一个元素上，并把结果生成一个新的数组
```javascript
map(res,item => {
 return {label: item.id}
})
result = arr.map(fx)
```
#### reduce
结果与数组下一个进行累积计算
```js
[x1, x2, x3, x4].reduce(f) = f(f(f(x1, x2), x3), x4)
var arr = [1, 3, 5, 7, 9];
arr.reduce(function (x, y) {
    return x + y;
});
```
#### 排序
```javascript
arr.sort((a, b) => a.key - b.key)
```
#### filter
将传入的函数作用于数组的每个元素，根据返回值false或true来决定是否保留
```js
var r = arr.filter(function (x) {
    return x % 2 !== 0;
});
```
#### every
判断数组的所有元素是否满足条件，全部满足返回true，有不满足的返回false
```js
arr.every(function (s) {
    return s.length > 0;
})
```
#### find&findIndex
find查找数组中符合条件的元素，返回第一个符合的元素，没有则返回undefined
findIndex返回元素索引，没有返回-1
```js
var arr = ['Apple', 'pear', 'orange'];
console.log(arr.find(function (s) {
    return s.toLowerCase() === s;
})); // 'pear', 因为pear全部是小写
```
#### forEach
依次传入数组的元素，遍历函数，与map的区别是没有返回值


# Angular
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * 
#### 从其他页面或组件调用函数
```javascript
@Output demoCallBack=new EventEmitter(); 
this.demoCallBack.emit();
```
```html
<aui-demo (demoCallBack)='demo()'></aui-demo>
demo{}
```
#### ng区别
ng-container - 不存在，仅作为容器使用（两个结构型指令*ngIf,*ngFor,*ngSwitch等是不可以应用在同一个元素上的）   
ng-template - 模板
```html
<ng-template #loadingTemp>定义模板</ng-template>
<div *ngIf="!loading else loadingTemp">使用模板</div>
```
ng-content - 公共组件



# live组件
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *



# 错误总结
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * 
#### 命名
类名: aui-demo;  
变量: auiDemo;
#### 空值处理
容易遗漏，不处理会报错，一般采用判断语句
#### 函数返回值为布尔类型
返回表达式的写法`return (demo)`
#### isleaf属性
在下拉选择、数中的最小节点中设置
#### 对象可能为 "null"情况处理
对象后加！，编译不报错，但是为空还是会报错;  
对象后加？，为空也不会报错（3.7版本以上）  
#### a标签有click事件时需要加`href="javascript:void(0)"`
`void(demo)`输入任何值都返回undefined



# 软件使用
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * 
#### 启动环境
code或isource中配置SSH  
git中输入`git clone` + 工程的ssh链接  
host配置`C:\Windows\System32\drivers\etc`  
新建分支 `git checkout -b feat/kanghui`  
拉代码`git pull origin master`  
#### npm命令
npm install - package.jason中的包变化;  
npm run gen - swagger文件变化;  
npm start - package或proxy变化;  
#### 组件更新
组件更新`npm i @iux/live@latest`latest也可以是版本号  
html,ts(`demo()`,`@ViewChild`,`@Output`,`@Input`),module  
#### cmd常用命令
IP查询 - `ipconfig`
#### vscode常用
Ctrl+P - 搜索文件
Ctrl+f - 搜索代码
#### Chrome常用
#### http错误类型
2开头 - 成功  
4开头 - 客户端问题  
5开头 - 服务器问题  



# 其他
* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * 
#### jason国际化
jason文件中`"demo":"中文"`;  
1.html中使用插值`{{'demo' | i18n}}`,在标签中引号引用`<ng-container *ngSwitchCase='"demo"'>`;  
2.js中`this.i18n.get("demo")`;  
3.动态填入内容`"demo":{name}`,js中使用时`this.i18n.get('demo',{name:'动态值'})`;  
