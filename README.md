# 前端面试题
### 1、解决版本冲突
* 冲突情况：服务器代码和自己代码改动的地方相同
* 将自己的代码保存一份到本地，然后直接将服务器代码更新下来，然后在新的代码上修改自己的逻辑

### 2、上拉加载原理
* 监听 scroll、touch事件
* 判断 滚动距离

### 3、setTimeout核心作用
* 定时器
* 轮播图
* 动画效果
* 自动滚动
* 执行一次指定代码，使用clearTimeout清除定时器对象

### 4、setInterval
+ 不断地执行指定代码，直到调用clearInterval清除定时器对象

### 5、雪碧图
* CSS Sprite，也叫CSS精灵，CSS图像合并技术
+ 是将小图标和宽高固定的背景图片合并到一张图片上，利用css的背景定位来显示需要显示的图片部分
* 优点
  * 减少加载网页图片时对服务器的请求次数
  * 提高页面的加载速度
  * 不失真 

### 6、开发过程
+ 1/3时间  需求分析  产品经理
+ 1/6时间  编码
+ 1/2时间  测试
 + 性能测试
   + 网页访问速度不能超过3秒  
 + 业务测试

### 7、清除浮动
+ display: block 变为 块元素
+ overfolw: hidden
+ :before / :after 伪元素 清除浮动
+ clear: both

### 8、BFC
+ 解决高度塌陷，通过overflow: hidden开启
 + 开启BFC以后，子元素的垂直外边距不会传递给父元素
 + 开启BFC以后，元素不会被浮动的元素所覆盖
 + 开启BFC以后，父元素可以包含浮动的子元素

### 9、CSS方法隐藏元素	
+ display : none  看不见摸不到
+ visible : hidden  看不见摸得到，占空间 
+ opacity : 0 透明度为0
+ 宽高设为0，然后overfolw: hidden  隐藏

### 10、css引入方式
+ 直接在html标签里面引入，或者在html文件前面声明
+ 在style标签内写样式
+ 通过link导入样式
+ 通过@import导入样式
 + link和@import的区别
   + link网页主题装载前就先装载CSS 
   + @import有数量限制，而且是先等网页加载完再引入样式，如果网页足够大，则可	   能出现闪烁，就是漫长的无样式网页加载之后，css突然出来

### 11、同源
+ 协议、域名、端口 相同

### 12、relative与absolute
+ relative
  + 相对于自身在文档流中的位置，相对定位会提升元素的层级
+ absolute
  + 相对于离他最近的，开启了定位的，祖先元素进行定位，如果所有的祖先元素都没有开启定位 则相对于浏览器窗口进行定位一般情况下开启一个元素的绝对定位时，都会同时开启它父元素的相对定位，会提升元素的层级
+ 3、fixed
  + 相对于浏览器视口

### 13、懒加载、预加载
+ 懒加载也叫延迟加载：符合某些条件时才加载某些图片
+ 预加载是提前加载图片，当用户需要查看时可直接从本地缓存中渲染

### 14、img标签上的title和alt区别
+ title属性是在你鼠标悬停在该图片上时显示一个小提示，鼠标离开就没有了，类似hover，title专门做提示的
+ alt是图片不能正常加载时候显示的提示语

### 15、面向对象
+ 把数据及对数据的操作方法放在一起，作为一个相互依存的整体——对象
+ 面向对象特点
  + 封装、继承、多态

### 16、快速点击
+ 设置点击时间，几秒后才能再次点击

### 17、块级.内联元素
+ 块级元素
  + 总是在新行上开始，占据一整行
  + 高度，行高以及外边距和内边距都可控制
  + 宽带始终是与浏览器宽度一样，与内容无关
  + 它可以容纳内联元素和其他块元素
  + div、form、table、p、H1-H6、ul
+ 内联元素
  + 和其他元素都在一行上
  + 高，行高及外边距和内边距部分可改变
  + 宽度只与内容有关
  + 行内元素只能容纳文本或者其他行内元素
  + 不能设置宽高，其宽度随着内容增加，高度随字体大小而改变，内联元素可以设置外边界，但是外边界不对上下起作用，只能对左右起作用，也可以设置内边界，但是内边界在ie6中不对上下起作用，只能对左右起作用 
  + a、span、label、input、img、br
  
### 18、事件委托/事件代理
+ 利用事件冒泡原理，让父元素代替执行
 + 事件冒泡：就是事件向上传导
  + 大部分情况下冒泡都是有益的，都是对我们开发的简化。但是有些情况下，我们不希望发生事件的冒泡，来取消冒泡
    + stopPropagation()       
    + stopImmediatePropagation()	

### 19、停止事件冒泡、阻止默认行为
+ 停止事件冒泡
  + stopPropagation
  + IE浏览器中  cancelBubble
+ 阻止默认行为
  + preventDefault
  + IE浏览器中  window.event.returnValue = false;

