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


### 1.7 模糊查询 类

tag:input[class*=password]：
这个选择器匹配所有类型为 input 的元素，其 class 属性中包含字符串 "password" 的元素。
例如，class="input-input password" 或 class="input password-field" 都会被匹配。
tag:input@class=password：
这个选择器匹配所有类型为 input 的元素，其 class 属性完全等于 "password" 的元素。
只有当 class 属性的值完全是 "password" 时，才会被匹配，例如 class="password"



### 1.8 多个 class 组合
#### 1.8.1 组合 type = pass and value
password_input = wall.ele('x://input[@type="password"][@value=""]')
            if password_input:
                password_input.input(PASSWORD)
                page.wait(1)



### 1.9 shdow 获取
#### 1.9.1 进入元素shadow dom内再定位okx
 shadow = swap_page.ele("tag:div@data-testid=dynamic-modal-shadow").shadow_root

#### 1.9.2 点击shdow 元素
shadow.ele("tag:button@data-testid=SelectNetworkButton").click()




