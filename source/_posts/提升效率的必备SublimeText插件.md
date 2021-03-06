---
title: 提升效率的必备SublimeText插件
categories:
  - 开发工具
tags:
  - SublimeText
---



# 安装package control

使用 

```
 Ctrl + `
```

  打开命令面板，输入

```
import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

安装插件使用命令

```
Ctrl + Shift + P
```

输入`package control: install package`

插件可以在 https://packagecontrol.io/ 中查找



# 常用插件

## 代码提示与自动完成

### [<u>All Autocomplete</u>](https://packagecontrol.io/packages/All%20Autocomplete) 

　　Sublime Text 默认的 Autocomplete 功能只考虑当前的文件，而 AllAutocomplete 插件会搜索所有打开的文件来寻找匹配的提示词。

### [<u>AutoFileName</u>](https://packagecontrol.io/packages/AutoFileName) 

　　快速在文件中写路径，如`img`标签的`src`。 

### [<u>Autoprefixer</u>](https://packagecontrol.io/packages/Autoprefixer) 

　　这个插件主要应用css的浏览器兼容书写，自动分析你的css文件，解析出新的css文件，可以配置你要兼容的浏览器，不过这个插件要在之前安装nodejs

​	**使用方法**

​	选中要进行分析的css代码，`ctrl`+`shift`+`P`,输入Autoprefixer CSS即可

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/sublime/001.gif)





## 功能增强

### [<u>SublimeServer</u>](https://packagecontrol.io/packages/SublimeServer) 

使用sublime开启一个本地服务器，右键可以看到View in sublime server

### [<u>rem-unit</u>](https://packagecontrol.io/packages/rem-unit) 

一个CSS的px值转rem值的Sublime Text 3自动完成插件。

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0054.gif)

### [<u>SideBarEnhancements</u>](https://packagecontrol.io/packages/SideBarEnhancements) 

　　增强右键菜单文件操作功能

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/sublime/002.png)



## 视觉体验

### [<u>BracketHighlighter</u>](https://packagecontrol.io/packages/BracketHighlighter) 

　　配置文件的高亮设置，让你的代码有不同的颜色区分该插件提供配对标签，或大括号或字符引号的配对高亮显示，算是对系统高亮的加强吧。 

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/sublime/003.png)

### [<u>Color Highlighter</u>](https://packagecontrol.io/packages/Color%20Highlighter) 

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/sublime/004.png)

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0056.gif)

Color Picker，使用快捷键`Ctrl + Shift + C` 

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/sublime/005.gif)



## 代码格式化

### [<u>Pretty JSON</u>](https://packagecontrol.io/packages/Pretty%20JSON) 

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0057.gif)

### [<u>HTML-CSS-JS Prettify</u>](https://packagecontrol.io/packages/HTML-CSS-JS%20Prettify) 

　　全能序列化，需要指定Nodejs路径

​	配置:

> HTMLPrettify.sublime-settings

```json
{
  // 配置路径
  "node_path": {
    "windows": "D:/Program Files/nodejs/node.exe",
    "linux": "/usr/bin/nodejs",
    "osx": "/usr/local/bin/node"
  },

  // 保存时自动格式化
  "format_on_save": false,

  // 只格式化选中部分
  "format_selection_only": true,

  // Log the settings passed to the prettifier from `.jsbeautifyrc`.
  "print_diagnostics": true
}
```

> Default (Windows).sublime-keymap

```json
[{
  "keys": ["ctrl+shift+h"],
  "command": "htmlprettify"
}, {
  "keys": ["ctrl+alt+h", "p"],
  "command": "htmlprettify_set_prettify_prefs"
}, {
  "keys": ["shift+alt+h", "o"],
  "command": "htmlprettify_set_plugin_options"
}, {
  "keys": ["ctrl+alt+h", "k"],
  "command": "htmlprettify_set_keyboard_shortcuts"
}, {
  "keys": ["ctrl+alt+h", "n"],
  "command": "htmlprettify_set_node_path"
}]
```

### [<u>DeleteBlankLines</u>](https://packagecontrol.io/packages/DeleteBlankLines) 

