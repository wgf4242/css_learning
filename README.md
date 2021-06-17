

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

## 2-5 CSS设计模式完结（3）_.mp4
ITCSS 模型 7层


Settings
Tools 样式工具 clear fix
Generic -- normalize.css
Base
Objects
Components
Trumps 都会加!important 权重变高

ACSS
一个样式属性一个类
好处：极强的利用性、维护成本低
坏处：破坏了css命名的语义化
`<div class="bg-gray-200 p-4></div>`

使用时 SMACSS和ITCSS二选一

## 2-7 CSS架构之Settings层代码实现_.mp4
SASS
定义一些公共变量
公共变量：颜色、边框、字体大小、阴影、层级 

http://sass.hk/docs

https://github.com/ElemeFE/element/blob/dev/packages/theme-chalk/src/common/var.scss



## 2-8 CSS架构之Tools层代码实现（上）_.mp4
引入SassMagic工具库

https://github.com/W3cplus/SassMagic 复制到 src/styles/tools目录下, 去掉些没有的内容

https://cli.vuejs.org/zh/guide/css.html#%E5%90%91%E9%A2%84%E5%A4%84%E7%90%86%E5%99%A8-loader-%E4%BC%A0%E9%80%92%E9%80%89%E9%A1%B9

2.vite.config.js 配置
```js
export default defineConfig({
  resolve: {
    alias: {
        '@': path.resolve(__dirname, 'src')
    }
  },
  css: {
    preprocessorOptions: {
      scss: {
        additionalData: `@import '@/styles/tools/_sassMagic.scss';`,
      },
    },
  },
  plugins: [vue()],
});
```

## 2-10 CSS架构之Base层代码实现（1）_.mp4
npm install normalize.css

Generic层：引入normalize.css 重置浏览器默认样式
Base层： 对各类元素基础样式进行补充

## FAQ

### 1.vite scss add additionalData, 预处理
https://vitejs.dev/config/#css-preprocessoroptions

