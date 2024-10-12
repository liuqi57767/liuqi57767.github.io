![sunpanel##shadow##](https://blossom.57767.top:15678/pic/home/bl/img/U1/sunpanel-1.png)

#  一、**前言** 
&nbsp;&nbsp;&nbsp;&nbsp;作为一名折腾nas的小白，怎么能少得了个人导航页呢，毕竟nas上要跑很多服务，你不可能一一的都记住端口号。
#  二、**我的选择** 
&nbsp;&nbsp;&nbsp;&nbsp;NAS导航页有很多容器可以选择，我也折腾过很多，比如：Sun-Panel、Homarr、Heimdall、Flare、Homepage、Dashy、Homer；每个容器都有其特色，但就我个人而言，sun-panel最符合我的需求（可以切换内外网模式），而且颜值也在线，编辑也方便。项目地址：[sun-panel](https://github.com/hslr-s/sun-panel)。

&nbsp;&nbsp;&nbsp;&nbsp; [我的导航页](https://sun.57767.top:15678)  **欢迎围观，右上角可以切换内外网模式，加了一些背景和简单的特效。** 
#  三、**项目部署** 
&nbsp;&nbsp;&nbsp;&nbsp;Sun-panel 是我个人非常推荐的一个导航页，你可以将这个项目部署在任何支持docker的nas系统中，我是部署在ubuntu系统中的。

&nbsp;&nbsp;&nbsp;&nbsp;最大特色：1、支持一键切换内外网链接；2、支持自动抓取链接图标。

&nbsp;&nbsp;&nbsp;&nbsp;部署很简单，直接docker run就行了，如果部署遇到问题，可以留言交流。

&nbsp;&nbsp;&nbsp;&nbsp;我正在使用的版本是v1.5.0-beta24-05-11，截止2024年8月19日，项目最新版本应该是v1.5.2-beta24-08-10，在用的版本已经能满足我的需求，所以没有及时更新，如果你也想和我用一样的版本，那就按照下面的命令部署就行。
##  四、**参考部署命令** 
```bash
sudo docker run -d --restart=always \
-p 3002:3002 \  #左侧可以替换成你喜欢的端口号
-v /home/docker/sun-panel/conf:/app/conf \  #给页面加点特效的话就要编辑这个目录内相关文件，必须映射出来。
-v /var/run/docker.sock:/var/run/docker.sock \  #如果不需要sun-panel管理docker应用，则删除此行，我就没用
--name sun-panel \
hslr/sun-panel:v1.5.0-beta24-05-11 #你也可以直接使用latest标签
```
#  五、**后续** 
&nbsp;&nbsp;&nbsp;&nbsp;部署完毕后，就可以访问你的设备ip:3002进入主页，可视化编辑还是很好用的，在编辑导航页时你一定会用到相关的图标，这里给大家推荐几个图标网站，不用下载，直接去复制链接粘贴到sun-panel编辑页面相应位置就可以生效了。[阿里巴巴矢量图](https://www.iconfont.cn)、 [爱给图标](https://www.aigei.com/icon/class)、 [Iconify图标库](https://icon-sets.iconify.design/)
#  六、**友情提示** 
&nbsp;&nbsp;&nbsp;&nbsp;对于拉取不下来镜像的同学，可以使用如下地址加速：

&nbsp;&nbsp;&nbsp;&nbsp;**示例:docker.1panel.live/hslr/sun-panel:v1.5.0-beta24-05-11** 

&nbsp;&nbsp;&nbsp;&nbsp;`docker.m.daocloud.io`

&nbsp;&nbsp;&nbsp;&nbsp;`dockerhub.timeweb.cloud`

&nbsp;&nbsp;&nbsp;&nbsp;`docker.1panel.live`

&nbsp;&nbsp;&nbsp;&nbsp;`docker.nastool.de`

&nbsp;&nbsp;&nbsp;&nbsp;`docker.agsv.top`

&nbsp;&nbsp;&nbsp;&nbsp;`docker.agsvpt.work`

&nbsp;&nbsp;&nbsp;&nbsp;`docker.m.daocloud.io`

&nbsp;&nbsp;&nbsp;&nbsp;`dockerhub.anzu.vip`

&nbsp;&nbsp;&nbsp;&nbsp;`docker.chenby.cn`

&nbsp;&nbsp;&nbsp;&nbsp;`docker.jijiai.cn` 
##  七、**我的背景图** 
![buckgroud.png##shadow##](https://blossom.57767.top:15678/pic/home/bl/img/U1/sunpanel-2.png)


