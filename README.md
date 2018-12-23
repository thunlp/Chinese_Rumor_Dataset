# 中文谣言数据

该数据为从新浪微博不实信息举报平台抓取的中文谣言数据，分为两个部分。其中当前目录下的数据集仅包含谣言原微博，不包含转发/评论信息；而CED_Dataset中是包含转发/评论信息的中文谣言数据集。

## 数据集介绍

第一部分数据集（./rumors_v170613.json）共包含从2009年9月4日至2017年6月12日的31669条谣言。文件中，每一行为一条json格式的谣言数据，字段释义如下：

* **rumorCode**: 该条谣言的唯一编码，可以通过该编码直接访问该谣言举报页面。
* **title**: 该条谣言被举报的标题内容
* **informerName**: 举报者微博名称
* **informerUrl**: 举报者微博链接
* **rumormongerName**: 发布谣言者的微博名称
* **rumormongerUr**: 发布谣言者的微博链接
* **rumorText**: 谣言内容
* **visitTimes**: 该谣言被访问次数
* **result**: 该谣言审查结果
* **publishTime**: 该谣言被举报时间

### 引用

如果您使用该数据集，请引用以下论文：

* 中文：

```
	@article{liu2015rumors,
	  title={中文社交媒体谣言统计语义分析},
	  author={刘知远 and 张乐 and 涂存超 and 孙茂松},
	  journal={中国科学: 信息科学},
	  volume={12},
	  pages={1536--1546},
	  year={2015}
	}
```

* English：

```
	@article{liu2015rumors,
	  title={Statistical and semantic analysis of rumors in Chinese social media},
	  author={Liu, Zhiyuan and Zhang, Le and Tu, Cunchao and Sun, Maosong},
	  journal={Scientia Sinica Informationis},
	  volume={45},
	  number={12},
	  pages={1536},
	  year={2015}
	}
```

第二部分数据集（CED_Dataset）包含与微博原文相关的转发与评论信息，数据集中共包含谣言1538条和非谣言1849条。该数据集分为微博原文与其转发/评论内容。其中所有微博原文（包含谣言与非谣言）在original-microblog文件夹中，剩余两个文件夹non-rumor-repost和rumor-repost分别包含非谣言原文与谣言原文的对应的转发与评论信息。（该数据集中并不区分评论与转发）该数据文件中，每条原文，评论或评论均为json格式的数据，部分字段释义如下：

* 微博原文信息：
    *  **text**: 微博原文的文字内容
    *  **user**: 发布该条微博原文的用户信息
    *  **time**: 用户发布该条微博原文的时间（时间戳格式）
* 转发/评论信息：
    *  **uid**:  发布该转发/评论的用户ID
    *  **text**: 转发/评论的文字内容（若部分用户转发时不添加评论内容，该项无内容）
    *  **data**: 该转发/评论的发布时间（格式如：2014-07-24 14:37:38）

### 引用

如果您使用该数据集，请引用以下论文：

```
@article{song2018ced,
  title={CED: Credible Early Detection of Social Media Rumors},
  author={Song, Changhe and Tu, Cunchao and Yang, Cheng and Liu, Zhiyuan and Sun, Maosong},
  journal={arXiv preprint arXiv:1811.04175},
  year={2018}
}
```
