#移动端布局常见问题
1.横竖屏限制问题


<meta name="x5-orientation" content="portrait | landscape"/>只支持x5内核
<meta name="screen-orientation" content="portrait">  只支持uc浏览器


2.全屏限制问题


<meta name="x5-fullscreen" content="true"/> 只支持x5内核
<meta name-"full-screen" content="yes">  只支持uc浏览器


3.禁止识别电话号码和邮箱


<meta name="format-detection" content="telephone=no,email=no"/>


3.禁止识别电话号码和邮箱


<meta name="format-detection" content="telephone=no,email=no"/>


*禁止识别后面页面中所有的邮箱和电话将不会识别，如果有特殊要求，要配合一下代码实现*


<a href="tel:110">请拨打110电话</a>
<a href="qq@.com">请发送邮件qq@.com</a>


4.消除链接\表单\按钮默认背景样式


-wekit-tap-highlight-color:rgba(0,0,0,0);


5.消除按钮圆角


-webkit-appearance:none;


6.移动字体
7.ios系统
    默认中文字体是Heiti SC
    默认英文字体是 Helvetica
    默认数字字体是HelveticaNeue
    无微软雅黑字体
8.android系统
    默认中文字体是Droidsansfallback
    默认英文和数字字体是Droid Sans
    无微软雅黑字体
9.winphone系统
    默认中文字体是Dengxian（方正等线字体）
    默认英文和数字字体是Segoe
    无微软雅黑字体
*结论*
* 各个手机系统有自己的默认字体，切都不支持微软雅黑
* 如无特殊要求，手机端无需定义中文字体，使用系统默认
*英文字体和数字字体可使用Helvetica，三种系统都支持


body{font-family:Helvetica;}


2.禁止用户设置字体大小


-wekit-user-select:none     //安卓不支持


3.font boosting *移动端设备为了是用户能看清楚大批量的字体，会自动对字体进行放大,但是只要是指定了容器的高度，就能解决*


p{max-height:9999999px}


4.固定定位问题


#移动端环境搭建
1.利用chrome浏览器deviceToolbar来调试移动端页面的尺寸
2.利用本地服务器创建端口，进行真机调试
3.利用hbuider等工具惊醒虚拟机调试           
