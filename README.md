## Introduction

- 你是否有这样的烦恼？在国科大的课程网站正在刷网课看视频，突然提示会话过期，影响上课体验
- 你是否有这样的烦恼？登录到国科大的课程网站后突然有其他的事，等回过头想继续操作一波的时候发现会话已经过期，需要重新登录，还有那烦人的验证码

现在，这些问题通通可以通过**UCAS-SessionTimeoutHelper**来解决了，它的作用就是：自动点击[国科大教务处课程网站]( https://course.ucas.ac.cn/ )会话过期的提示框。

`UCAS-SessionTimeoutHelper`是一个安装在浏览器中的脚本，只针对国科大课程网站起作用。每隔一段时间检查是否有会话即将过期的弹出框，如果有，则模拟用户点击。

## Features

1. 设定检测弹出框的时间间隔，自行修改代码中的参数：

    ```javascript
    window.setInterval(function(){
    	checkSessionTimeoout();
    }, 60000);
    ```

    根据测试，课程网站**每21分钟**弹出一次会话过期提示框。

2. 自动点击弹出框的按钮，保持在线状态

## Installation

1. 安装脚本管理软件

    打开 [Tampermonkey.net](https://link.zhihu.com/?target=http%3A//tampermonkey.net/) 官网，安装对应版本的插件。

    **注**：chrome 可以通过网站 [crx4chrome](https://link.zhihu.com/?target=https%3A//www.crx4chrome.com/) 来下载扩展程序 crx 文件，手动将 crx 文件拖动至扩展页面安装即可。

2. 安装**UCAS-SessionTimeoutHelper**

    - 方法一：打开[UCAS-SessionTimeoutHelper脚本安装网页]( https://greasyfork.org/zh-CN/scripts/397403-ucas-sessiontimeouthelper )进行安装
    - 方法二：点击浏览器扩展栏中油猴脚本的图标（一个黑乎乎的正方形，里面有两个小圆形）→ 点击加号，创建用户自定义的脚本 → 从项目的**UCAS-SessionTimeoutHelper.js**中复制代码到网页的代码编辑器中 → ctrl+s保存即可

    

