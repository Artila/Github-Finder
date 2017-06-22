# Github-Finder

一个小功能，可以查找 Github 上的用户，直接显示用户的头像，资料和仓库。

> 原作者：Traversy Media，视频在 [YouTube](https://www.youtube.com/watch?v=lIKrfLWNsUI),当然也有人搬运的，国内在B站[jQuery & Ajax_ Build A Github Finder App](http://www.bilibili.com/video/av8235835/)。
> 这是我完成的代码，可以在 [Github](https://github.com/Artila/Github-Finder) 上观看，下载

主要涉及：
- **bootstrap** 构建网页
- **jQuery和ajax**

怎样获取 Github 的数据呢？

主要靠这个 https://api.github.com ，就是它的 api 啦。

想找用户：'https://api.github.com/users/' + username ，就是这么简单。

所以这是个很简单的小功能，对 bootstrap 和 jQuery 有一定了解的人可以在30分钟之内完成。

写这个的目的，主要是为了理清自己的思路。

首先，构建页面，这个就不自己写了，直接找个 bootstrap 模板，[最简单的](http://getbootstrap.com/examples/starter-template/)就足够了,把源代码 copy 过来。

也可以在 [Bootswatch](http://bootswatch.com/) 选择一个自己喜欢的 bootstrap 主题。

把不需要的部分删删减减，主要是 css 和 js 的引入，换成自己需要的，主要是 bootstrap 的 css 和 js ,记得选合适的版本。

还有 jQuery ，要放在  bootstrap 的链接前面，国内有很多合适的 cdn 。

我多加了一个 Tether ，这也是   bootstrap 4 必需的，放在前面，不然会报错。

别忘了引入自己的 js。

主页面做好了，就是数据方面了。

jQuery 里的 on() 负责事件处理程序，监控 keyup 的变化，就是输入框的内容。

ajax 来获取数据，必须的参数 url：  https://api.github.com/users。

请求成功后用 done 来处理数据，把所需的数据放在合适的地方呈现出来。

就这样，是不是很简单，如果写得慢的话，大概是对 bootstrap 和 jQuery 不熟悉的缘故。
