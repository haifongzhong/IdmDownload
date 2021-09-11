## IDM下载豆丁官网资料

![image-20210911160824412](C:\Users\haifongzhong\AppData\Roaming\Typora\typora-user-images\image-20210911160824412.png)

​	①使用前务必确保浏览器安装了internetdownload插件，简称IDM

​	②安装文件目录中的idm拓展文件下的exe文件，双击即可，卸载双击即可。

​	③打开Debug文件夹下，双击ConsoleApplication1.exe文件

![image-20210911161349726](C:\Users\haifongzhong\AppData\Roaming\Typora\typora-user-images\image-20210911161349726.png)

​	④输入来在豆丁书房抓取的文件连接（例：https://docimg1.docin.com/docinpic.jsp?file=410960029&width=1000&sid=--oouFb138yQDk5F6mN1fapgA9Z5X3NNfXSrDV68D*Sbekbwh66XnQqe7-e0GW*t&pageno=1），最后一位代表我们要下载的页数，比如例子中的为第一页，所以要将等于号后的“1”删除，输入如下：

![image-20210911161750911](C:\Users\haifongzhong\AppData\Roaming\Typora\typora-user-images\image-20210911161750911.png)

​	⑤此时Debug文件下会产生一个“idmDownload.ef2”文件，原本有的已经更新，☛右击 ☛打开方式 ☛选择IDM EF2 解析工具，点击解析。

​	⑥解析会启动idm，运气好不会自动下载，运气会有几个文件提前下载，点击windows运行程序，进入idm任务列表，最好把以前下载的任务列表清除一下，发现运气比较差，部分已经下载了，不过没关系，点击开始列队。

![image-20210911162637808](C:\Users\haifongzhong\AppData\Roaming\Typora\typora-user-images\image-20210911162637808.png)

​	⑦下载完桌面自动生成了一个fileImg的文件夹，打开发现都是下载下来的图片，Ctrl+A全选，将图片合并在PDF文件中，这里我使用的是Adobe Acrobat Pro DC，不知道的小伙伴可以百度下载一个破解版，好使。



------

```tex
到这里有人就问，这些不是直接用idm的批量下载不是可以解决吗，这就错了，我写这个是为了弥补idm的批量下载的两个缺陷，第一个缺陷：通配符（*）只能在连接中出现一次，但是，我们从豆丁图书获取的连接都是带有多个通配符的，所以，这里就导致我们不能使用批量下载这个功能。第二个缺陷：了解过.ef2文件的都知道，可以在idm中直接导入ef2文件产生idm下载队列，我们可以把连接复制到一个ef2文件中就可以解决了批量下载的问题了，显然我也是从这个想法出发去解决问题的，所以简单的复制连接到ef2肯定是用问题的，问题一，麻烦！问题二，idm用这样产生的文件名是默认的文件名，这和它解析连接的速度有关，所以当我们用下载下来的图片组装成PDF文件时，页码肯定是会乱序的，所以借用ef2文件解析后，不但可以对图片批量命名，在后面生成的页码也是不会乱序。
```

