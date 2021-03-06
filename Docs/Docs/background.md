---
title: 系统部署背景
---

# 系统部署背景
系统部署阶段会显示你设置的一张图片作为背景，并且带有部署状态 Toast  
这样使部署过程中不会一片漆黑，看起来体验极差    
也可以用于电脑店宣传，或者社区第三方定制系统宣传等  

## 用法
将`OOBE_BG`字段中`OOBE_BG`值设置为1(启用)状态   
并且放置一张常规格式（jpg,png,bmp）（建议 jpg）的图片到 WTDR 主程序目录，并设置`OOBE_BG_Name`值为图片文件名

```ini
[OOBE_BG]
;系统部署背景
OOBE_BG=1
;背景图片名（请放置在WTDR根目录）
OOBE_BG_Name=name.jpg
```

## 分辨率适配
Win10 在系统部署中，会随着显卡驱动安装上而更改分辨率，更改分辨率后背景可能会变形，所以可以准备多张常用不同分辨率的背景，程序会根据当前分辨率而调用
```ini
[OOBE_BG]
OOBE_BG=1
;背景图片名（请放置在WTDR根目录）
OOBE_BG_Name=default.jpg
;1920*1080 分辨率下使用 1080.jpg 作为背景
1920_1080=1080.jpg
;1366*768 分辨率下使用 notebook.jpg 作为背景
1366_768=notebook.jpg
```