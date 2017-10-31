# 项目预览

在这个项目中，你会得到一个基于 web 的用来读取 rss 源的应用。最开始的这个项目的开发者意识到了测试的价值，他们也已经把 [Jasmine](http://jasmine.github.io) 包含在了项目之中，而且甚至已经开始写他们第一个测试用例。但是不幸的是，他们决定去创建一个他们自己的公司，所以我们现在拿到的是一个缺乏完整测试用例的应用，这样是你会参与到这个项目的原因。

## 项目目的

测试是开发过程中一个很重要的部分，很多组织把一个标准的开发过程称之为测试驱动开发。意思就是开发人员在他们开始着手编写应用代码之前先写好测试用例。当然这个时候所有的测试用例都是通不过的，然后他们就开始编写应用代码使测试全部通过。

不管你是在一个推崇测试驱动开发的组织，或者是一个编写测试只是为了防止未来的开发中出现与已有代码冲突的 bug 的团队工作，测试都是我们要掌握的一项重要技能。

# 我如何完成这个项目

查看订阅阅读器项目的[评审标准](https://review.udacity.com/#!/projects/3442558598/rubric)

1. 编写测试，对allFeeds使用toBeDefined()和对allFeeds的length属性判断not.toBe(0)确定allFeeds是否存在。
2. 编写测试，对allFeeds对象中的每条反馈执行循环操作，使用toBeDefined()和not.toBe('')，判断源中的url和name都是被定义且不是空的。
3. 编写测试，确保菜单 (menu) 元素在默认情况下处于隐藏状态。使用.hasClass 函数判断是否含有menu-hidden，预期为true。
4. 编写测试，确保当点击菜单时， 菜单改变其可见性。测试应有两项期望：当点击时，菜单是否显示， 当再次点击时，菜单是否隐藏。通过trigger('click')触发点击操作，使用.hasClass 函数判断是否含有menu-hidden确定菜单是否显示。
5. 编写测试，保在调用并执行 loadFeed 函数后， 在 .feed 容器中至少存在一个 .entry 元素。loadFeed()是异步调用的，且有一个callback函数在所有内容完成后调用，所以结合beforeEach,done;在callback中调用done若loadFeed 函数被调用而且工作正常，则feed 容器元素里面至少有一个 .entry 的元素。获取.entry 元素数组的长度与0比较大小，大则成功。
6. 编写测试，确保每当 loadFeed 函数加载一条新反馈后， 内容会相应更改。根据上一个测试，将loadFeed调用两次，每次调用后，获取.feed中的html，两次html内容对比，不相等，即为成功

