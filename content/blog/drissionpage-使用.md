---
title: DrissionPage 使用
date: 2024-09-30T02:13:56.504Z
---





# 1. 根据标签获取

### 1.1 span text

ele("tag:span@text():Unlock")

### 1.2 input  class

tag:input@class=class-input-input

### 1.3  div text
tag:div@text():unlock

#### 1.4 打开 plugin
 self.driver.get("chrome-extension://mcohilncbfahbmgdjkbpemcciiolgcge/popup.html#/initialize")


### input 获取多输入框
 inpts=self.driver.eles("tag:input@class=words-inputs__container__input")
 for i in range(3):
            inpts[i].input(xxx[i])

### 1.6 根据 title 获取  插件
wall = page.get_tab(title='xxx Wallet')


