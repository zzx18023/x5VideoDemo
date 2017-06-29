# 移动端video标签的一些特殊性以及x5内核下如何使用同城播放器。
***
>在移动端video标签的表现和PC端不大一样，相信开发者们基本都有接触过。
>大部分浏览器都会对video标签进行接管，使用自己的播放器进行视频播放。
>普遍表现为悬浮于网页内对应video标签位置，造成的影响便是置顶播放。
>也有的手机上表现为全屏播放！
>从而造成了很多问题，比如因为video置顶显示，导致自制播放器UI被遮挡，字幕、弹幕被遮挡，甚至播放器内会出现广告。
***
>###在x5内核下使用同层播放器
>>不过x5内核给开发者提供了一种同层播放模式，[H5同层播放器接入规范](https://x5.tencent.com/tbs/guide/video.html)
>>使用该模式可以实现video在页内正常渲染。
>>先看看其表现如何(主要做微信内):
>>**测试环境：**
>>>机型：小米MIX
>>>Android版本：7.0
>>>微信版本：6.5.8
>>>TBS内核版本：043307 (大于036849表示支持同层播放器)

>在video标签上添加属性x5-video-player-type="h5"启用Ｈ5同层播放器
>```
<style type="text/css">
	video {
		width: 100%;
	}
</style>
<video controls="controls" src="video/advideo.mp4" x5-video-player-type="h5" ></video>
```
><img src="http://zzx18023.oschina.io/x5-video/img/Screenshot/001.jpg" width="300px"/>






























