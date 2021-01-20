# web
web前端大作业（苹果网站网页设计模拟）

目录

一、 程序设计思路

二、 设计题目	

三、 编程环境和工具

四、 功能实现

五、 结构设计

六、 代码调试	

七、 运行效果

八、 存在问题

九、 实验总结

一、程序设计思路

在网络飞速发展的今天，互联网成为人们快速获取、发布和传递信息的重要渠道，它在人们政治、经济、生活等各个方面发挥着重要的作用。因此网站建设在网络应用上的地位显而易见，它已成为政府、企事业单位信息化建设中的重要组成部分，从而倍受人们的重视。我们当代大学生更是离不开网络给我们带来的好处与便利，本课程的设计目的是通过实践使同学们经历网页制作的全过程。通过设计达到掌握网页设计、制作的技巧。

为了熟练掌握WebStorm 软件的的操作和应用，了解和熟悉网页设计的基础知识和实现技巧。根据老师的要求，给出网页设计方案，利用合适图文素材设计制作符合要求的网页设计作品。

二、设计题目

苹果网站网页设计

三、编程环境和工具

JetBrains WebStorm 软件 以及QQ浏览器

四、功能实现

1、页面布局

2、显示广告轮播

3、搜索框

4、侧边栏跳转

5、链接跳转

五、结构设计

https://github.com/duchangchang/web/blob/main/1.png

六、代码调试