删除空白行

操作步骤：

1.  选中要删除空白行的文本范围，一般是ctrl+A直接全选
2.  通过ctrl+alt+backspace执行一键去除空白行功能




## 语言包

### [<u>ChineseLocalization</u>](https://packagecontrol.io/packages/ChineseLocalizations) 

　　各国语言包

### [<u>GBK Support</u>](https://packagecontrol.io/packages/GBK%20Support) 

​	支持GBK编码格式



## 指定环境

### react开发插件

#### babel

​	支持ES6、React.js、jsx代码语法高亮。

​	**安装**

​	`command+shift+p` -> `install package` -> `babel`

​	**配置**

​	该插件不需要额外配置，在打开`.js`或`.jsx`后缀的文件，直接选择`Babel`为对应的语法就可以了。

#### [<u>Emmet</u>](https://packagecontrol.io/packages/Emmet) 

​	Emmet的前身是大名鼎鼎的Zen coding，它使用仿CSS选择器的语法来生成代码，大大提高了HTML/CSS代码编写的速度。还可以自动扩展react的className，我们要做的，只是安装好它之后稍微做下配置修改，就可以愉快的开撸了。

​	**安装**

​	`command+shift+p` -> `install package` -> `emmet`

​	**配置**

​	打开菜单`Preferences` -> `Package Settings` -> `Emmet` -> `Key Bindings - User`

​	将下面代码贴进去保存。更详细的规则可以参考 [emmet-sublime文档](https://github.com/sergeche/emmet-sublime#how-to-expand-abbreviations-with-tab-in-other-syntaxes) 

```json
[{
    "keys": ["tab"],
    "command": "expand_abbreviation_by_tab",

    // put comma-separated syntax selectors for which 
    // you want to expandEmmet abbreviations into "operand" key 
    // instead of SCOPE_SELECTOR.
    // Examples: source.js, text.html - source
    "context": [{
            "operand": "source.js",
            "operator": "equal",
            "match_all": true,
            "key": "selector"
        },

        // run only if there's no selected text
        {
            "match_all": true,
            "key": "selection_empty"
        },

        // don't work if there are active tabstops
        {
            "operator": "equal",
            "operand": false,
            "match_all": true,
            "key": "has_next_field"
        },

        // don't work if completion popup is visible and you
        // want to insert completion with Tab. If you want to
        // expand Emmet with Tab even if popup is visible -- 
        // remove this section
        {
            "operand": false,
            "operator": "equal",
            "match_all": true,
            "key": "auto_complete_visible"
        }, {
            "match_all": true,
            "key": "is_abbreviation"
        }
    ]
}]
```

#### [<u>jsformat</u>](https://packagecontrol.io/packages/JsFormat) 

​	`jsformat`是sublime上js格式化比较好用的插件之一，通过修改它的`e4x`属性可以使它支持`jsx`。

​	**安装**

​	`command+shift+p` -> `install package` -> `jsformat`

​	**配置**

​	打开菜单`Preferences` -> `Package Settings` -> `JsFormat` -> `Settings - User`，将下面代码贴进去保存。

```
{
  "e4x": true,
  // jsformat options
  "format_on_save": true,
}
```

#### SublimeLinter-jsx

​	jsx的验证插件



## 其他

### SublimeCodeIntel

　　一个全功能的 Sublime Text 代码自动完成引擎

　　支持的语言挺多的（JavaScript, Mason, XBL, XUL, RHTML, SCSS, Python, HTML, Ruby, Python3, XML, Sass, XSLT, Django, HTML5, Perl, CSS, Twig, Less, Smarty, Node.js, Tcl, TemplateToolkit, PHP.）

### CTags

　　实在方法跳转，跳转到你方法

　　之后在win7下或者linux下安装ctags软件

1. 打开ctags插件包的use-setting配置"command": "d:/IDE/ctags58/ctags.exe"这个路径是下载ctags的安装路径
2. 这个插件能跨文件跳转，跳转到指定函数声明的地方(ctrl+alt+左键)。 使用package control 搜索ctags 进行安装（安装ctags插件就可以了， 还有一个 CTags for PHP 插件没什么用）,注意安装好插件后要需要安装ctags命令。window 下载 ctags.exe  http://vdisk.weibo.com/s/7QZd7 。 将ctags.exe文件放在一个环境变量能访问到的地方。打开cmd， 输入ctags，如果有这个命令，证明成功了。ubuntu下安装运行命令：sudo apt-get install exuberant-ctags 。然后在**sublime项目文件夹右键**， 会出       现Ctag:Rebuild Tags 的菜单。点击它，然后会**生成.tags的文件** 然后在你代码中， 光标放在某个函数上， 点击 就可以跳转到函数声明的地方。



### CSS Comments

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0058.gif)

