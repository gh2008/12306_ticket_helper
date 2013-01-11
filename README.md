﻿12306.CN 订票助手
===================

这是一个用于辅助在[12306.CN]上订票的Chrome&amp;Firefox脚本。



功能
---------------------

这是一个可以运行在**[遨游3]**、**[Chrome]**、**[猎豹]**或**[Firefox]**浏览器上的脚本扩展，可以帮助您在 [12306.CN](https://dynamic.12306.cn/otsweb/) 购买火车票（或抢火车票？），反正就是偷懒呗。
    

**目前已经实现的功能包括**：

*	记录登录的用户名和密码，在打开登录页面后自动填写；
*	自动登录，遇到人过多或繁忙的时候自动重试，直到登录成功（有点儿抢线的味道）；
*	自动记录查询信息，一次查询线路后下次再查询自动填入；
*	自动刷新查询，当没有需要的车次时，自动重新刷新；
*	在[Chrome]/[遨游3]/[猎豹]下，查票和登录有右下角提示和声音提示；[Firefox]下暂不支持声音提示，但有桌面弹窗提示。
*	自动提交订单，直到订单成功
*	查询失败时自动刷新
*	预定失败时自动重新预定
*	禁用查询缓存
*	查询界面参数和设置自动保存
*	支持过滤无法预定车次
*	支持过滤无需要席别车次
*	现在系统已禁止验证码自动跳过，所以当出现验证码错误时，系统将会自动刷新验证码并自动定位到验证码输入框中并请求输入验证码，输入满四位的时候系统将会自动重新提交。


安装需求
---------------------

目前支持**[Chrome]**（含RC、Beta以及每夜版），**[Firefox]**（需要Scriptish扩展支持，使用了新的API所以GreaseMonkey不支持），**[遨游3]**（**需要使用高速模式，不过没用的话也没关系，脚本会提示你用高速模式的**），**[猎豹]浏览器**。

**提示**：如果您不是很熟**[Firefox]**或**[Chrome]**浏览器，那么您在付款时可能会遇到问题。**此时强烈建议您使用[遨游3]**！

####[遨游3]下安装

[遨游3] 请至官方的扩展库中安装，请 **[点击这里转到扩展页面](http://extension.maxthon.cn/detail/index.php?view_id=1339)**。

####在Chrome/[猎豹]上安装
[Chrome]下可以直接安装。直接打开 [助手主页](http://www.fishlee.net/soft/44/)，在**下载**一节中点击**通用版本**后（如果您实在木有找到，也可以直接[点击这里安装](http://www.fishlee.net/Service/Download.ashx/44/47/12306_ticket_helper.user.js)），Chrome将会在浏览器下方的下载区域通知进行安装：

![Chrome安装提示1](https://github.com/iccfish/12306_ticket_helper/raw/master/images/installation/chrome_1.png)

点击『继续』后，在弹出的对话框中继续点击『安装』。安装完成后即可。

![Chrome安装提示2](https://github.com/iccfish/12306_ticket_helper/raw/master/images/installation/chrome_2.png)


如果您未能看到安装提示，而是提示了下载或其它内容，请确认您的浏览器版本较新。

####在Firefox上安装
在[Firefox]上运行需要**Scriptish**扩展提供支持。**请注意，由于使用了Scriptish提供的新语法，因此_GreaseMonkey_扩展是不支持的**。

* 如果您尚未给[Firefox]安装Scriptish扩展，请[在此安装](https://addons.mozilla.org/zh-CN/firefox/addon/scriptish/)；
* 打开 [助手主页](http://www.fishlee.net/soft/44/)，在**下载**一节中点击**通用版本**后（如果您实在木有找到，也可以直接[点击这里安装](http://www.fishlee.net/Service/Download.ashx/44/47/12306_ticket_helper.user.js)）
* 正常情况下，Scriptish会弹出下列的安装提示，请点击『安装』继续；如果没有这样的提示框而是看到了下载或一堆『乱码』，那么请检查是否成功安装了Scriptish扩展。


提醒
---------------------

由于各大网银都不支持Firefox/Chrome支付，因此请务必在订票前做好支付的准备措施。
这里推荐使用银联在线支付，请开通银联后绑定快捷支付，这样在Firefox和Chrome下都可以顺利付款。
也可以使用招行的手机银行进行支付。


更新历史
----------------------
**版本: 1.0，更新时间： 2012-1-9**

**版本: 1.1，更新时间： 2012-1-9**

* 增加订单自动提交功能

**版本: 1.1.1，更新时间： 2012-1-9**

* 增加取消自动提交订单的功能

**版本: 1.1.2.1，更新时间： 2012-1-9**

* 更改登录判断逻辑，避免提示登录成功却又跳回登录页面的问题； 
* 其它细微更改

**版本: 1.1.3，更新时间： 2012-1-10**

* 增加改签页面的自动刷新支持

**版本: 1.3，更新时间： 2012-1-10**

* 新增查询失败时自动刷新的功能 
* 新增预定失败时自动重新预定的功能 
* 新增禁用查询缓存的功能 
* 其它细节更改

**版本: 1.3.2，更新时间： 2012-1-11**

* 修复了一些BUG 
* 增加了自动提交订单时的休息时间的设置

**版本: 1.4，更新时间： 2012-1-16**

* 将Chrome和Firefox两个版本分支完全合并，兼容处理 
* Firefox下支持声音提示 
* 修改了提示声音 
* 提示窗口均设置默认值自动关闭 
* 修正点击查询后参数保存的问题 
* 修改了参数保存位置，不再保存在Cookies中 
* 加入改签页面的自动提交 
* 增加脚本更新提示功能

**版本: 2.0.0.0，更新时间： 2012-1-19**

* 登录界面重新调整 
* 增加查询界面参数和设置保存功能 
* 增加过滤无法预定车次功能 
* 增加过滤无需要席别车次功能 
* 修复数个BUG 
* 现在系统已禁止验证码自动跳过，所以当出现验证码错误时，系统将会自动刷新验证码并自动定位到验证码输入框中并请求输入验证码，输入满四位的时候系统将会自动重新提交。 

**版本: 2.2.0，更新时间：2012.05.30**

* 根据最新版12306网站修正登录脚本
* 其它细节更新

**版本3.0.0，更新日期：2012.08.20**

* 增加新开专门订票网页窗口的提示；
* 席别过滤的勾选可以记录到设置中；
* 修改列表标题文字，避免换行；
* 增加过滤车次功能；
* 增加出现指定车次时，自动进入预定的功能；
* 增加自定义提示音乐地址功能；
* 增加进入预定页面后，自动播放提示音乐功能（针对自动预定）
* 增加自定义提示音乐地址功能
* 修复进入订票页面时，没有点击自动提交时输入验证码也会提交的BUG

**版本3.0.1，更新日期：2012.08.21**

* 修复勾选“仅座票”、“仅卧铺”过滤无效的BUG

**版本3.0.2，更新日期：2012.08.22**

* 修正在Firefox下查询有票时桌面提示不出现的错误

**版本3.0.4，更新日期：2012.08.23**

* 增加遨游3的扩展格式支持； 
* 修改提示打开全屏订票的弹框为链接，避免频繁提示造成困扰

**版本3.0.5 ，更新日期：2012.08.23**

* 修改登录成功提示，变成右下角弹窗提示
* [遨游3] 扩展兼容性改进，允许直接访问 www.12306.cn 时的运行
* 修正自定义时间里，24不被认为是正确时间的错误

**版本3.0.6，更新日期：2012.08.23**

* 添加输入验证码后自动开始提交的选项
* 修正遨游3更新链接提示的地址
* 修改检查更新所使用的地址，避免出现不安全脚本不让更新的问题

**版本3.2.0，更新日期：2012.09.10**

* 添加日期快捷操作
* 添加无票时在指定日期范围内循环查询的功能
* 重写自动提交订单逻辑到最新版
* 移除登录界面上无关紧要的弹窗提示
* 修正登录界面成功的提示不会消失的问题
* 修正登录脚本的兼容性
* 去除CSCript兼容检测代码，因为发现检测还是会出编译错误，没用 o(︶︿︶)o
* 修改刷新查询出错逻辑，改为延迟查询而不是立刻刷新（与自动刷新使用同样时间间隔）
* 修正当查询出错时以高频率刷新的问题;
* 其它细节更新

**版本3.2.1版本: 3.2.1，更新时间： 2012-9-10**

* 修正提交订单时的逻辑

**版本: 3.2.3，更新时间： 2012-9-10**

* 修改自动订票逻辑, 实际优先订票车次以加入列表的顺序而定 
* 修复 Chrome 下订票提示在启用自动订票时不消失的问题

**版本: 3.2.4，更新时间： 2012-9-11**

* 修改自动提交逻辑，未知状态代码时自动跳转到未支付订单页面 
* 修改自动预定逻辑，在进入订票页面提示系统忙时将可以自动重新提交
* 修改自动刷新逻辑

**版本：3.2.6，更新时间：2012.09.12**

* 修正服务器出错时以高速进行重试的BUG
* 修正当获得登录随机码失败时，以高速重复获得随机码的BUG
* 添加默认禁止查询缓存的功能
* 修正当自动轮查的日期中第一个日期选择时，无法自动切换的BUG
* 添加隐藏当查询失败时系统弹出来的提示失败对话框

**版本：3.2.7，更新时间：2012.09.13**

* 修正改签页面中验证码被帮助隐藏功能隐藏的BUG
* 出现重复提交错误时，自动刷新页面验证TOKEN并重新提交
* 修改对-4状态码的处理动作

**版本：3.2.8，更新时间：2012.09.13**

* 修改登录页面重试时间为2秒以免速度过快被封
* 添加403错误页自动重试顺便卖卖萌 o(︶︿︶)o， 买不着票只能自娱自乐了

**版本：3.2.9，更新时间：2012.09.13**

* 彻底修正登录人多时自动重试过快的问题
* 修改默认音乐地址，避免浏览器安全设置导致没有音乐;

**版本：3.3.0，更新时间：2012.09.16**

* 增加Firefox中的Storage设置检测 
* 增加基础设置对话框，允许设置登录重试时间间隔 
* 为防未经作者授权的出售, 加入注册系统 

**版本：3.3.1，更新时间：2012.09.17**

* 修正点击我的12306却跳转到查询的BUG 
* 注册系统升级，新的序列号注册更简单，新增绑定12306帐户而没有注册时间限制的序列号 

**版本：3.3.2，更新时间：2012.09.17**

* 移除自动提交排队时右下角的提示，因为排队太蛋疼，所以看得很多人也比较蛋疼 ╮(╯▽╰)╭
* 添加提交预定、未完成订单页面的出错自动重载功能
* 添加排队订票成功后，转到支付页时音乐提醒的功能
* 修正访问人数过多时，自动重新提交表单没有时间间隔的BUG

**版本：3.3.5,3.3.6，更新时间：2012.09.18**

* 允许禁用自动登录改用手动登录 
* 增加对 https://www.12306.cn/otsweb/ 网址的支持 
* 修改自动更新逻辑，允许在更新前查看更新内容以决定是否更新，并允许屏蔽指定版本的更新推送 
* 修正预定操作提示系统忙时无法自动重试的BUG
* 登录页添加快速链接区， 并添加重新注册快速链接 
* 其它细节修改

**版本：3.4.0，更新时间：2012.09.19**

* 订票提交页面添加实时队列数显示！
* 修正对 https://www.12306.cn/otsweb/ 的支持 【感谢（K.T.S）的提交！】
* 修正对【改签】页面自动刷新的支持
* 修正在提交订单页面出现错误后，重试之间没有时间间隔的BUG
* 恢复老版本的音乐地址，因为新版本的音乐地址经常有人放不出来(仅WEBKIT内核，Firefox对HTTP地址拒绝播放)
* 增加排队时间过久的警告

**版本：3.4.3，更新时间：2012.09.21**

* 增加谷歌的扩展包CRX类型的助手！（如果安装此类型，切记卸载脚本版的助手！）
* 修正订单提交排队逻辑，解决当被强行退出登录时出现的错误并反复重新请求
* 排队提示中增加当前排队人数，并将显示逻辑同步到铁道部最新更改
* 增加对未完成订单页面支持，显示时间和排队更及时完整，订单成功失败均有声音提示
* 增加两首用于提示的音乐（蓝精灵、超级玛丽），添加订票失败的悲歌（忽然之间 by 莫文蔚）……
* 修改选项对话框显示位置，防止显示在可视区域之外
* 修改登录逻辑，防止多次重试
* 修复各查询页面提示刷新却失效的问题

**版本：3.5.0，更新时间：2012.09.24**

* 在预定页面即可选择要自动填入订单的联系人，并自动定位到验证码框中
* 自动预定和黑名单添加开关，可自定义是否启用
* 黑名单和自动预定允许手动添加
* 黑名单和自动预定允许使用正则表达式进行匹配(正则表达式哦亲！)
* 登录界面，取消勾选保存密码时，自动清空已保存的密码
* 添加手动修改订单日期的高级功能（谨慎使用！）
* 警告！谷歌商店中由 www.6pmhaitao.com 发布的订票助手扩展为盗用本助手并加入恶意脚本后打包的，请大家不要安装！

**版本：3.5.5/6，更新时间：2012.12.04**

* 修复自动预定中不能使用正则表达式的BUG
*- 取消订票时间手动修改功能(喔……被铁道部枪毙了 ╮(╯▽╰)╭)
* 增加订票最小张数限制
* 修改刷新余票为即时刷新 (感谢 cutefelix 的提交)
* 自动选择人员增加对护照等其它类型证件的支持
* 增加请求日志功能（左上角显示日志按钮，出现异常的操作时请点击此按钮并复制日志）
* (其它细节更改)

**版本：3.5.7，更新时间：2012.12.11**
* 修正登录成功但没有能判断出的错误(2012.12.11铁道部最新修改)

**版本：3.6.0，更新时间：2012.12.11**
* 修正登录成功但没有能判断出的错误(2012.12.11铁道部最新修改)
* 修正自动预定功能失效的问题(2012.12.11铁道部最新修改)
* 修正过滤不可预定车次功能失效的问题(2012.12.11铁道部最新修改)
* 修正自动刷新查询功能混乱的问题(2012.12.11铁道部最新修改)
* 修正自动预选乘客功能失效的问题(2012.12.11铁道部最新修改)
* 修正因铁道部的弹出框出错而导致重新查询的问题(2012.12.11铁道部最新修改)
* -----------------------------------------------------------
* 提示：如果您发现车次的提示信息无法显示，这是铁道部的问题，请不要怪责老衲 =。=
* -----------------------------------------------------------
* (新功能陆续开发中，为避免封杀咱不透露细节 #^_^#)

**版本：3.6.1，更新时间：2012.12.18**
* 支持预先选择席别并自动选中
* 修正部分情况下可能导致的自动选择乘客失败的问题
* 其它细节调整

**版本：3.6.2，更新时间：2012.12.29**
* 跟进最近修改，解决提交时显示非法提交的错误 (感谢 cutefelix 比作者还快的手 =。=)
* 增加预先选择上下铺功能，显示预定界面的上下铺选择（但作者无法保证一定起效）
* 其它细节调整

**版本：3.6.4，更新时间：2012.12.29**
* 修正因铁道部改签页面程序问题导致的无法自动刷新（检测和刷新流程重写了）
* 增加对查票结果中星号（*）的处理
* 取消记录部分请求（因为有同学担心隐私泄漏）
* 对遨游3/4做兼容性改进（取消点击日期下拉时会弹重复安装的提示）

**版本：3.6.5，更新时间：2012.12.29**
* 修正在3.6.4版本中导致的学生票刷新BUG

**版本：3.6.7，更新时间：2012.12.30**
* 修改自动预定逻辑, 现在预定当有多个车次有效时, 将会按照列表的顺序进行优先判定, 而不再是查询结果中的顺序
* 修正取消自动预定时依然会自动预定的BUG
* 修正通過查詢介面設置的自動選中上下鋪可能未能在预定界面设置的BUG
* 修正取消自动刷新无效的BUG（这个BUG是在3.6.5修正版中修复的）
* 部分界面用语的调整(主要是日志部分)

**版本：3.7.0，更新时间：2013.1.1**
* 祝各位新年快乐
* 增加保存查的车次类型功能
* 增加过滤发到站或始发站不完全匹配的车次的功能
* 更新预售时间查询链接

**版本：3.7.1/2，更新时间：2013.1.1**
* 修正前版本中部分配置保存不了的BUG
* 修改过滤站点不匹配行为，直接隐藏对应车次
* 调整交换站点按钮样式，避免在Firefox下换行

**版本：3.8.0**
* 改进站点过滤，修正部分情况下未能过滤的BUG（不可预订车次），可以发到站分开过滤
* 修正在自动预定列表和黑名单中存在“|”符号时，保存后会被替换为换行的BUG
* 支付页面增加获得在IE中打开的代码（感谢xphelper提交的代码）
* 其它部分细节修改


**版本：3.8.2**
* 增加对取消订单后跳转的页面的自动的支持
* 预先选择席别后增加自动调整查询结果中的席别过滤选项
* 音乐地址同时提供HTTP和HTTPS的（但是好像依然不稳定，可以提供HTTPS协议音乐地址的同学请联系作者）
* 其它相关逻辑及提示上的修正


**版本：3.8.5**
* 登录页面增加起售日期提示和查询
* 增加保持在线功能（即使不刷新只是挂着也会每隔一分钟提交一次请求防止掉线）
* 新增服务器时间显示以及本地时间和服务器差额时间显示
* 修正注册后无法刷新整页(框架时)
* 修正谷歌浏览器下安装脚本版本时显示版本号不正确


**版本：3.8.6**
* 修正淘宝浏览器等专版中的反复弹注册失败的提示


**版本：3.9.0**
* 优化自动预定流程，提供全新的席别优先判定，允许优先选择级别
* 为Firefox启用全新的自动更新流程，检测升级更及时准确方便
* 增强谷歌浏览器下的版本升级检测，提高稳定性
* 修正服务器时间和本地时间差的负数显示问题
* 修改部分废话，精简文字量，捎带卖卖萌（卖萌无罪……）


**版本：4.0.0**
* 全新的自动提交订单功能，允许你在查询界面预先填写验证码并全自动提交
* 添加车次过滤白名单，在白名单中的车次将不会被过滤
* 修改黑名单和自动预定列表为席别优先级一样的选择模式
* 修改添加名单逻辑，现在自动预定和黑名单直接点击车次即可，不需要弹出层
* 修改席别选择；增加全部席别按钮；当不优选席别时，改为选中所有席别
* 重新加入被铁道部移除的上下铺选择下拉框，当然，加着玩儿，有效果更好，没效果……咱大肚能容那啥……
* 席别优先选择中加入硬座的无座
* 添加对在支付页面点击取消订单后跳回的查询页面的功能支持
* 增加清除已保存配置的功能按键
* 更新部分页面展示内容及效果, 增加部分选项提示，调整页面高度尽量避免太多滚动条
* 修正预定界面上的『显示帮助』的配置保存问题(真是个古老的BUG……)。
* 有童鞋提醒我一周年了……一看记录果然2012年1月9日发布的1.0版……一周年之际发布4.0版，感谢各位的支持和鼓励，希望每一位同学都能顺利地回家，2013都能收获自己想要的，不管是高雅的爱情还是庸俗的钱财 :-)


**版本：4.0.1**
* 解决预定页只能提交一次的限制，出现后台错误时自动刷新预定；其它细节修改；

**版本：4.0.2**
* 查询界面增加IE登录按钮；
* 修复主动打开设置中的IE登录时没有代码的小问题；
* 部分功能BUG修正和优化

**版本：4.0.3**
* 修改有席别优选存在时的优选顺序，调整为先席别再车次优选

官方网站
---------------------

* [官方发布主页](http://www.fishlee.net/soft/44/)
* [作者的腾讯微博](http://t.qq.com/ccfish)
* [项目主页@GitHub](https://github.com/iccfish/12306_ticket_helper)

相关资料
---------------------

* 感谢所有开发过相关脚本，以及作出贡献的前人们。


[遨游3]: http://www.maxthon.cn/mx3/
[软件主页]: http://www.fishlee.net/soft/44/
[腾讯微博]: http://t.qq.com/ccfish/
[木鱼]: http://www.fishlee.net/ "木鱼的软件主页"
[12306.CN]: http://dynamic.12306.cn/otsweb/ "12306.CN 购票网站"
[Chrome]: https://www.google.com/chrome/ "Google Chrome"
[Firefox]: http://www.mozilla.org/en-US/firefox/all.html "Firefox"
[猎豹]: http://www.liebao.cn/ "猎豹浏览器"