首页代码：
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <style>
        #sy{
            width: 1400px;
            height: 1200px;
        }
        .top1{
            width: 1398px;
            height: 150px;
            background: url("../photo/p1.jpg");
        }
        .top2{
            width: 1398px;
            height: 50px;
            background-color: darkgrey;
        }
        .left{
            width: 200px;
            height: 500px;
            background-color:lightslategrey;
            display: inline-block;
            margin-top: 20px;
        }

        .right{
            width: 1090px;
            height: 490px;
            display: inline-block;
            margin-left: 10px;

        }
        img{
            width: 1000px;
            height: 470px;
            margin-right: 0px;
        }
       .list{
            list-style: none;
            position: relative;
        }
        .item{
            position: absolute;
        }
        .item.active{
            z-index: 10;
        }
         .shu{
            list-style: none;
            position: relative;
            left: 450px;
            top: 400px;
            z-index: 1000;
        }
       .point{
            width: 15px;
            height: 15px;
            background-color:gainsboro;
            border-radius: 100%;
            float: left;
            margin-right: 50px;
            border-style: solid;
            border-width: 1px;
            border-color: black;
            cursor: pointer; /*把鼠标变成小手*/
        }
        .point.active {
            background-color: rgba(255, 255, 255, 0.2);
            z-index: 100;
        }

        .bottom1{
            width: 1400px;
            height: 800px;
            margin-top: 20px;
            background-color: gainsboro;
        }
        .ph1,.ph2,.ph3,.ph4,.ph5,.ph6,.w1,.w2,.w3,.w4,.w5,.w6{
            width: 350px;
            height: 250px;
            margin: 0px 20px 0px 50px;
        }
        .b1,.b2,.b3,.b4,.b5,.b6{
            width: 400px;
            height: 400px;
            float: left;
        }

        .bottom2{
            width: 1400px;
            height: 300px;
            background-color: gainsboro;
            font-size: 20px;
            font-style: inherit;
        }
        .kj1{
            width: 290px;
            height: 300px;
            margin-left: 200px;
            background-color: darkgray;
            float: left;
        }
        .kj2,.kj3,.kj4{
            width: 240px;
            height: 300px;
            background-color: darkgray;
            float: left;
        }
        .kj11{
            margin-left: 40px;
            float: left;
        }

        .bottom3{
            width: 1400px;
            height: 100px;
            background-color: lightgray;
        }
        .bt{
            padding-top: 10px;
           margin-left: 10px;
        }

        .wz1{
            width: 200px;
            height: 30px;
            padding-top: 10px;
            margin-left: 1100px;
            float: right;
        }
        .dhl{
            height: 40px;
            padding-top: 5px;
            margin-left: 450px;
        }
        .dhl1{
            width: 400px;
            height: 30px;
        }
        .dhl2{
            width: 50px;
            height: 30px;
        }
        .fll{
            width: 200px;
            height: 490px;
            background-color:lightslategrey;
            margin-top: 10px;
        }
        #fz1,#fz2,#fz3,#fz4,#fz5{
            width: 200px;
            height: 50px;
            float: left;
            background-color: lightslategrey;
        }
        #fz1:hover{  background-color: dimgray;  }
        #fz2:hover{  background-color: dimgray;  }
        #fz3:hover{  background-color: dimgray;  }
        #fz4:hover{ background-color: dimgray;  }
        #fz5:hover{background-color: dimgray;  }
        .fl{
            margin-left: 10px;
            font-size: 30px;
            font-weight: 600;
            color: midnightblue;
            float: left;
        }
        .fl1,.fl2,.fl3,.fl4,.fl5{
            margin-left: 25px;
            font-size: 20px;
            font-weight: 600;
            color: black;
        }
    </style>   
    </head>
    <body>
    <div id="sy">
    <div class="top1">
    <div class="wz1">
    <a href="../跳转页面/登录.html" >登录 </a> &nbsp;&nbsp;|
    <a href="../跳转页面/注册.html">注册 </a> &nbsp;&nbsp;|
    <a href="kf">客服 </a> &nbsp;&nbsp;|
    <a href="gd">更多</a> &nbsp;&nbsp;
    </div>
    </div>
    <div class="top2">
    <div class="dhl">
    <input class="dhl1" type="text" placeholder="请输入">
    <input class="dhl2" type="submit" value="搜索">
    </div>
    </div>

    <div class="left">
    <div class="fll">
        <div id="fz"><P class="fl">全部商品分类</P></div>
        <div id="fz1"><P class="fl1">Mac &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;></P></div>
        <div id="fz2"><P class="fl2">iPad &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;></P></div>
        <div id="fz3"><P class="fl3">Watch&nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;></P></div>
        <div id="fz4"><P class="fl4">iphone  &nbsp; &nbsp; &nbsp;&nbsp; &nbsp;></P></div>
        <div id="fz5"><P class="fl5">配件 &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;></P></div>
     </div>
    </div>

    <div class="right">
    <ul class="shu">
        <li class="point active" data-index= '0'></li>
        <li class="point" data-index= '1'></li>
        <li class="point" data-index= '2'></li>
        <li class="point" data-index= '3'></li>
    </ul>
    <ul class="list">
        <li class="item active"><img src="../photo/p2.jpg"></li>
        <li class="item"><img src="../photo/p3.jpg"></li>
        <li class="item"><img src="../photo/p5.jpg"></li>
        <li class="item"><img src="../photo/p6.jpg"></li>
    </ul>
    </div>

    <div class="bottom1">
    <div class="b1">
        <img class="ph1" src="../photo/p4.jpg">
        <div class="w1">
           <h2>iPad Pro</h2>
           <h4>你的下一台电脑，何必是电脑</h4>
           <a href="../跳转页面/Mac.html">进一步了解</a> &nbsp;&nbsp;<a href="iPad.html">购买</a>
        </div>
    </div>
    <div class="b2">
        <img class="ph2" src="../photo/p7.jpg">
        <div class="w2">
            <h2>iPad Pro</h2>
            <h4>你的下一台电脑，何必是电脑</h4>
            <a href="../跳转页面/iPad.html">进一步了解</a> &nbsp;&nbsp;<a href="iPad.html">购买</a>
        </div>
    </div>
    <div class="b3">
        <img class="ph3" src="../photo/p8.jpg">
        <div class="w3">
            <h2>iPad Pro</h2>
            <h4>你的下一台电脑，何必是电脑</h4>
            <a href="../跳转页面/iphone.html">进一步了解</a> &nbsp;&nbsp;<a href="iPad.html">购买</a>
        </div>
    </div>
    <div class="b4">
        <img class="ph4" src="../photo/p9.jpg">
        <div class="w4">
            <h2>iPad Pro</h2>
            <h4>你的下一台电脑，何必是电脑</h4>
            <a href="../跳转页面/Watch.html">进一步了解</a> &nbsp;&nbsp;<a href="iPad.html">购买</a>
        </div>
    </div>
    <div class="b5">
        <img class="ph5" src="../photo/p10.jpg">
        <div class="w5">
            <h2>iPad Pro</h2>
            <h4>你的下一台电脑，何必是电脑</h4>
            <a href="../跳转页面/配件.html">进一步了解</a> &nbsp;&nbsp;<a href="iPad.html">购买</a>
        </div>
    </div>
    <div class="b6">
        <img class="ph6" src="../photo/p11.jpg">
        <div class="w6">
            <h2>iPad Pro</h2>
            <h4>你的下一台电脑，何必是电脑</h4>
            <a href="../跳转页面/Mac.html">进一步了解</a> &nbsp;&nbsp;<a href="iPad.html">购买</a>
        </div>
    </div>
    </div>

    <div class="bottom2">
    <div class="kj1">
        <div class="kj11">
        选购及了解<br>
        翻新和优惠<br>
        分期付款<br>
        Apple Trade In 换购计划<br>
        订单状态<br>
        </div>
     </div>
    <div class="kj2">
        服务<br>
        Apple Music<br>
        iCloud<br>
        账户<br>
        管理你的 Apple ID<br>
        </div>
    <div class="kj3">
        Apple Store 商店<br>
        查找零售店<br>
        Genius Bar 天才吧<br>
        Today at Apple<br>
        Apple 夏令营<br>
    </div>
    <div class="kj4">
        商务应用<br>
        Apple 与商务<br>
        商务选购<br>
        教育应用<br>
        Apple 与教育<br>
        高校师生选购<br>

    </div>
    </div>

    <div class="bottom3">
    <div class="bt">更多选购方式：查找你<a href="bth">附近的 Apple Store 零售店</a> 及更多门店，或者致电 400-666-8800。 </div>
    </div>
    </div>
    </body>
    <script type="text/javascript">//跳转页面
    document.getElementById("fz1").onclick=function(){
        window.location ="../跳转页面/Mac.html";
    }
    document.getElementById("fz2").onclick=function(){
        window.location ="../跳转页面/iPad.html";
    }
    document.getElementById("fz3").onclick=function(){
        window.location ="../跳转页面/Watch.html";
    }
    document.getElementById("fz4").onclick=function(){
        window.location ="../跳转页面/iphone.html";
    }
    document.getElementById("fz5").onclick=function(){
        window.location ="../跳转页面/配件.html";
    }
    //轮播
    var items = document.getElementsByClassName('item')
    var points = document.getElementsByClassName('point');
    var index = 0;
    var clearActive = function () {
    for (var i = 0; i < items.length; i++) {
        items[i].className = 'item';
    }
    for(var i = 0; i < points.length; i++){
        points[i].className = 'point'
    }
    }
    var goIndex = function () {
    clearActive();
    items[index].className = 'item active'
    points[index].className = 'point active'
    }
    for (var i = 0; i < points.length; i++) {
    points[i].addEventListener('click',function () {
        var pointIndex = this.getAttribute('data-index');
        index = pointIndex;
        goIndex();
    })
    }
    </script>
    </html>

    登录代码：
    <!DOCTYPE html>
    <html>
    <head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <style>
        #sy{
            width: 1300px;
            height: 1200px;
            background-color: lightcyan;
        }
        .top1{
            width: 1300px;
            height: 150px;
            background: url("../photo/p1.jpg");
        }
        .top2 {
            width: 1300px;
            height: 50px;
            background-color: darkgrey;
        }
        .body{
            width: 300px;
            height: 400px;
            margin-left: 500px;
            margin-top: 20px;
            background-color: mediumspringgreen;
        }
        .body1{
            font-size: 20px;
            font-weight: 600;
            margin-left: 30px;
            padding-top: 20px;
        }
        .hym,.mm1,.mm2,.dz{
            width: 200px;
            height: 30px;
        }
    </style>
    </head>
    <body>
    <div id="sy">
    <div class="top1"></div>
    <div class="top2"></div>
    <div class="body">
        <form class="body1" onsubmit="fun()">
            用 户 名<br><input class="hym" type="text" placeholder="请输入"><br>
            密 码<br><input class="mm1" type="password" placeholder="8-12位字符即可"><br>
            确认密码 <br><input class="mm2" type="pass" placeholder="与上方密码一致"><br>
            收货地址<br><input class="dz" type="add" placeholder="可多次进行更改"><br>
            <div><input type="submit" value="立即注册"></div>
        </form>
        <script>
            function fun(){
                alert("注册成功")
            }
        </script>
    </div>
    </div>
    </body>
    </html>

    iPad代码：
    <!DOCTYPE html>
    <html>
    <head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <style>
        .iPad{
            width: 1300px;
            height: 1200px;
            background-color: mediumspringgreen;
            position: absolute;
        }
        .iPad11,.iPad12{
            width: 300px;
            height: 400px;
            margin-top: 10px;
            margin-left: 10px;
            position: relative;
            float: left;
        }
        .iPad112,.iPad122{
            padding-left: 50px;
        }
    </style>
    </head>
    <body>
    <div class="iPad">
    <div class="iPad11">
        <img class="iPad111" src="../photo/p7.jpg">
        <div class="iPad112">
            <h2>选购及了解</h2>
            <h3>选购及了解</h3>
            <h3>选购及了解</h3>
        </div>
    </div>
    <div class="iPad12">
        <img class="iPad121" src="../photo/p7.jpg">
        <div class="iPad122">
            <h2>选购及了解</h2>
            <h3>选购及了解</h3>
            <h3>选购及了解</h3>
        </div>
    </div>
    </div>
    </body>
    </html>