### 20、如何区分 HTML 和 HTML5
+ 在文档类型声明上不同
+ 在结构语义上不同

### 21、浏览器内核
+ IE：trident
+ Chrome
  + js引擎：V8引擎
  + 渲染引擎：webkit 
+ Firefox：gecko

### 22、同步、异步区别
+ 同步：阻塞
  + 浏览器向服务器请求数据，服务器比较忙，浏览器一直等着（页面白屏），直到服务器返回数据，浏览器才显示页面
+ 异步：非阻塞 (async = true)
  + 服务器返回数据的时候通	知浏览器一声，浏览器把返回的数据渲染到页面上，局部刷新

### 23、原型
+ 每个函数都有一个prototype属性, 它默认指向一个Object空对象 (即为: 原型对象)

### 24、闭包
+ 函数嵌套
+ 内部函数引用外部函数的局部变量
+ 外部函数调用返回的是内部函数的句柄
+ 闭包也是一个对象，对象的本质是管理保存变量
  + 作用
    + 延长外部变量的生命周期
 + 注意
   + 内存消耗很大，在IE中可能会内存泄漏
   + 在退出函数之前，删除不用的局部变量
 + 使用场景
   + 采用函数引用方式的setTimeout调用
   + 将函数关联到对象的实例方法
   + 封装相关的功能集
   + 写插件时会用到，jQuery就是闭包的形式
   + 通过循环给页面上多个dom节点绑定事件
   + 封装变量
   + 延续局部变量寿命 
 + 用途
   + 匿名函数执行函数
   + 结果缓存
   + 实现类和继承
   + 读取内部函数变量
![](https://i.imgur.com/CKpvfmG.png)  
 + 哪些操作会造成内存泄漏
   + 闭包
   + 循环
   + 控制台日志

### 25、DOM	
+ 文档对象模型
+ 是W3C的标准

### 26、DOM事件流/事件传播机制
+ 事件捕获阶段
  + 事件从最上一级标签开始往下查找，直到捕获到事件目标(target)
+ 处于目标阶段
+ 事件冒泡阶段
  + 事件从事件目标(target)开始，往上冒泡直到页面的最上一级标签

### 27、正则表达式
+ 手机号码 
  + ^1[3|4|5|7|8][0-9]{9}$ 
  + ^((\+86)|(86))?(13)\d{9}$ 
+ 固话 区号3-4位，第一位为0，中横线，7-8位数字，中横线，3-4位分机号
  +  ^[0]\d{2,3}\-\d{7,8}\-\d{3,4}$
+ 电子邮件地址的正则表达式	
  + /^[a-zA-Z0-9_-]+@[a-zA-Z0-9_-]+(\.[a-zA-Z0-9_-]+)+$/
+ 字母开头，其余由数字、字母、下划线组成的6~30的字符串
  + ^[a-zA-Z]{1}[\W]{5,29}$ 
+ 最短6位，最长20位，数字和字母组成
  + ^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])[a-zA-Z\d]{6,20}$
 
### 28、HTTP版本
+ 0.9
+ 1.0
+ 1.1 最广泛
+ 2.0   

### 29、HTTP状态码 
+ 200 成功
+ 304 重定向
+ 404 客户端错误
+ 500 服务器端错误

### 30、Ajax (Asynchronous JavaScript And XML)
+ 异步通信
+ 不用刷新整个页面就能请求数据
+ 比如：地图的缩放、收货地址的三级联动
  + 优点
    + 异步通信、局部刷新、按需加载、节约带宽
  + 缺点
    + 无历史记录，不能回退、对搜索引擎支持较弱、暴露了与服务器交互的细节
 
### 31、跨域的几种方法
+ jsonp (JSON with Padding)
  + jsonp是一种“技巧”
  + 利用scirpt标签的src属性不受跨域的限制的特点
  + 解决跨域
    + 浏览器端
      + 动态生成script标签，提前定义好回调函数，在合适的时机添加src属性				指定请求的地址
    + 服务器端
      + 后台接收到回调函数，将数据包括在回调函数调用的句柄中，一起返回
    + 只能发送get请求
+ jsonp写法
```
  $.ajax({
              type: "get",
              async:false,
              url: "http://192.168.1.102:8080/carop/jsonp",
              data: {“name”:"VUE"},	//参数
	      dataType: "jsonp",
	      jsonp:"",
              jsonpCallback:"jsonpCallback",              
              success: function(data){
		  //业务处理
		alert(data.name+"\n "+data.tel);
              },
	      error:function(msg){
		 //执行错误
	      }
          }); 
	  
type:请求提交的 方式
async:是否同步
url：请求地址
data:待发送Key/value参数
dataType:请求的数据类型，是使用jsonp这种跨数据访问协议的json数据格式还是用其他的数据格式
jsonp:有了这个参数，那么实际请求的url地址会变成http://b.com/index.php?callback=?,如果jsonp设置为test111,那么请求地址就是           	http://b.com/index.php?test111=?
jsonpCallback:定义回调函数的名称，和上面的参数jsonp一起使用，如果这个参数为myCallback,请求的地址会变成http://b.com/index.php?callback=myCallback,另外值得注意的是，如果这个值为空的话，那么jquery会默认随机生成一个函数名传过去，那么实际请求的地址就是：http://b.com/index.php?callback=jquery12253158788754457
success:请求响应 成功的回调
error:请求响应 失败的回调
```
+ cors
  + cors是一门技术，在本质上让ajax引擎允许跨域 
	 + 浏览器端什么也不用干
	 + 服务器端设置响应头：Access-Control-Allow-Origin
	 + 支持get和post请求
	 + 兼容IE8 
