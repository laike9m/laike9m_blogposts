[zhihu-card][1] 是我最近写的一个东西。受 [github-cards][2] 启发，既然知乎的影响越来越大，张兆杰们都把知乎的赞数粉丝数作为体现自身价值的筹码，为什么程序员们不能在自己的网站上展现知乎账户呢？于是就有了这么一个东西。

现在只要在页面中插入两行代码，填入你的 `user_hash` ，就能显示类似本站右侧的卡片。

```javascript
<div class="zhihu-card" data-userhash="your hash"></div>
<script src="//cdn.jsdelivr.net/zhihu-card/latest/widget.js"></script>
```

如果你有兴趣一起来改进，欢迎给项目提 issue 和 pr。

## 实现
鉴于之前有人问过实现原理，这里简单说一下。显然，如果直接去拿知乎的信息会遇到跨域问题，知乎不允许我们这么干。唯一的解决方法就是用一个 server 去获取用户信息，然后 zhihu-card 去访问 server。server 是拿 Go 写的，目前不开源，因为之后打算大改。

Enjoy.

[1]: https://github.com/laike9m/zhihu-card
[2]: https://github.com/lepture/github-cards