# Chrome Workspace
使用Chrome实现在浏览器中编辑源代码

一般调试项目的CSS的时候，往往在页面中F12调试CSS样式，然后将调试好的样式再复制到源代码中，完成源代码的更新。<br>
在学习SASS的时候偶然发现了Chrome的一个很好用的工具Workspace，就在F12开发者工具中。

使用的条件：Chrome 版本 68.0.3440.106（正式版本） （32 位），Ruby Sass 3.5.7

1.Workspace 将在开发者工具中（F12）修改源文件，但是Chrome并不知道文件的具体位置，<br>
  所以需要Workspace建立映射关系来告诉Chrome修改哪个文件。
  
2.打开本地文件，打开页面，F12打开开发者工具界面，选择菜单中的settings，选中workspace，点击add folder，找到要映射的项目路径（源文件路径）。

3.然后就可以在F12的source中调试了，修改的部分将自动同步到源代码中。

----------------

#### 本地文件只支持编辑，不支持删除和重命名，一般用于编辑CSS,JS,HTML，多用于CSS，修改JS和HTML需要刷新页面才能执行。

#### 本地搭建的127.0.0.1服务中，同样不支持删除和重命名，而且HTML不能修改，但是在localhost中可以，不知道为什么。另外修改JS不需要刷新，直接调用。

#### 我使用了koala工具来监听、编译sass，修改了.scss文件后自动会修改编译出来的.css文件，所以这种方法也解决了sass在页面中调试困难的问题。<br>（我在source中看不到sass文件，需要等一下，可能是资源加载中吧，毕竟引入的不是.scss而是.css）


**************
看到一些文章说需要开启“开发者工具实验”再进行上述操作，但是我没有开启一样可以用。
开启方法：
使用Chrome进入chrome://flags/,找到Developer Tools experiments，然后启用它。

![test](https://github.com/myworldlh/Images-Warehouse/raw/master/pictures/奶油.JPG)
