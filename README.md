# 选项卡切换 组件


这是一款基于jQuery的选项卡切换插件，特点如下：
1. 支持 click, mouseover, mousedown, dblclick 等N类鼠标事件；
2. 标签内部可以使用超链接；
3. 支持Ajax方式载入内容；
4. 支持多层嵌套，理论上可以实现无限层级的嵌套切换；

## 参数

``` javascript
// ES6
import tab from 'jquery-tabs';
tab({ selector , [start], [event], [delay], [selected], [callback] });
```

``` js
// jquery plugin
$(selector).tabs([start], [event], [delay], [selected], [callback]);
```

### 参数

|名称	|类型	|默认值	|描述
| :--------|:--------|:--------|:--------|
|selector	|jQuery可用的选择器	|null	|必选参数。绑定切换事件的标签的父容器，可以为使用jQuery选择器匹配的一个或多个对象。例如："#id", ".className"
|start	|Integer, String	|0	|可选参数。默认显示容器的索引或id。如果为整数，则默认显示索引值为该值的容器，该值从0开始；如果为"#"开始的字符，则默认显示id为该值的容器；
|event	|String	|"click"	|可选参数。触发切换事件的动作。可使用以下鼠标动作：click, mouseover, mousedown, mouseup, dblclick, mouseenter, mouseleave, mouseout
|delay	|Integer	|150	|可选参数。切换事件延时毫秒(ms)数。该参数只有在 action 为 mouseover, mouseenter, mouseleave, mouseout 时才有效。
|selected	|String	|".selected"	|可选参数。当前标签的样式名，该字符串是否以"."开始皆可。
|callback	|Function	|$.noop	|可选参数。每次切换完成后的回调函数。function(id){//do something}回调函数中可以使用返回值id,即当前需要展示的内容标签id。可以结合"id"进行相应的操作，或者Ajax载入内容。