+ 服务器跨域
+ postmessage跨域

### 32、Ajax的状态值
+ 0: (未初始化) 还没有调用send()方法
+ 1: (载入) 已经调用send()方法，正在派发请求
+ 2: (载入完成) send()已经执行完成，已经接收到全部的响应内容
+ 3: (交互) 正在解析响应内容
+ 4: (完成) 响应内容已经解析完成，用户可以调用

### 33、Ajax拿到数据怎么处理
+ Ajax成功回调的函数返回的数据在回调函数的参数里，直接将参数赋值给其他变量就	可以实现回调获得的数据传递给函数外的变量，进而可以供其他的函数使用该数据

### 34、Ajax原理
+ Ajax的原理简单来说通过XmlHttpRequest对象来向服务器发异步请求，从服务器获	   得数据，然后用javascript来操作DOM而更新页面
+ XMLHttpRequest是在IE5中首先引入的是一种支持异步请求的技术。javascript可以	   及时向服务器提出请求和处理响应，不阻塞用户，达到无刷新的效果

### 35、Ajax的过程
+ 创建XMLHttpRequest对象，也就是创建一个异步调用对象
+ 创建一个新的http请求，并指定该http请求的方法、URL及验证信息
+ 设置响应http请求状态变化的函数
+ 发送http请求
+ 获取异步调用返回的数据
+ 使用JavaScript和DOM实现局部刷新

### 36、Ajax请求参数get、post区别
+ get：请求数据 (安全性低)
  + 请求可被缓存
  + 请求保留在浏览器历史记录中
  + 请求可被收藏为书签
  + 请求不应再处理敏感数据时使用
  + 请求有长度限制
  + 请求只应当用于取回数据
+ post: 提交数据
  + 请求不会被缓存
  + 请求不会保留在浏览器历史记录中
  + 不能被收藏为书签
  + 对数据长度没有要求
  + 向服务器发送大量数据
  + 发送包含未知字符的用户输入时，POST 比 GET 更稳定也更可靠

### 37、性能优化的办法
+ 减少HTTP请求
+ 文件最小化
+ 启用缓存
+ 使用CDN托管
+ 文件合并
+ 精简代码
+ 使用浏览器缓存
+ 使用压缩组件
+ 图片、JS的预载入
+ 将脚本放在底部
+ 将样式文件放在页面顶部
+ 使用外部的JS和CSS
+ 少用全局变量、缓存DOM节点查找的结果。减少IO读取操作

### 38、优化的作用
+ 提升网页 响应速度
+ 提高可读性、可维护性

### 39、如何优化代码
+ 注释
+ 代码复用

### 40、SEO（搜索引擎优化）
+ 网站结构调整
+ 内容建设
+ 代码优化

### 41、CDN（内容分发网络）
+ 尽可能的避开互联网上有可能影响数据传输速度和稳定性的瓶颈和环节，使内容传输的更快、更稳定
+ 访问速度有保障，稳定性也有保障
+ 省下资源服务器的一部分资源负担，节省空间节省流量

### 42、CDN的好处
+ 有利于Google的排名
+ 有利于转化
+ 网站不容易挂机
+ 减少托管的成本

### 43、页面从输入url到页面加载显示完成
+ 输入地址
+ 浏览器查找域名的IP地址
+ 浏览器先从web服务器发送一个http请求
+ 服务器的永久重定向响应
+ 浏览器跟踪重定向地址
+ 服务器处理请求
+ 服务器返回一个http响应
+ 浏览器显示HTML
+ 浏览器发送请求获取嵌入在HTML中的资源（图片..）
+ 浏览器发送异步请求（如Ajax请求）
+ 页面构建完成

### 44、页面的重绘、重排	
+ "重绘"不一定需要"重排"，比如改变某个元素的颜色，只会触发"重绘"，不会触发"重排"，因为布局没有改变
+ "重排"一定会"重绘"

### 45、浏览器的渲染过程
+ 浏览器解析html源码，然后创建一个DOM树
+ 浏览器解析CSS代码，计算出最终的样式数据
+ 构建出DOM树，并且计算出样式数据，构建一个渲染树
+ 浏览器就根据渲染树把页面绘制到屏幕上

