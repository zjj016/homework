# 开发报告</br>
## 一、本站点的策划思路</br>
### 1)为什么做？</br>
	   《福尔摩斯侦探小说全集》是欧美侦探小说的早期经典之作,它以跌宕起伏的情节,缜密的逻辑推理,细致的心理分析以及福尔摩斯这个家喻户晓的侦探形象,打动着我的心。
	    使得同好者不必再去各个网站寻找他需要的信息。
### 2）期望的效果？</br>
		期望达到的效果是网页大方简洁，简单明了，不拖沓。
### 3）内容来源？</br>
		图片来自百度图片，详细内容来自百度百科，视频来自youku视频网站。
## 二、页面结构与说明</br>
		站点有四个页面构成：一个主页面，一个书籍介绍页面，一个影视介绍页面，一个意见反馈页面。
		主页面负责提供跳转其他页面的功能；
		书籍页面负责介绍福尔摩斯系列书籍的详细信息；
		影视介绍页面负责通过视频文字介绍夏洛克系列的影视作品；
		以及一个站长的自我介绍。
		页面的URL地址：
主页面：https://zjj016.github.io/homework/</br>

		

## 三、技术指标</br>
		兼容IE6,7,8,9,10+；使用的HTML版本为4与5，css2和css3，css5；开发工具为sublime，GitHub；


## 四、技术点说明</br>
### 1）技术难点</br>
#### 1.主页面设置时壁纸留白问题：</br>
		难点：调节图片大小和div大小均不能解决
		知识背景：把div的display属性进行改变内边距外边距
		最终解决方法：
		对壁纸设定两个div，然后改变div的display属性
```css
		.a{ 
			display:table;
			width:100%;
			height:auto;
			background:#f00
		}
        
		.b{
            
			width:1200px;
			display:inline-block !important;
			display:inline; 
		}

```
#### 2.内容无法再壁纸上移动</br>
		难点：课堂已知知识无法解决
		知识背景：background-attachment的属性
		最终解决方案：</br>
		（查阅background-attachment的属性)
```
body{
        background-image:url("../picture/form.jpg");/*图片地址*/
        background-repeat:no-repeat;/*询问是否重复图片，选择不重复*/
        background-attachment: fixed; /*定义背景图片随滚动轴的移动方式,fixed是固定于浏览器窗口*/     
    }
```
#### 3.网页出现异常白条 </br>
		难点：body与html界面大小不一致
		知识背景：内边距外边距
		最终解决方案：
        body，html{
		width:100%; 
		height:100%; 
		}

#### 4.git上部分样式不能显示问题
		难点：因为是应用插件的原因，开始时候没有具体熟悉插件的各个代码。	。
		知识背景：修改hosts和bootstrap文件的引用
		最终解决方案：
        1.在网上搜到了解决方案，在此分享以供各位遇到问题的同好参考：在ff的地址栏中输入“about:config”，即进入配置界面。进入后，搜索“security.fileuri.strict_origin_policy”，这是该值应该是true。双击该项，其值自动变为false，即可。修改后，再刷新遇到问题的页面，即可看到正常显示的图标了。那是什么原因导致了这个问题的出现呢？原因是ff的一个安全策略导致的。该策略限制了HTML文件访问不在根目录下的文件夹中的web fonts。这种限制只在本地开发环境下，同时webfonts并未从远程获取时出现。后来看了下前面提到的那个没有出现问题的bootstrap项目。果然，其fonts文件夹被放置在了项目的根目录下。这样即使不去改变上述安全策略，也是可以正常显示的。

#### 5.
## 五、开发心得</br>
### 1.在开发中，技术逐渐熟练，遇到不会的问题，查找解决方案的速度越来越快，逐渐意识到动手实践和自己解决问题的重要性。</br>
### 2.在开发过程中，需要清晰的条例，按部就班，同时css文件与html文件一定要写好格式，便于之后的修改。</br>
### 3.多寻找不同解决方案，在别人的解决方案里面得到自己想要的方法并加以实现。</br>
### 4.多看手册，在不同的标签和属性中，多加实验，研究相关实例得出经验。。</br>
### 5.关于本门课的感想：html技术确实在当今社会相当重要，一个好的网页相当于一个好的门面，老师也是身体力行，手把手教导我们许多标签以及css样式的使用及其细节和注意点。</br>
### 6.关于该课程的展望：老师可以适当多多鼓励学生，毕竟我们基础薄弱，不可能与多年经验的老师相提并论</br>
		

## 六、结合考核要求的关于本作业的内容详细说明</br>
### 1.必须用到的HTML标签（基本用到，根据要求，用到的标签如下）</br>
>		元标记：<title>、<meta>
>		语义类标记 <h1-h2>、<p>、<ul>、<table>、<em>、<pre>、<code>
>		媒体类标记 <a>、<img>、<audio>
>		容器类标记 <div>、<span>、<nav>、<section>
>		表单及其控件：<form>、<input>、<submit>
### 2.必须涉及的CSS知识点（完成）</br>
>		基本排版：各html标记的基本样式设置
>		字体：安全字体（fallback机制）、图标字体icon font
>		横向布局：使用浮动方式实现
>		定位：绝对定位或固定定位
>		背景与边框
>		css特效：2D转换或过渡（每个文件都有使用到）
>		杂项：text-aglin、display等属性的使用
>		移动WEB优化：media query的应用
### 3.javascript要求(完成)
>		使用jquery插件实现至少一个特效或交互效果（在每个页面有使用）
>		自行开发JS脚本实现至少一个特效或交互效果（new.html）
### 4.加分因素（完成）
>		合理的使用了上述未提及的各类前端知识点，如html5和css3新特性、sass等
>		(html5:<address>/<nav>/<section>/<progress>/<acronym>)
>		浏览器兼容性：IE9+兼容，各浏览器表现一致(实现代码如下)
>		(<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">)
>		可访问性：如对听觉设备、打印设备的优化
>		(使用了youku的官方js播放器)
>                 <script type="text/javascript" src="http://player.youku.com/jsapi">
            player = new YKU.Player('youkuplayer',{
            styleid: '0',
            client_id: 'YOUR YOUKUOPENAPI CLIENT_ID',
            vid: 'XMTc3MzU4NDM1Ng==',
            autoplay: false,
            show_related: false,
            events:{
            onPlayerReady: function(){ /*your code*/ },
            onPlayStart: function(){ /*your code*/ },
            onPlayEnd: function(){ /*your code*/ }
            }
            });
            function playVideo(){
            player.playVideo();
            }
            function pauseVideo(){
            player.pauseVideo();
            }
            function seekTo(s){
            player.seekTo(s);
            }
            function currentTime(){
            return player.currentTime();
            }
          </script>