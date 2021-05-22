

## 环境配置

npm init @vitejs/app css_project
cd css_project
npm i axios sass mockjs

### mockjs
线上 RAP2
本地 mockjs

## 2-3 css设计模式
### OOCSS
OO 面向对象 ， 就是组件

原则一：容器与内容分离
原则二：结构（基础对象）与皮肤分离
原则二：面向设计开发 


vue中组件 = OOCSS

OOCSS应用：Grid栅格系统、布局组件等

### [BEM](https://en.bem.info/methodology/quick-start/)

块(Block) 元素(Element) 修饰符(Modifier)
作用：命名规范、让页面结构清晰
进阶版的OOCSS

作用于元素 就是元素 --Modifier名字
块名--Modifier名字
Modifier 是不 能单独存在的

### SMACSS
http://smacss.com/
https://github.com/jeffwcx/translate-smacss-zh

分类： Base, Layout、 Modules State Theme
好处：易维护、易利用、易扩展
命名规范：.l-header .is-hidden .theme-nav

替换浏览器默认样式 https://github.com/necolas/normalize.css
 
Base 浏览器的默认样式
Layout 布局方式 前缀 .l-header .l-main .l-footer 
Modules 可复用的样式
State 模块的不同状态的一些样式, 可加前缀 is-hidden
Theme 
