
#微博谣言数据集

该数据为根据新浪微博不实信息举报平台抓取的中文谣言数据，并包含与微博原文相关的转发与评论信息。
数据集中共包含谣言1538条和非谣言1849条。

##数据集介绍

该数据集分为两部分，分别是微博原文与其转发/评论内容。其中所有微博原文（包含谣言与非谣言）在original-microblog文件夹中，
剩余两个文件夹non-rumor-repost和rumor-repost分别包含非谣言原文与谣言原文的对应的转发与评论信息。
（该数据集中并不区分评论与转发）

##数据形式

该数据文件中，每条原文，评论或评论均为json格式的数据，部分字段释义如下：

* 微博原文信息：
    *  **text**: 微博原文的文字内容
    *  **user**: 发布该条微博原文的用户信息
    *  **time**: 用户发布该条微博原文的时间（时间戳格式）
* 转发/评论信息：
    *  **uid**:  发布该转发/评论的用户ID
    *  **text**: 转发/评论的文字内容（若部分用户转发时不添加评论内容，该项无内容）
    *  **data**: 该转发/评论的发布时间（格式如：2014-07-24 14:37:38）


##引用

如果您使用该数据集，请引用以下论文：

```
@article{song2018ced,
  title={CED: Credible Early Detection of Social Media Rumors},
  author={Song, Changhe and Tu, Cunchao and Yang, Cheng and Liu, Zhiyuan and Sun, Maosong},
  journal={arXiv preprint arXiv:1811.04175},
  year={2018}
}
```