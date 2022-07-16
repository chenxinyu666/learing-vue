1、{{}}：不能作用在标签的属性上，只能在标签内部用
2、v-text：以文本格式显示在标签内部
3、v-html：以html格式显示在标签内部
4、v-bind：给标签属性赋值，v-bind:属性名="Vue对象中的值"
5、v-on：给标签绑定事件 v-on:事件名="函数名或表达式"
                                      @事件名="函数名或表达式"
                                                   .prevent：阻止标签的默认事件
                                                   .once:       事件只触发一次
                                                   .stop:        阻止事件冒泡
                                                   .self:         阻止所有子元素的事件冒泡
                                                   .capture:   事件捕获
6、v-if：满足条件的标签才会在DOM中渲染
7、v-show：带有v-show的标签始终会被渲染并保留在DOM中，v-show只是简单地切换标签的CSS的display属性来决定标签是否显示
8、v-for：被遍历的对象可以是number，string，array，object，Iterable
              (1):  (item,index) in items
              (2):  (value,key,index) in object
                   index可选
9、v-model: 在<input>、<textarea>和<select>标签上创建双向数据绑定，需要在Vue对象中给标签声明初始值;
    单个复选框，v-model只绑定布尔类型的值，即复选框是否被选中;
    多个复选框，v-model绑定数组，选中的元素添加到数组中;
    v-model用于下拉列表，下拉列表最终选中的选项对应的value会绑定到对应的属性上；(如果没有设置选项的value，会将标签内部的文字作为value）
        修饰符：
                    (1).lazy：绑定的数据在change事件之后进行同步
                    (2).number：将输入值转为数值类型
                    (3).trim：过滤首尾空格
10、<template>：按条件显示，源代码中不渲染<template>标签
11、Vue对象的computed属性，能够在取值和设值之前进行计算。
        get函数使用的数据如果发生了改变，会自动重新计算。
        将函数绑定到输入标签上，实际上绑定的是set函数
12、Vue对象的watch属性，侦听的都是data中的属性，当被侦听属性发生改变时，调用函数
        这种方式只能侦听一个属性调用一个函数。