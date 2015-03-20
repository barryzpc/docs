Symfony文档中文翻译
===================

翻译请求
--------

请在[issue](https://github.com/sfcn/symfony-docs-chs/issues)里提出翻译请求。

标题格式，以`book/controller.rst`为例：


```
[翻译请求] book/controller.rst
```

内容不限。

在发起新的issue前，请尝试使用搜索功能，确认翻译申请或翻译请求已经存在。如果翻译请求已经存在但是依然不在“WIP（进行中）”状态，可添加回复，比如回复“+1”，我们会根据回复的数量决定翻译的顺序。

翻译申请
--------

请在[issue](https://github.com/sfcn/symfony-docs-chs/issues)里提出翻译申请。

标题格式，以`book/controller.rst`为例：

```
[翻译申请] book/controller.rst
```

内容不限

在发起新的issue前，请尝试使用搜索功能，确认翻译申请或翻译请求已经存在。

翻译进度
--------

翻译进度将通过issue的标题体现：

* 无`[WIP]`前缀，任务还未开始;
* 有`[WIP]`前缀，任务正在进行中;
* 任务完成，我们将去掉标题中`[WIP]`并且关闭issue;

译者署名
--------

为尊重译者的劳动，翻译人员可在参与过翻译的文档大标题下方签署自己的名字。名字可带链接，链接可以是自己的邮箱地址、github帐号地址、微博地址、博客地址。但只可以放一个链接：

```
.. index::
   single: Controller

控制器
======

译者：`symfony.cn`_，`a Symfony fan`_

.. _symfony.cn: http://symfony.cn
.. _a Symfony fan: http://symfony.fans.blog
```

文档格式
--------

文档必须是[reStructuredText](http://docutils.sourceforge.net/rst.html)格式。翻译时可偷懒无需学习reStructuredText语法，但请一定做到*只替换原文里的文字，而不要改动其格式*。

版权说明
--------

所有中文文档遵循[CC BY 3.0](http://creativecommons.org/licenses/by/3.0/)协议。对于任何形式的使用，请保留译者的署名、网址、联系方式等信息。
