# 一.总述
+ js由三部分组成，ECMAScript,BOM,DOM。其中BOM和DOM统称为web_api。
+ Web Api 是浏览器提供的操作浏览器和页面元素的接口，用于做交互效果

# 二.各部分的标准化组织
+ javascript语法的标准化组织是ECMAscript
+ DOM的标准化组织是W3C
+ BOM缺乏标准，最初是Netscape浏览器的一部分，所有兼容性比较差。

# 三.web_api学习目录
+ 1.Dom文档对象模型
    - 01.获取元素
    - 02.事件三要素
    - 03.修改元素
    - 03.修改元素样式-案例-京东商品tab栏切换
    - 04.设置属性的两种方式
    - 05.H5自定义属性data-
    - 06.按节点层次关系获取节点
    - 07.获取节点-案例-新浪下拉菜单
    - 08.创建添加删除节点
    - 09.克隆节点
    - 10.创建元素的三种方式
    - 11.总结
    - Dom.md
+ 2.Dom事件高级
    - 01.注册事件的三种方式
    - 02.删除事件的三种方式
    - 03.Dom事件流
    - 04.事件对象[兼容性问题]
    - 05.事件对象的target，type属性
    - 06.阻止事件默认行为[兼容性问题]
    - 07.阻止事件冒泡[兼容性问题]
    - 08.事件委托
    - 09.其他鼠标事件-鼠标右击事件-选择文字事件
    - 10.鼠标事件对象之鼠标坐标
    - 11.鼠标坐标-案例-跟随鼠标移动的飞机
    - 12.3种键盘事件
    - 13.键盘事件对象之键的ASCII码值
    - 14.案例-京东按s键自动对焦输入框
    - 15.案例-模拟京东快递单号查询案例
+ 3.Bom浏览器对象模型
    - 01.window顶级对象
    - 02.两种页面加载事件
    - 03.调整窗口大小事件
    - 04.定时器-setTimeout
    - 05.定时器-setInterval-京东倒计时
    - 06.定时器-setInterval-发送手机验证码
    - 07.js执行机制
    - 08.location对象
    - 09.location页面跳转的三种方式及页面刷新-案例-5秒后跳转链接
    - 10.location.search案例-登录页面跳转获取参数
    - 11.navigator 对象
    - 12.history对象
    - Bom.md
+ 4.PC端网页特效
    - 01.element.offset系列属性
    - 02.offset与style的区别
    - 03.offset案例-获取鼠标在盒子中的坐标
    - 04.可拖动的模态框
    - 05.京东放大镜效果
    - 06.element.client系列
    - 07.立即执行函数的两种创建方式
    - 08.像素比,pageshow事件
    - 09.淘宝flexible.js解读
    - 10.element.scroll系列属性
    - 11.仿淘宝固定侧边栏
    - 12.三大系列总结
    - 13.mouseenter与mouseover的区别
    - 14.js动画-封装盒子移动的函数
    - 15.js缓动动画
    - 16.封装缓动动画函数
    - 17.轮播图制作
    - 18.筋斗云导航栏
+ 5.移动端网页特效
    - 01.touch触摸事件
    - 02.触摸事件对象touchEvent
    - 03.移动端拖动元素
    - 04.element.classList的使用
    - 05.移动端轮播图-返回顶部
    - 06.移动端解决点击事件300ms延迟的问题
    - 07.使用fastclclick插件解决触摸的延时问题
    - 08.移动端常见插件的使用
    - 09.移动端常用框架
    - 10.本地存储
    - 11.sessionStorage
    - 12.localStorage
    - 13.记住用户名案例

# 四. 实际开发经验分享

+ 1.总共有两种以上的状态，点击一次就更改一种
    - 对于点击一个按钮，但有多种不同状态的情况，需要设计一个标记值flag来进行状态的更改，即每点击一次，都要修改flag的值。
    - 但对于只有两个状态的情况来说，且恰巧这种两种状态只是为了更改样式，此时可以通过element.classList.toogle()方法来选择使用或删除该样式

+ 2.排他思想
    - 清除所有元素的样式，再为自身添加样式。

+ 3.立即调用定时器
    - 将函数单独写出来，然后先直接调用一次函数，再通过定时器不断的调用函数 

+ 4.日常开发中，若发现代码正确但运行结果不正确，可以通过Ctrl+F5进行强制刷新，避免浏览器缓存的影响

+ 5.自制的js插件最好通过立即执行函数包裹起来，然后把window和document对象作为参数传进去，这样可以防止污染其他的变量


# 五. 实际应用
+ 1.tab栏样式切换
+ 2.下拉菜单的显示
+ 3.留言板
+ 4.跟随鼠标移动的图标
+ 5.快捷键自动对焦输入框
+ 6.输入框放大镜
+ 7.调整窗口大小时自适应布局
+ 8.倒计时
+ 9.发送手机验证码
+ 10.几秒后自动跳转链接
+ 11.可拖动的模态框
+ 12.固定侧边栏，返回顶部
+ 13.盒子匀速移动
+ 14.盒子缓动动画（先快后慢）
+ 15.PC端轮播图（js实现）
+ 16.筋斗云导航栏
+ 17.移动端拖动元素
+ 18.移动端轮播图（CSS3实现）

# 六. 概念性解释
+ 1.什么是DOM事件流
+ 2.什么是事件委托
+ 3.js的执行机制是什么

# 七. 兼容性问题
1.element.dataset
+ 获取自定义属性的值，IE11以上才支持

2.firstElementChild,lastElementChild
+ IE9以上支持

3.nextElementSibling,previousElementSibling
+ IE9以上支持

4.addEventListener
+ IE9以上支持

5.事件对象e,触发事件的对象e.target
+ IE9以上支持

6.e.preventDefault()，e.stopPropagation()
+ IE9以上支持

7.classList
+ IE10以上支持

# 八.待探讨问题
+ 1.NodeList与HTMLCollection的区别