### 46、HTML标签
+ head
+ meta
+ title
+ link
+ style

### 47、H5新特性
+ 语意化元素 
  + 如 header、footer、length、remove	有利于搜索引擎优化和快速查找   
+ 音频和视频
+ 本地离线存储 
  + localStorage 长期存储数据，浏览器关闭后数据不丢失
  + 会话存储 sessionStorage 的数据在浏览器关闭后自动删除
+ canvas绘图功能
+ 地理位置
+ 表单控件
  + date日期、time、search
  + number : 只能包含数字的输入框	

### 48、浏览器上多个标签页间的通信
+ 使用cookies
+ 使用localStorage 本地储存方式

### 49、cookie默认过期时间
+ 默认cookies生存期限 就到 关闭浏览器 为止

### 50、如何保证cookie的安全
+ 1、这两个前缀分别为 __Secure- 和 __Host- ，它们会被用作 Cookie 名称的前缀而非数值。如果你的网站有一个名为 sid 的 Cookie，那么为了发挥 Cookie 前缀的优势，应当将名称改为 __Secure-sid
```
2、__Secure- 前缀
   a、如果 Cookie 名称带有 __Secure- 前缀，那么它肯定具有 Secure 属性并且被设置为来源于一个安全的源
   b、告诉浏览器需要设置 Secure 属性
3、__Host- 前缀
  a、如果 Cookie 名称带有 __Host- 前缀，那么它也肯定会具有 Secure 属性，而不应当具有 Domain 属性，因为 Cookie 只作用于同源的网站，必须设置Path=/ 
  b、告诉浏览器同时需要设置 Path=/ 和 Secure 属性，同时不应当设置 Domain 属性
4、注意
  //支持 __Secure 前缀的浏览器会拒绝以下连接，因为缺少 Secure 属性
  document.cookie = '__Secure-invalid-without-secure=1';
    
  //所有浏览器包括支持 __Secure 前缀的浏览器都会接受以下连接，因为设置了 Secure 属性
  document.cookie = '__Secure-valid-with-secure=1; Secure';
  
  //支持 __Host 前缀的浏览器会拒绝以下连接，因为缺少 Secure 和 Path=/ 属性
  document.cookie = '__Host-invalid-without-secure-or-path=1';
  
  //支持 __Host 前缀的浏览器会拒绝以下连接，因为缺少 Path=/ 属性，即使设置了  Secure 属性
  document.cookie = '__Host-invalid-without-path=1; Secure';
  
  //所有浏览器包括支持 __Host 前缀的浏览器都会接受以下连接，因为同时包含了 Secure 和 Path=/ 属性
  document.cookie = '__Host-valid-with-secure-and-path=1; Secure; Path=/';
	  
```

### 51、CSS3新特性 
+ 背景
+ 字体样式
+ 2D/3D转换
+ 动画
+ 过渡
+ 圆角
+ 旋转
+ 多列布局

### 52、jQuery (write less,do more)
+ 功能丰富的JS函数库、项目开发首选
+ 主要用于PC端
+ 封装简化DOM操作
+ 增删改查操作
+ jQuery的所有的功能都需要通过核心函数来实现
+ 主要功能是选择器
+ 属性的修改和绑定
+ jQueryMobile用于移动端

### 53、jQuery版本
+ 1.x	兼容老版本IE
+ 2.x 兼容新版本IE（已停止更新）
+ 3.x	兼容新版本IE

### 54、jQuery的attr和prop方法区别
+ attr
  + 如果有相应的属性，返回指定属性值
  + 如果没有相应的属性，返回值是undefined
  + 获取匹配的元素集合中的第一个元素的属性的值,或设置每一个匹配元素的一个或多个属性
  + 对于HTML元素我们自己自定义的DOM属性，在处理时，使用attr方法
+ prop
  + 如果有相应的属性，返回指定属性值
  + 如果没有相应的属性，返回值是空串
  + 获取匹配的元素集中第一个元素的属性（property）值,或设置每一个匹配元素的一个或多个属性
  + 对于HTML元素本身就带有的固有属性，在处理时，使用prop方法

### 55、zepto
+ 函数库
+ 移动端框架
+ 轻量级，8kb
+ 封装简化DOM操作

### 56、zepto解决了tap事件点透
+ 出现场景
  + 因为click延迟
  + A/B两个层上下z轴重叠
  + 上层的A点击后消失或移开
  + B元素本身有默认click事件（如：a标签）或B绑定了click事件
  + （zepto的tab事件有点透问题，新版的已修复）
+ 解决
  + 用touchend代替tap事件并阻止掉touchend的默认行为preventDefault()

### 57、angular
+ 结构化框架 
+ 动态展示页面数据、与用户进行交互 
+ 双向数据绑定
+ 声明式依赖注入
+ 表单验证
+ Ajax封装
+ 单页面Web应用（局部刷新）
+ 完善的页面指令
+ 解耦应用逻辑，数据模型和视图
+ angular解决了 单页面应用、跳转、无法回退

