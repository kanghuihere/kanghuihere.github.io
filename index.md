# 错误汇总

### 使用新需要引入module
调用其他页面和组件中的函数
```
@Output demoCallBack=new EventEmitter(); //触发位置
this.demoCallBack.emit();
<aui-demo (demoCallBack)='demoCallBack()'></aui-demo>
demoCallBack{}
```

---
### 2222222
