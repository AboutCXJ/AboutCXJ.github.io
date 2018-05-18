---
layout: post
title: '自学 Swift - 三十天三十个 Swift 小项目（更新中...）'
date: 2017-10-13
categories: Swift
tags: Swift
---



个人拖延症太严重，一直没好好学习Swift。受[@Allen_朝辉](http://www.jianshu.com/u/7211e265e765)启发，决定每天写个小项目来学习Swift。

项目代码同步更新到github：[项目地址](https://github.com/AboutCXJ/30DaysOfSwift)

## Project 01 - SimpleStopWatch

![SimpleStopWatch](https://github.com/AboutCXJ/30DaysOfSwift/blob/master/Project%2001%20-%20SimpleStopWatch/Project%2001%20-%20SimpleStopWatch.gif?raw=true)

* 1）简单的计时器
* 2）使用 Timer.scheduledTimer
* 3）开始，暂停，重置功能


## Project 02 - CustomFont
![CustomFont](https://github.com/AboutCXJ/30DaysOfSwift/blob/master/Project%2002%20-%20CustomFont/Project%2002%20-%20CustomFont.gif?raw=true)

* 1）自定义字体
* 2）项目中导入字体文件（注意：直接拖到项目中，Build Phases - Copy Bundle Resources 肯没有自动包含，需要手动添加）
* 3）在info.plist中添加Fonts provided by application属性，添加字体
![info.plist](/resources/2017-10-13-自学-Swift-三十天三十个-Swift-小项目/字体配置.png)
4）使用以下代码打印出字体名字

``` swift
for family in UIFont.familyNames {
print("font-family:",family)
for font in UIFont.fontNames(forFamilyName: family) {
print("font-name:",font)
}
}
```

## Project 03 - PlayLocalVideo
![PlayLocalVideo](https://github.com/AboutCXJ/30DaysOfSwift/blob/master/Project%2003%20-%20PlayLocalVideo/Project%2003%20-%20PlayLocalVideo.gif?raw=true)

* 1）播放本地视频
* 2）使用UITableView做个个视频列表
* 3）import AVKit 使用AVPlayerViewController播放视频


## Project 04 - SnapChatMenu

![SnapChatMenu](https://github.com/AboutCXJ/30DaysOfSwift/blob/master/Project%2004%20-%20SnapChatMenu/Project%2004%20-%20SnapChatMenu.gif?raw=true)

* 1）模仿SnapChat样式
* 2）左右两个视图是UIImageView
* 3）相机使用AVFoundation框架

## Project 05 - CarouselEffect
![CarouselEffect](https://github.com/AboutCXJ/30DaysOfSwift/blob/master/Project%2005%20-%20CarouselEffect/Project%2005%20-%20CarouselEffect.gif?raw=true)


* 1）UICollectionView实现的卡片选择
* 2）使用UIBlurEffect UIVisualEffectView 添加了模糊效果

## Project 06 - FindMyLocation
![FindMyLocation](https://github.com/AboutCXJ/30DaysOfSwift/blob/master/Project%2006%20-%20FindMyLocation/Project%2006%20-%20FindMyLocation.gif?raw=true)

* 1）定位
* 2）在info.plist中添加 NSLocationWhenInUseUsageDescription
* 3）使用CoreLocation框架获取当前位置


## Project 07 - PullToRefresh

![PullToRefresh](https://github.com/AboutCXJ/30DaysOfSwift/blob/master/Project%2007%20-%20PullToRefresh/Project%2007%20-%20PullToRefresh.gif?raw=true)

* 1）使用UIRefreshControl实现的下拉刷新

## Project 08 - RandomGradientColor


![RandomGradientColor](https://github.com/AboutCXJ/30DaysOfSwift/blob/master/Project%2008%20-%20RandomGradientColor/Project%2008%20-%20RandomGradientColor.gif?raw=true)

* 1）使用CAGradientLayer实现的随机渐变背景色

```markup
CAGradientLayer的坐标起点是左上角（0，0）终点是右下角（1，1）
CAGradientLayer属性:

colors
var colors: [AnyObject]?
一个包含CGColor的数组,规定所有的梯度所显示的颜色,默认为nil

locations
var locations: [NSNumber]?
一个内部是NSNumber的可选数组,规定所有的颜色梯度的区间范围,选值只能在0到1之间,并且数组的数据必须单增,默认值为nil


endPoint
var endPoint: CGPoint
终点坐标

startPoint
var startPoint: CGPoint
与endPoint相互对应,起点坐标

type
var type:String
绘制类型,默认值是axial,也就是线性绘制,各个颜色阶层直接的变化是线性的
```

## Project 09 -ImageScroller


![ImageScroller](https://github.com/AboutCXJ/30DaysOfSwift/blob/master/Project%2009%20-ImageScroller/Project%2009%20-ImageScroller.gif?raw=true)


* 1）使用UIScrollView实现的图片缩放功能


## Project 10 - VideoBackground

![VideoBackground](https://github.com/AboutCXJ/30DaysOfSwift/blob/master/Project%2010%20-%20VideoBackground/Project%2010%20-%20VideoBackground.gif?raw=true)

* 1）模仿spotyfi的登录背景视频播放
* 2）使用AVPlayer和AVPlayerLayer


## Project 11 - GradientTableView


![GradientTableView](https://github.com/AboutCXJ/30DaysOfSwift/blob/master/Project%2011%20-%20GradientTableView/Project%2011%20-%20GradientTableView.gif?raw=true)

* 1）渐变色TableView
* 2）根据行数计算颜色

``` Swift
let color = CGFloat(indexPath.row) / CGFloat(self.datas.count) * 0.8
cell.backgroundColor = UIColor.init(red: 0, green: color, blue: 1.0, alpha: 1.0)
```


## Project 12 - LoginAnimation


![LoginAnimation](https://github.com/AboutCXJ/30DaysOfSwift/blob/master/Project%2012%20-%20LoginAnimation/Project%2012%20-%20LoginAnimation.gif?raw=true)

* 1）登录界面的小动画
* 2）进入页面的动画使用UIView.animate
* 3）点击登录按钮使用的CAKeyframeAnimation

