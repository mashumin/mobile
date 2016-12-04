# 移动端视口（viewport)问题
*viewport就是设备的频幕上能用来显示我们的网页的那一块区域*
*移动设备上一般存在3种视口*
## layout viewport 默认的布局视口

`移动端设备的频幕不是很宽，但是又想完整的呈现各种页面（PC端的页面），所以移动端浏览器把视口默认的定义为一个较宽的值，一般为980px可以通过document.documentElement.clientWidth获取到`
*但是一般布局视口都会比我们的屏幕大，所以会出现滚动条，用户体验很不好，于是出现了visual viewport*
## visual viewport视觉视口
一般来说视觉视口，就是我们移动设备屏幕的大小 window.innerWidth,我们都知道移动设备的屏幕尺寸小于桌面端的屏幕尺寸，那么要想在有限的窗口内表达更多的像素
那么移动端的设备就必须要通过物理手段来解决，在有限的屏幕内显示更多的像素点，于是就有了各种高清屏，比方说2k\4k\视网膜屏等，这些设备的dpi很高
dpi指的就是屏幕像素密度，我们也叫做物理像素，比方说：安卓分为ldpi、mdpi、hdpi、xhdpi等不同的等级
而css所指的一个像素我们叫做独立像素，像素比：devicePixelRatio=物理像素/独立像素可以通过 window.devicePixelRatio 获取，不过有些浏览器不支持
在有的浏览器里面会用物理像素表示独立像素，有的浏览器里面会用独立像素单独表示，就会出现要不然很小，要不然很大的情况
如何解决这个问题，浏览器帮我们创建了一个理想的视觉窗口，让我们可以自己定义该视口有多大，并且强制用独立像素来表达
## ideal viewport 理想视口
理想视口并没有一个固定的尺寸，那么我们就能将浏览器的视口，设置我们任意想要的大小，并且强制用独立像素来表达诉求，其实就是用将布使用局视口设置为理想视口
一般来说我们会将理想窗口，设置为我们屏幕的大小，这样更符合用户的使用习惯和视觉习惯
但是移动设备的屏幕千差万别，我们会通过html5给我们提供的meta标签来进行设置



<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0">


1.width=|device-width设置布局视口的宽度
2.initial-scale=页面的厨师缩放值
3.minimum-scale=允许用户的最小缩放值
4.maximum-scale=允许客户的最大缩放值
5.height= 这个属性对我们并不重要，很少使用
6.user-scalable=no | yes 是否允许用户缩放 (iOS10不支持)