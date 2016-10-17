title: Composer
speaker: 李春强
url: https://github.com/ksky521/nodePPT
transition: slide3
theme: blue

[slide]

# Composer
## h1是作为封面用的，内部的都用h2
<small>演讲者：xxx</small>

[slide]
# 让Coding更简单
---

![](/img/composer.png)

[slide]
# Composer是什么
---

__Composer__是PHP用来管理依赖关系的工具。我们可以在项目中声明所依赖的外部工具库，Composer会帮我们安装这些依赖。

Github: https://github.com/composer/composer

[slide]
## 什么是包管理
----

* Node.js 有 npm {:&.rollIn}
* Python 有 pip
* blabla...

[slide]
### 来感受一下之前的代码方式
---

```php

require CODE_BASE . '/app/fuwu/ServiceStore.php';

$instance = new ServicStore();
$instance->someMethod();
```

__这只是一个简单的开始！__ {:&.rollIn}


[slide]

```php
require CODE_BASE . '/app/fuwu/Common.php';
require CODE_BASE . '/util/post/Post.php';
require CODE_BASE . '/util/redis/Redis.php';
require CODE_BASE . '/app/memcache/Memcache.php';
require CODE_BASE . '/app/foo/Foo.php';
require CODE_BASE . '/app/bar/Bar.php';
require CODE_BASE . '/app/chr/Chr.php';
require CODE_BASE . '/app/Nic/Nic.php';
require CODE_BASE . '/app/God/God.php';
//....
```

一行业务逻辑代码都没有写，我们已经做了这么多！![](/img/diao.gif)

[slide]

![](/img/ku.png)

[slide]
# 声明依赖
---

在项目目录下创建一个 `composer.json` 文件，指明依赖:

```json
{
	"name": "ganji/app",
	"require": {
		"symfony/http-foundation": "3.1.*",
		"symfony/http-kernel": "3.1.*",
		"illuminate/database": "5.3.*",
		"monolog/monolog": "~1.11",
		"twig/twig": "~1.26",
		"pimple/pimple": "~3.0.2",
		"nikic/fast-route": "~1.0.0"
	}
}
```

[slide]
# 安装依赖
---

接下来我们只需要执行：{:&.flexbox.vleft}

```bash
$ composer install --prefer-dist
```

[slide]

代码会被 Composer 自动下载到本地目录下的 `vendor`

![](/img/vendor.png)

[slide]
# 自动加载
---

Composer 提供了自动加载的特性，只需在你的代码的初始化部分中加入下面一行:{:&.flexbox.vleft}


```php
require __DIR__ . '/vendor/autoload.php';
```

接下来就可以享受自动加载带来的便利了！{:&.flexbox.vleft}

[slide]

# 样式展示 {:&.flexbox.vleft}
> nodePPT 让每个人都爱上做分享！