七、运行效果

首页

https://github.com/duchangchang/web/blob/main/2.png
https://github.com/duchangchang/web/blob/main/3.png
https://github.com/duchangchang/web/blob/main/4.png

登录及注册

https://github.com/duchangchang/web/blob/main/5.png
https://github.com/duchangchang/web/blob/main/6.png

跳转

https://github.com/duchangchang/web/blob/main/7.png
https://github.com/duchangchang/web/blob/main/8.png
https://github.com/duchangchang/web/blob/main/9.png
https://github.com/duchangchang/web/blob/main/10.png
https://github.com/duchangchang/web/blob/main/11.png

八、存在问题

在广告轮播图的设置上，未设置为动态轮播，而是点击轮播，改为动态的轮播效果会给人一种更加高级的感觉。

九、实验总结

通过这次实验，在制作时总遇到这样那样的问题，为了使自己的网页更加丰富多彩，在网页中插入图象，运用轮播图，设置跳转页面。经过不断地修改，最后在自己摸索的情况下完成了这个实验的成果。但是在实验当中也遇到了很多的困难，这也反映出学习的还不够，需要更加刻苦钻研及学习，不断开拓视野，增强自己的实践操作技能，为以后能做出出色的网页而努力。

近一个星期的实验操作，在制作网页过程中，我学到了美化网页的方法，运用了更多的技巧。这使我学到了更多的知识，并且为我自己在制作网页这方面积累了一些经验。这些将是我人生中的一次重要的经历，将是我今后走上社会后的一笔巨大的财富。总体来说这次是对我的综合素质的培养，锻炼和提高。 