### 58、react
+ 结构化框架、动态构建用户界面的js库
+ 高效
+ 单向数据流
+ 单页面应用
+ 声明式编码
+ 组件化编码
+ 虚拟DOM
+ 支持客户端 和 服务器渲染

### 59、react的生命周期
+ 创建  
  + getDefaultProps
  + getInitialState
+ 实例化	componentWillMount
+ 更新 render
+ 销毁 componentDidMount

### 60、react高效的原因
+ 虚拟DOM，不是直接操作DOM
+ 高效的DOM Diff算法，最小化页面重绘

### 61、虚拟DOM
+ 虚拟DOM是在DOM的基础上建立了一个抽象层，我们对数据和状态所做的任何	   改动，都会被自动且高效的同步到虚拟DOM，最后再批量同步到DOM中
+ 虚拟DOM具有批处理和高效的Diff算法，可以无需担心性能问题而随时“刷新”整个页面，因为虚拟DOM可以确保只对界面上真正变化的部分进行实际的DOM操作
  + 优点
    + 最终表现在DOM上的修改只是变更的部分，可以保证非常高效的渲染
  + 缺点
    + 首次渲染大量DOM时，由于多了一层虚拟DOM的计算，会比innerHTML插入慢

### 62、Vue		
+ MVVM框架
+ 双向数据绑定
+ 单页面应用
+ 虚拟DOM
+ 组件化、模块化、工程化
+ 体积小、效率高、编码简洁、PC/移动端 都合适
+ vue.js不支持IE8及以下版本

### 63、Vue原理
+ 实现 （数据监视器） Observer
+ 实现 （指令解析器） Compile
+ 实现 （桥梁） Watcher
+ 实现 （入口函数） MVVM

### 64、MVVM原理
+ 双向数据绑定
+ View - Model：DOM Listeners （DOM监听）
+ Model - View：Date Bindings （数据绑定）

### 65、MVVM
+ 解决了js混乱，便于管理  
+ 优点
  + 低耦性
  + 可重用性
  + 孤立开发
  + 可测试性
+ 缺点
  + 内存消耗很大

### 66、Vue指令
* v-text : 当作 纯文本
* v-html : 将value作为 html标签来解析
* v-if : 用于在运行条件下不大可能改变
* v-else : 与v-if一起使用, 如果value为false, 将当前标签输出到页面中
* v-show : 用于频繁切换
* v-for : 遍历，用于列表
* v-on : 绑定事件监听
* v-bind : 强制绑定 解析表达式
* v-model ： 双向数据绑定

### 67、vue传参
+ vue父组件向子组件传参 props
+ vue父组件获取子组件 ref
+ vue子组件向父组件 emit
+ vue组件间传参 vuex

### 68、Vue全家桶
+ vue-cli 脚手架
  + 自动生成模板工程、目录结构、本地调试、热加载、单元测试
+ vue-router
+ vue-resource  资源
+ vuex 状态管理模式

### 69、Vuex 
+ 状态管理模式
  + state：驱动应用的数据源 (数据)
  + view：以声明方式将state映射到视图 (界面)
  + actions：响应在view上的用户输入导致的状态变化 (方法)
  + 把组件的共享状态抽取出来，以一个全局单例模式管理。在这种模式下，我们的组件树构成了一个巨大的“视图”，不管在树的哪个位置，任何组件都能获取状态或
者触发行为
+ 组件间传参（交互）
+ 单向数据流	
+ vuex解决了
  + 组件之间共享同一状态的问题
  + 单一状态树管理，让数据的修改脉络更加清晰，便于定位的问题	 
+ 用于构建 中、大型 单页应用，更好地在组件外部管理状态 

### 70、Vue生命周期
+ 8个阶段：
  + beforeCreate  （创建前）
  + created       （创建后）
  + beforeMount  （载入前）
  + mounted      （载入后）
  + beforeUpdate  （更新前）
  + updated       （更新后）
  + beforeDestroy  （销毁前）
  + destroyed      （销毁后）
+ beforecreate : 可以在这加个loading事件
+ created ：结束loading，还做一些初始化，实现函数自执行 
+ mounted ： 发起后端请求，拿回数据，配合路由钩子做一些事情
+ beforeDestory： 你确认删除XX吗？ destoryed ：当前组件已被删除，清空相关内容    

