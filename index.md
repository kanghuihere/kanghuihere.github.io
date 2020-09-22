# 错误汇总

### 使用新需要引入module
调用其他页面和组件中的函数
```
@Output demoCallBack=new EventEmitter(); 
this.demoCallBack.emit();
```

```
<aui-demo (demoCallBack)='demoCallBack()'></aui-demo>
demoCallBack{}
```

```
<h2 class="demo">111</h2>
```
---
### 2222222
