# calibrerecipes
recipe for calibre

把 Recipe 脚本转化为 mobi 文件
和转换普通的电子书的格式一样，只需要输入以下命令即可开始进行转化。

`ebook-convert test.recipe test.mobi --output-profile kindle`

注意上面的代码中增加了一个参数 --output-profile kindle，这个参数的意思是根据 Kindle 设备做适配，如果不添加这个参数，转换出来的电子书会有一个对 Kindle 来说多余的翻页导航。

另外在转换的过程中也会有意外情况，比如由于资源链接被墙，或由于网络不稳定导致页面抓取失败。本例中抓取的博客由于引用了两张 Google 服务器上的图片，不使用代理就会抓取失败。

以上命令执行完毕后便可以得到最终的电子书文件 test.mobi，拷贝或推送到 Kindle 即可阅读。

提示1：如果你不想使用命令行工具，当然也可以使用 Calibre 界面上的“抓取新闻”功能来完成同样的工作。你只需要把编写好的 Recipe 代码粘贴到新建的 Recipe 脚本中，或者直接导入已有的 Recipe 脚本文件，然后和抓取 RSS 的操作一样，在“定期新闻下载”面板上选中“自定义脚本”，点击【立即下载】按钮即可完成转换。不过这种方法会始终带有翻页导航。

提示2：当然还有一个比较方便的转换方法，就是直接把 Recipe 脚本拖进 Calibre，然后像转换普通电子书那样进行转换，Calibre 会自动执行抓取工作，最终将抓取的数据转成目标格式。

[calibre API](https://manual.calibre-ebook.com/news_recipe.html)