### 71、vue获取DOM元素
+ 在vue中可以通过给标签加ref属性，就可以在js中利用ref去引用它，从而操作该dom元素
 ```
<template>  
  <div>  
    <div id="box" ref="mybox">  
      DEMO  
    </div>  
  </div>  
</template>  
  
<script>  
export default {  
  data () {  
    return {  
        
    }  
  },  
  mounted () {  
    this.init();  
  },  
  methods:{  
    init() {  
      const self = this;  
      this.$refs.mybox.style.color = 'red';  
      setTimeout(() => {  
        self.$refs.mybox.style.color = 'blue';  
      },2000)  
    }  
  }  
  
}  
</script>  
  
<style scoped>  
  #box {  
    width: 100px;  
    height: 100px;  
    line-height: 100px;  
    font-size: 20px;  
    text-align: center;  
    border: 1px solid black;  
    margin: 50px;   
    color: yellow;  
  }  
</style>  
 ```

### 72、ES6声明块级作用域
+ let、const

### 73、var、let、const区别
+ var
  + 声明的变量，没有块的概念，可以跨块访问, 不能跨函数访问
  + 变量，作用域为该语句所在的函数内，在定义语句前就可以访问到，变量提升
+ let
  + 只能在块作用域里访问，只能在当前作用域中访问
  + 没有变量提升，在声明之前无法访问
  + 不能声明一个变量两次
  + 应用：循环遍历加监听   
+ const
  + 用来定义常量，使用时必须赋值，只能在块作用域里访问，不能修改
  + const声明的变量如果保存的是一个对象，则可以修改对象的属性 
+ 如果变量有可能修改则用let，如果 不修改 则用const

### 74、mock数据
+ 数据的 结构、类型 不变
+ 值 可变

### 75、react 和vue的区别
+ 性能上vue比react好，用的是双向绑定机制
+ react用的是differ算法，走的是dom树渲染
+ 使用上vue对工具的使用者更友好，声明式编码的的封装性更高
+ react有更强大的社区和更完善的解决问题的方案
+ 对DOM的渲染方式不同
  + vue可以直接在vue文件中使用html标签，数据绑定时类似angular，可以进行条件渲染
  + react.js则采用了jsx语法，运用虚拟DOM的概念进行DOM对页面元素进行渲染，获取页面元素需要用ref来获取，更加安全

### 76、px、em和rem的区别	
+ px是绝对单位，相对于显示器分辨率
+ em 相对父元素  通常1em = 16px
+ rem相对于根元素<html>，只要在根节点设定好参考值，那么全篇的1rem都相等，1rem = 16px

### 77、rem的值
+ 根据js来调整html的字号
+ 通过媒体查询来调整字号

### 78、1像素边框（移动端）
+ devicePixelRatio的官方的定义为：设备物理像素和设备独立像素的比例，也就是devicePixelRatio = 物理像素 / 独立像素 
+ 0.5px边框  border-width：0.5px
+ border-image	border-image: url(../img/linenew.png) 0 0 2 0 stretch
+ background-image	将边框模拟在背景上
+ 背景渐变  设置1px的渐变背景，50%有颜色，50%透明
+ box-shadow模拟边框	阴影处理的方式实现0.5px的效果
+ viewport + rem
+ 伪类 + transform 	
  + 把原先元素的 border 去掉，然后利用 :before 或者 :after 重做 border ，把 transform 的 scale 缩小一半，原先的元素相对定位，新做的 border 绝对定位比较完美的方法了
+ 用于 导航栏边线

### 79、移动端适配/兼容
+ mete 完美标签
+ rem适配
+ viewport
+ 清除默认样式
+ 清除边框高亮
+ flexbox (伸缩盒模型)

### 80、Flex布局（伸缩盒模型）
+ 用于需要 自适应 宽度或者高度的场景

### 81、移动端事件机制
+ touchstart
+ touchmove
+ touchend

### 82、拖拽(原生js)
+ mousedown  
+ mousemove  
+ mouseup

### 83、CSS选择器的优先级
+ !important 比 内联 优先级高
+ 内联样式    优先级 1000
+ id选择器    优先级 100
+ 类和伪类    优先级 10
+ 元素选择器  优先级 1
+ 通配选择器  优先级 0
+ 继承的样式  没有优先级

### 84、this
+ 全局中的 this 是  window
+ 函数中的this 是 函数所在的对象
+ 对象中的this 是 它本身

### 85、JS继承的6种方法
+ 原型链继承
+ 构造函数继承
+ 组合继承（原型+借用构造）
+ 原型式继承
+ 寄生式组合
+ 寄生组合式继承

### 86、src与href区别
+ src：替换当前元素
+ href：在 当前文档 和 引用资源 之间确立联系

### 87、bind、call、apply区别
+ bind，call，apply都能强制指定this
+ call，apply指定完this后，立即调用当前函数
+ bind绑定完this，不会立即调用，将当前的函数返回
+ call，apply传参形式不一样，apply需要传入数组里
+ bind同call一样，可以直接传参
+ call是将所有的参数一个个传递进去
+ apply是将所有参数放入数组中传递

### 88、node
+ 在V8引擎上运行
+ 适用场景
  + 大量用户访问，低计算量的场景
  + 实时应用：在线聊天
  + 游戏应用