### CSS Format

　　css序列化插件，支持默认多种序列方案，还可以自己配置自己喜欢的

### DocBlockr

　　DocBlocker 是在Sublime平台上开发一款自动补全代码插件，支持JavaScript (including ES6), PHP, ActionScript, Haxe, CoffeeScript, TypeScript, Java, Apex, Groovy, Objective C, C, C++ and Rust.等众多语言

​	DocBlockr 可以使你很方便地对代码建立文档。它会解析函数，变量，和参数，根据它们自动生成文档范式，你的工作就是去填充对应的说明。

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0059.gif)

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0060.gif)

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0061.gif)

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0062.gif)

### JavaScript Completions

　　js最基本的api快查片段

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0063.gif)

### Keymaps

　　快速查找所有插件的快捷键

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0064.gif)

### LiveStyle

　　LiveStyle是Chrome中提高开发效率的一款CSS编辑器插件。利用LiveStyle和Sublime Text3编辑器结合可实现可视化开发，一次配置，简单易用！，并且最近支持less,scss

　　你本地css文件可以和浏览器的css文件映射，同步到本地，但是必须在chrome上运行，chrome必须安装相应的插件

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0065.png)









### SublimeTmpl

　　创建常用文件初始模板，必须html,css,js模板

### Alignment

　　这个插件让你能对齐你的代码，包括 PHP、CSS 和 Javascript。代码看起来更简洁和可读，便于编辑。

### PackageResourceViewer

　　通过这个特殊的插件，会给你查看和编辑SublimeText附带的不同的包带来很多方便。您也可以提取任何给定的包。这一行动将其复制到用户文件夹，以便您可以安全地对其进行编辑。

　　很多人苦恼不能修改左侧导航面板字体大小，用这个可以轻松办到

　　安装PackageResourceViewer 快捷键 ⌘(command)+⇧(shift)+P 打开 Command Palette 输入 Package Control:Install 回车，等待加载package列表 搜索并安装 PackageResourceViewer 包

　　最后，使用PackageResourceViewer打开Theme文件进行编辑 快捷键 ⌘(command)+⇧(shift)+P 打开 Command Palette 输入 PackageResourceViewer: Open Resource 回车，打开包列表 选择 Theme - Default，再选择 Default.sublimt-theme 搜索 　　sidebar_label，在 "class": "sidebar_label" 后边加一行："font.size": 18，将字体大小设置为18，保存。 好啦，大功告成！

　　如果觉得行间距太小，可以往上找下，有个class:"sidebartree"，调一下里边的rowpadding配置即可。

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0066.gif)

### Themr

　　sublime可以下载很多风格样式，用这个插件可以管理所有的风格

### Git

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0067.gif)

虽然名字看上去并不友好，但作为开发者的你肯定一眼就能明白它是干什么的。这个插件会将Git整合进你的SublimeText，使的你可以在SublimeText中运行Git命令，包括添加，提交文件，查看日志，文件注解以及其它Git功能。

### Terminal

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0068.gif)

这个插件可以让你在Sublime中直接使用终端打开你的项目文件夹，并支持使用快捷键。

### CSSComb

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0069.gif)

这是用来给CSS属性进行排序的格式化插件。如果你想保持的代码干净整洁，并且希望按一定的顺序排列（是不是有点强迫症了？），那么这个插件是一种有效解决的方案。特别是当你和其他有自己代码编写风格的开发者一同协作的时候。

### Trmmer

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0070.gif)

