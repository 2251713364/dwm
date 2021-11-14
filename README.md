# dwm -dynamic window manager
================================

dwm is an extremely fast, small, and dynamic window manager for X.


Requirements
------------
In order to build dwm you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.




## patches

### autostart
开启dwm时自动运行一些脚本
### dwm-alpha
状态栏透明
### awesomebar
让状态栏显示窗口名字
### fullscreen
让窗口全屏
### hide_vacant_tags
只显示有窗口的标签
### pretag
不同的标签可以使用不同的排列方式
### noborder
状态栏视觉效果
### viewontag
将窗口移到另一个标签时，切换到相应的标签
### rotatestack
转换某一标签内窗口的顺序
### scratchpad
临时打开一个小窗口
### vanitygaps
给窗口之间增加一些小空隙
