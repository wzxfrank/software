vim命令


- 整理开智部落github的iss 内容
v/反常识：/d （查找“反常识：”在所有行，高亮显示）
替换语法 %s/替换前\N/替换后：/gc  全部确认输入a  把开智iss种金句卡+换行统一为金句卡：
	- %s/金句卡\N/金句卡：/gc 
	- v/第.章/d  (查找包含/目标/的行，如果没有就删除)
	- [vim删除进阶 - dp的日志 - 网易博客](http://dpinglee.blog.163.com/blog/static/144097753201202925213917/)
	- 经常处理一些文本，需要匹配某些特殊行，然后整行删除。:g/user-head/d
	- 扩展删除所有没有匹配的行:g!/要匹配的文字/d或者:v/要匹配的文字/d
	- :g/s*^$/d 删除所有空行
- 我常用的vim 命令   : ctrl+f 进入命令行窗口 在窗口菜单可关闭
> [(20)VIM 用正则表达式 批量替换文本，多行删除，复制，移动_php_sir_新浪博客](http://blog.sina.com.cn/s/blog_5f66526e0100wol5.html)
> :n1,n2 m n3     移动n1-n2行(包括n1,n2)到n3行之下；
:n1,n2 co n3    复制n1-n2行(包括n1,n2)到n3行之下；
:n1,n2 d        删除n1-n2行(包括n1,n2)行； 

- :%norm jkdd删除奇数行 
- :%norm jdd删除偶数行

> [Vim正则表达式[转] - 柯枫 - C++博客](http://www.cppblog.com/kefeng/archive/2010/10/20/130574.aspx)

v/第.章> （在豆瓣或深图复制图书目录到vim用， 效果是突出章节名，整理目录用）
g/^\s*$/d  删除空白行，不过更习惯在editplus用正则表达式（^[ \t]*\n）清除空行 [参考](http://blog.csdn.net/menghun_99520/article/details/2517970) 
延伸：[vim查找替换及正则表达式的使用 ](http://tanqisen.github.io/blog/2013/01/13/vim-search-replace-regex/)
vim 标签命令 
[Vim操作 解释 ruanyf/articles](https://github.com/ruanyf/articles/blob/master/dev/vim/operation.md)
[Vim 实用技术，第 1 部分: 实用技巧](https://www.ibm.com/developerworks/cn/linux/l-tip-vim1/index.html)
[超过 130 个你需要了解的 vim 命令 - maowang - 博客园](http://www.cnblogs.com/maowang1991/p/3572299.html)
Vim 键盘图中文版 - 小众软件![](http://img1.appinn.com/2010/03/vim_g.jpg)
:tabnew 新标签

> [Editing With Vim_野生技术协会_科技_bilibili_哔哩哔哩](http://www.bilibili.com/video/av8257061/)

命令模式输入i，a，进入插入模式，在当前光标前，后；I行首A行尾，O往前新建一行，o向后新建一行
r，替换单个，R替换之后的；w,W skip to next word/WORD;e,E move to end word/WORD
> this.is.test，e会移动到.is而E不会 WORD将this.is.test当成一个组

c,C删除单个或后续词并变为插入模式,x,X after ，before delete； dd 删除指定行 DD删除到行尾;Y复制P粘贴D剪切
/search forward？search backward <Enter> 回车查询 n,N 向下，上查找下一个
:nohlsearch清除高亮
:%s/tihuan1/tihuan2/g替换 全文中2替换1

vim 多窗口命令 splite vsplite   简写 sp  vsp
多窗口切换ctrl +ww
:Ex 开启目录浏览器，可以浏览当前目录下的所有文件，并可以选择
 
[用 Vim 对文本进行排序和删除重复行 - VimChina](http://www.vimchina.org/vimtips/2015-09-17-vim-sort-unique.html)
 >:h :sort查看帮助，:[range]sort[!] [i][u][n][x][o][/pattern/] :sort!	对全文逆序排列:'<,'>sort	对当前选中部分进行排序
 
在命令模式下键入大写的J来合并两行
 
[史上最强的Vim 配置文件（2008-3-21修正版） - redguardtoo的专栏 - CSDN博客](http://blog.csdn.net/redguardtoo/article/details/2204289)


[Installed GitHub App - GitBook](https://github.com/settings/installations/35236) 170627设置gitbook Repository access选项卡选了Only select repositories，结果新建新的gitbook的book发现不能选其他的repositories，google后没合适的答案。后边是自己在gitbook属性选中之前的图书找到设置界面。
[GitBook Clarity ](https://zhilidali.github.io/gitbook/)其中的gitbook发布与集成