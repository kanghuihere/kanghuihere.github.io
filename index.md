<span style="display: flex; justify-content: center"><span>[前端知识](#前端知识) | [错误总结](#错误总结) | [软件使用](#软件使用)</span></span>  

# 前端知识
* * *
## HTML
* * *

## CSS
* * *
#### 隐藏
```css
dispaly: none;
visibility: hidden;
```

#### :host :ng-deep
> 对组件中没有暴露的元素设置样式

## JavaScript
* * *
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
> 查找一个数组中是否包含某个元素

#### map
```javascript
map(res,item => {
 return {label: item.id}
})
```

#### join
> 将数组组合成字符串

#### 新建对象
```javascript
Array.from({ length: 7 }).map(e => {
return { name: 0, id: '' };
})
```

#### 排序
```javascript
sort((a, b) => a.order - b.order)
```



## Angular
* * *
#### 从其他页面或组件调用函数
```javascript
@Output demoCallBack=new EventEmitter(); 
this.demoCallBack.emit();
```
```html
<aui-demo (demoCallBack)='demo()'></aui-demo>
demo{}
```

elementRef
nativeElement

## 其他
* * *
#### _result使用
#### jason国际化
> jason文件中`"demo":"中文"`
> 1.html中使用插值`{{'demo' | i18n}}`,在标签中引号引用<ng-container *ngSwitchCase='"demo"'>
> 2.js中`this.i18n.get("demo")`
> 3.动态填入内容`"demo":{name}`,js中使用时`this.i18n.get('demo',{name:'动态值'})`
#### _cloneDeep(value)
> 改变地址，当只想要值，不想要地址时使用

# 错误总结
* * *
#### 命名
> 类名: aui-demo
> 变量: auiDemo

#### 空值处理
> 容易遗漏，不处理会报错，一般采用判断语句

#### 函数返回值为布尔类型
> 返回表达式的写法`return (demo)`

#### isleaf属性
> 在下拉选择、数中的最小节点中设置

#### 对象可能为 "null"情况处理
> 对象后加！，编译不报错，但是为空还是会报错
> 对象后加？，为空也不会报错（3.7版本以上）

# 软件使用
* * *
#### npm命令
> npm install - package.jason中的包变化
> npm run gen - swagger文件变化
> npm start - package或proxy变化

#### http错误类型
> 2开头 - 成功
> 4开头 - 客户端问题
> 5开头 - 服务器问题
