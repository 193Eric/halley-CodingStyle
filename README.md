## 哈雷云前端开发代码规范
### Html规范
>  命名

	class 以小写字母，单词之间以 - 分隔
	class 以模块或者页面内容或功能命名  例如：header-title
	id 必须唯一
	元素属性名，使用小驼峰命名

> 标签

	HTML 标签不要全是div，例如标题h1-h5系列要常用（seo要用到）
	Html5 新增标签要常用（例如header,footer,aside..... 代码易读和便于seo）

> 其他

	图片添加alt 属性（避免加载失败，影响用户体验）
	本地图片不是太大的图片都合成雪碧图，用css背景展示

### Js规范

> 命名，变量

	变量和函数名以小驼峰式命名 例如：submitImage，sendMessage
	常量用const定义，可以公用的放在统一的const.js文件里面，标好注释按需引用。
	减少全局变量的定义（多用局部变量）

> 其他

	减少重复和多余的http请求（性能优化）。
	遇到用到异步的地方，多用promise链式调用，少用回调函数（提升代码可读性）
	不要使用input用来html注入（防止XSS攻击）
	函数里面内容不要太多，尽量一个出口和一个入口（可读性）。
	用“＝＝＝“取代“＝＝“
	不要使用eval()函数
	注释！！！－－－为了方便其它同事，自己写代码的时候一定要写注释；

### Vue

> Vue

	Vue的话，有其他项目适用的公用组件的话，封装好，放到公用包里面，规范按照包里面已封装的组件（halley_packages）。
	data里面的变量和methods里面的函数统一命名为小驼峰 。
	页面初始化需要调用的api数据，放在create生命周期里面（提高页面速度）
	公共组件命名以公司名称简拼为命名空间(app-xx.vue)
	使用export ，import 模块化（公用的filter，const，validate模块管理）
	webpack打包要设置代码混淆