# 错误汇总

### 使用新需要引入module
调用其他页面和组件中的函数
```javascript
@Output demoCallBack=new EventEmitter(); 
this.demoCallBack.emit();
```

[跳转到错误总结](https://kanghuihere.github.io/error.md) 

```html
<aui-demo (demoCallBack)='demoCallBack()'></aui-demo>
demoCallBack{}
```

```html
<h2 class="demo"></h2>
```
---
### 2222222