+ 优点
  + 因为Node是基于 事件驱动 和 无阻塞的，所以非常适合处理 并发请求，因此构建在Node上的代理服务器相比其他技术实现（如Ruby）的服务器表现要好的多。与Node代理服务器交互的客户端代码是由javascript语言编写的，因此 客户端 和 服务器端 都用同一种语言编写
+ 缺点
  + Node是一个相对新的开源项目，所以不太稳定，它总是一直在变，而且缺少足够多的第三方库支持

### 89、项目构建工具
+ gulp
  + 一步步来配置环境
+ grunt
+ webpack
  + 配置了大部分需要的环境 
+ 简化项目构建、自动化完成构建
+ 代码转换
+ 文件优化
+ 模块合并
+ 代码分割
+ 自动刷新
+ 代码效验

### 90、TCP与HTTP区别
+ TCP对应于 传输层协议，主要解决数据如何在网络中传输
+ HTTP对应于 应用层协议，主要解决如何包装数据

### 91、rgba、opacity的透明效果
+ rgba: 只作用于 元素的颜色或背景色
+ opacity: 作用于 元素，以及元素内所有内容的透明度 

### 92、JSON（JavaScript Object Natation）
+ 轻量级数据交换格式
+ 是javacscript的一个子集
+ 数据格式简单
+ 易于读写
+ 占用带宽小

### 93、递归
+ 在运行的过程中调用自己

### 94、单页面应用
+ 优点
  + 用户体验好，不需要每次向服务器发送请求页面数据，响应快
+ 缺点
  + 使用浏览器的前进、后退键的时候会重新发送请求，没有合理得利用缓存

### 95、svg (Scalable Vector Graphics)
+ 不失真
+ 可缩放 矢量图形

### 96、可视化工具
+ echarts
  + 是画图表的 
  + 柱状图、折线图、饼图
  + 实现原理：用canvas
+ highcharts
+ d3
  + 更自由些 

### 97、Doctype作用
+ 文档类型 声明
+ 避免浏览器的 怪异模式

### 98、盒子模型
+ 标准W3C 盒子模型
  + border、margin、padding、content
+ IE 盒子模型
  + border、padding、margin、content
  + IE 盒子模型的 content 部分包含了 border 和 pading
+ 盒子的 内容 是否包含 边框 和 内边距

### 99、js的基本数据类型
+ string
+ number
+ boolean
+ null 
+ undefined

### 100、对象引用类型 
+ Object -- typeof/instanceof
+ Array -- instanceof
  + 数组 也是 对象
+ Function -- typeof

### 101、为什么会出现 引用类型
+ 基本数据 类型存储在 栈中
+ 引用数据 类型存储在 堆中

### 102、基本内置对象
+ Array对象
+ Date对象
+ 正则表达式 对象
+ String对象
+ Global对象

### 103、MongoDB的类型
+ 基于 分布式 文件存储的数据库

### 104、Hbuilder与WebStorm区别
+ Hbuilder 写 H5 比较好
+ Webstorm 写 js 比较好
+ Bracket 写 CSS 比较好
+ Sublime 写 HTML + CSS比较不错，轻便，插件安两个就行，一个是packagecontrol,一个是emmet

### 105、深度克隆 (Deep Clone)
+ 所有元素或属性均完全复制，与原对象完全脱离，也就是说所有对于新对象的修改都不会反映到原对象中

### 106、动画
+ 不复杂 的动画可以用css实现
+ 复杂的，或者需要 交互的 时候，用js

### 107、前端调试工具
+ Chrome的开发者工具
+ Firefox插件Firebug
+ IE的开发者工具
+ IETest，IE浏览器版本切换工具

### 108、new做了什么
+ 创建一个新对象
+ 将构造函数的作用域赋给新对象（因此 this 就指向了这个新对象）
+ 执行构造函数中的代码（为这个新对象添加属性）
+ 返回新对象

### 109、百度地图定位
+ PC端
  + IP地址
+ 手机定位
  + GPS、基站定位

### 110、版本控制工具
+ SVN -- CollabNet Subversion
+ GIT -- 最先进的分布式版本控制系统
+ VSS -- Visual Source Saf （Microsoft提供的）
+ CVS -- Concurrent Versions System

### 111、如果你有无穷多的水，一个3公升的捅，一个5公升的捅，两只提捅形状都不均匀，如何才能准确称出4公升的水?
+ 用5升桶 满桶，倒入3升桶中，倒满后大桶里剩2升
+ 把3升桶 倒空，把那2升倒入3升桶中
+ 用5升桶 满桶再向3升里倒，倒入一升就满，大桶里剩下的是4 升
---

### 112、display属性
+ display:block  行内元素 转换为 块级元素
+ display:inline  块级元素 转换为 行内元素
+ display:inline-block  转为 内联元素