你知道当你编写代码时，由于错误或别的某些原因，会产生一些不必要的空格。需要注意的是多余的空格有时也会造成错误。这个插件会自动删除这些不必要的空格。

### MarkDown Editing

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0072.gif)

SublimeText不仅仅是能够查看和编辑 Markdown 文件，但它会视它们为格式很糟糕的纯文本。这个插件通过适当的颜色高亮和其它功能来更好地完成这些任务。

### FileDiffs

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0073.gif)

这个插件允许你看到SublimeText中两个不同文件的差异。你可以比较的对象可以是从剪贴板中复制的数据，或工程中的文件，当前打开的文件等。

### CanIUse

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0074.gif)

如果您想检查浏览器是否支持你包括在你的代码中的CSS和HTML元素，那么这是你需要的插件。所有您需要做的就是选择有疑问的元素，插件将为你做其余的事情。

### SASS Build

SASS Build 是一个编写CSS的预处理器。这个特别的插件将帮助你妥善构建包括压缩选项在内的SASS文件。一旦你安装了这个插件，你可以很容易地通过按Ctrl+ B（MAC系统是 Command +B）来启动它。

### FTPSync

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0075.gif)

默认情况下SublimeText不具备FTP的功能，如果你正在寻找能在您的SublimeText应用程序中使用的免费和易用的FTP工具，你可以考虑FTPSync。这是一个非常简单的FTP同步工具，它可以控制上传目标的多重命名。让我们知道您的想法。



## 语言提示插件

CSS3、Less、Sass、Scss、Jade、Styls、JSX



## 代码验证插件

### SublimeLinter

　　代码校验插件，支持多种语言，这个是主插件，如果想检测特定的文件需要单独下载

SublimeLinter-jshint

SublimeLinter-json

SublimeLinter-jsx



## 主题插件

拥有不同的主题可以触发创意和想法，你可能想使用这些插件来实现不同的主题，带来更好的和令人兴奋的前景。

### <u>[Colorsublime](https://packagecontrol.io/packages/Colorsublime)</u>

它允许您在Sublime Text中立即更改当前的颜色方案。

![](http://xiaoyulive.oss-cn-beijing.aliyuncs.com/imgs/0076.gif)

Lyte、Boxy Theme




# 后记

　　这些就是我们大部分要用到的，插件的网址如下，你可以找到你喜欢的插件

　　https://packagecontrol.io/browse



# 激活码

```
—– BEGIN LICENSE —–
Michael Barnes
Single User License
EA7E-821385
8A353C41 872A0D5C DF9B2950 AFF6F667
C458EA6D 8EA3C286 98D1D650 131A97AB
AA919AEC EF20E143 B361B1E7 4C8B7F04
B085E65E 2F5F5360 8489D422 FB8FC1AA
93F6323C FD7F7544 3F39C318 D95E6480
FCCC7561 8A4A1741 68FA4223 ADCEDE07
200C25BE DBBC4855 C4CFB774 C5EC138C
0FEC1CEF D9DCECEC D3A5DAD1 01316C36
—— END LICENSE ——
```



```
—– BEGIN LICENSE —–  
TwitterInc  
200 User License  
EA7E-890007  
1D77F72E 390CDD93 4DCBA022 FAF60790  
61AA12C0 A37081C5 D0316412 4584D136  
94D7F7D4 95BC8C1C 527DA828 560BB037  
D1EDDD8C AE7B379F 50C9D69D B35179EF  
2FE898C4 8E4277A8 555CE714 E1FB0E43  
D5D52613 C3D12E98 BC49967F 7652EED2  
9D2D2E61 67610860 6D338B72 5CF95C69  
E36B85CC 84991F19 7575D828 470A92AB  
—— END LICENSE ——  
```



# 参考资料

[常用的sublime text 3插件（很爽哦）](http://www.cnblogs.com/qingkong/p/5039527.html)

[20 个强大的 Sublime Text 插件 ](http://www.oschina.net/translate/20-powerful-sublimetext-plugins) 

[Sublime text 3 中Package Control 的安装与使用方法](https://devework.com/sublime-text-3-package-control.html) 

