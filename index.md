<span style="display: flex; justify-content: center"><span>[前端知识](#前端知识) | [错误总结](#错误总结) | [软件使用](#软件使用)</span></span>  

# 前端知识
* * *
## HTML

## css
### 隐藏
```css
dispaly: none;
visibility: hidden;
```

## JavaScript
### canvas图片格式转jpg
```javascript
canvas = doucument.querySelector('canvas');
url = canvas.toDataURL();
```
* * *
### 下载图片
```javascript
<a href="url" download></a>
```
* * *
### includes
查找一个数组中是否包含某个元素


## Angular



### 从其他页面或组件调用函数
```javascript
@Output demoCallBack=new EventEmitter(); 
this.demoCallBack.emit();
```
```html
<aui-demo (demoCallBack)='demo()'></aui-demo>
demo{}
```
* * *
elementRef
nativeElement

## 其他
### _result使用

# 错误总结
* * *
### 空值处理
> 容易遗漏，一般采用判断语句

## 函数返回值为布尔类型
```javascript
return (demo); //返回表达式
```


# 软件使用
* * *

