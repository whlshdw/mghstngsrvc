# 记录 mghstngsrvc

This a PicBed Repo! Image hosting service!

- github访问不稳定是dns造成的，可通过添加host解决 或 科学上网。
- github仓库容量有1G限制：可创建过个仓库

# github 图床

- 使用 github 做图床，配合PicGo 或者 chrome 插件 Picee 来上传图片到图片仓库。

- 访问大图片会下载：
https://raw.githubusercontent.com/sthwhl/Gallery/master/gallery/qhh_0

- 访问小图加载
https://raw.githubusercontent.com/sthwhl/Gallery/master/gallery-tiny/lock.png


# 通过jsDelivr引用资源 加速

- 可加载图片或者视频

- 使用方法1：https://cdn.jsdelivr.net/gh/用户名/仓库名@发布的版本号/文件路径

- https://cdn.jsdelivr.net/gh/user/repo@version/file

例：https://cdn.jsdelivr.net/gh/sthwhl/Gallery@latest1/gallery/qhh_0.jpg

- 使用方法2：https://cdn.jsdelivr.net/gh/用户名/仓库名@分支名/文件路径

例：https://cdn.jsdelivr.net/gh/sthwhl/Gallery@master/gallery/qhh_0.jpg

# 通过jsDelivr 缓存刷新

当网站更新时，如果CDN节点上数据没有及时更新，即便用户在浏览器使用 Ctrl +F5（win）或者 command+shift+R（mac）的强制刷新方式使浏览器端的缓存失效，也会因为CDN边缘节点没有同步最新数据而导致用户端未能及时更新。

对于 jsDelivr，缓存刷新的方式也很简单，只需将想刷新的链接的开头的cdn 更改为 purge

`https://cdn.jsdelivr.net/`

切换为

`https://purge.jsdelivr.net/`

在浏览器访问这个接口得出以下数据，返回status: ok，就代表完成

```
{"fastly":[{"status":"ok","id":"20756-1612456493-583384"},{"status":"ok","id":"20749-1612196515-1217151"},{"status":"ok","id":"20733-1612198481-1229986"},{"status":"ok","id":"20772-1612459680-552370"},{"status":"ok","id":"20741-1612201887-1245252"},{"status":"ok","id":"20764-1612459445-576858"},{"status":"ok","id":"20780-1612461576-540843"},{"status":"ok","id":"20759-1612442796-791746"},{"status":"ok","id":"20775-1612444982-789870"},{"status":"ok","id":"20743-1612444070-769594"}],"maxcdn":{"code":200},"cloudflare":true,"quantil":"<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n<response><message>success</message></response>"}
```