### 113、块级元素
+ address – 地址
+ blockquote – 块引用
+ center – 举中对齐块
+ dir – 目录列表
+ dl – 定义列表
+ fieldset – form控制组
+ form – 交互表单
+ hr – 水平分隔线
+ isindex – input prompt
+ menu – 菜单列表
+ noframes – frames可选内容，（对于不支持frame的浏览器显示此区块内容）
+ noscript – 可选脚本内容（对于不支持script的浏览器显示此内容）
+ pre – 格式化文本
+ table – 表格

### 114、内联元素
+ abbr – 缩写
+ acronym – 首字
+ b – 粗体
+ big – 大字体
+ br – 换行
+ em – 强调
+ i – 斜体
+ label – 表格标签
+ s – 中划线
+ small – 小字体文本
+ strike – 中划线
+ strong – 粗体强调
+ sub – 下标
+ sup – 上标
+ textarea – 多行文本输入框
+ tt – 电传文本
+ u – 下划线

### 115、var numberArray = [3,6,2,4,1,5]
+ 倒排，输出[5,1,4,2,6,3]
  * numberArray.reverse()
+ 降序排列，输出[6,5,4,3,2,1]
  * numberArray.sort(function(a,b){return b-a})

### 116、输出今天的日期，以YYYY-MM-DD的方式
 ```
 var d = new Date();
 // 获取年，getFullYear() 返回4位数字
 var year = d.getFullYear();
 // 获取月，月份比较特殊，0是1月，11是12月
 var month = d.getMonth() + 1;
 // 变成两位
 month = month < 10 ? '0' + month : month;
 // 获取日
 var day = d.getDate();
 day = day < 10 ? '0' + day : day;
 alert(year + '-' + month + '-' + day);
 ```
### 117、documen.write、innerHTML的区别
+ document.write 只能重绘 整个页面
+ innerHTML 可以重绘页面的 一部分

### 118、jQuery框架中$.ajax()的常用参数有哪些？写一个post请求并带有发送数据和返回数据的样例
+ async 是否异步
+ url 请求地址
+ contentType 发送信息至服务器时内容编码类型
+ data 发送到服务器的数据
+ dataType 预期服务器返回的数据类型
+ type 请求类型
+ success 请求成功回调函数
+ error 请求失败回调函数	
```
  $.ajax({
        url: "/jquery/test1.txt",
        type: 'post',
        data: {
            id: 1
        },
        success: function(data) {
            alert(data);
        }
    }
```

### 119、js延迟加载的方式
+ defer属性
+ async属性
+ iframe方式
+ 动态创建 <script>标签
+ 使用jQuery的 getScript()方法
+ AJAX eval（使用AJAX得到脚本内容，然后通过eval_r(xmlhttp.responseText)来运行脚本）

### 120、jQuery与jQuery UI的区别
+ jQuery 是操作dom的 框架
+ jQueryUI 是基于jQuery做的一个 UI组件库

### 121、箭头函数 特点，数组 map 遍历的方法
+ 箭头函数没有自己的this，在语法上更为简洁。
+ 箭头函数的this不是在调用的时候决定的，是在定义的时候决定的，定义时候所处的对象就是箭头函数的this
+ 箭头函数的this是看外层有没有函数，如果有，和外层的函数指向的是同一个this，如果没有则指向window
```
  arr.map((item, index) => {
      console.log(item, index)
  })
```
### 122、promise 对象 的原理、作用
+ Promise对象: 代表了 未来 某个将要发生的事件(通常是一个异步操作)
+ ES6的Promise是一个构造函数, 用来生成promise实例
+ 有了promise对象, 可以将异步操作以同步的流程表达出来, 避免了层层嵌套的 回调函数 (俗称'回调地狱')
+ promise有三种状态('初始化状态'， '成功的状态'， '失败的状态')
+ 通过执行异步任务返回的结果(通常是发送ajax请求)来修改promise的状态，
+ 当promise的状态发生改变的时候会调用promise的实例中的then方法的成功或者失败的回调函数，去执行相应的操作

### 123、package.json 中最重要的 五个属性、作用
```
{
  "name": "npm_command",  //包名（必不可少）
  "version": "1.0.0",  //版本（必不可少）
  "scripts": {  //配置npm运行命令
    "start": "node bin/www"
  },
  "dependencies": {  //运行依赖的包
    "jquery": "^3.2.1"
  },
  "devDependencies": {	//开发依赖的包
    "babel": "^6.23.0"
  }
}
```

### 124、commonjs 和 ES6 模块化暴露的本质分别是什么
```
commonjs 暴露的方式
  1、module.exports = value;
  2、exports.xxx = value;
  
ES6中暴露的方式
  1、export xxx （常规暴露，暴露的本质是对象，接收的时候只能以对象的解构赋值的方式来接收值）
  2、export default （默认暴露，暴露任意数据类型，暴露什么数据类型，接收什么数据类型）
```

###### 本笔记由 靳新喜 &copy; 编写
###### 转载请注明作者信息 &copy;
---  
