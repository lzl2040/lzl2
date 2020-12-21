---
layout: post
title:  java大作业--音乐播放器
date:   2020-12-21 11:12:23 +0530
categories: java GUI
---
最近在做java课程设计，其中也包含了很多问题，虽然很简单，但正是因为不熟悉，导致花费了很多时间，这篇就用来记录做课设的历程！！

## 按钮图片的切换
这是今天遇到的问题，音乐播放器按下播放键就会变为暂停键，这个切换花了我一个多小时时间，其实非常简单，我也是做的想吐了，再加上学校垃圾的校园网，让我心情烦躁，害。  
下面是具体方法：
```java
public JButton changeIconSize(JButton button,String url,int width,int height,String command){//这是设置按钮的方法，url为图片地址,command为添加的命令
		        ImageIcon buttonImg=new ImageIcon(url);
		        //改变图片的大小
		        buttonImg.setImage(buttonImg.getImage().getScaledInstance(width, height, Image.SCALE_DEFAULT));
		        button.setActionCommand(command);
		        button.setIcon(buttonImg);
				button.addActionListner(this);
		        return button;
		}
```
利用上述方法就可以让图片大小与按钮相适应，接下来是更换按钮图片
```java
public void actionPerformed(ActionEvent e){
				if(e.getSource()==playB)
				{
					if(e.getActionCommand().equals("播放"))
					{
						playB = changeIconSize(playB, "./res/pause.png", 30, 30, "暂停");
					}
				else if(e.getActionCommand().equals("暂停"))
					{
						playB = changeIconSize(playB, "./res/play.png", 30, 30, "播放");
					}
				}
}
```
接下来是构造方法:
```java
public music(){
			JFrame musicFrame = new JFrame("音乐播放器");
			Container con = musicFrame.getContentPane();
			con.setLayout(null);//设置为绝对布局
			JButton playB = new JButton();
			playB = changeIconSize(playB, "./res/play.png", 30, 30,"播放");
			musicFrame.add(playB);
}
```
-------------------------------12-21日--------------------------------------