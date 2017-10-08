## 概要

这个数据可视化使用Kaggle上的[Titanic乘客数据](https://www.kaggle.com/c/titanic/data)来展现各种不同乘客人群的存活率。[Titanic](https://en.wikipedia.org/wiki/RMS_Titanic)上有2435名乘客，超过1500人死于这次海难。这个可视化所使用的数据集只有891名乘客的数据。

## 设计

### 初稿

* 这个可视化用柱状图来展示不同人群的存活率和死亡率。横轴来代表某个特征对乘客的划分，纵轴代表不同人群的存活率和死亡率的百分比。由于不同的分类中的人数可能差距比较大，在柱状图中添加了相应类别的人数以供参考。
* 首先要分析使用哪些特征去划分乘客。数据集提供了乘客的生死、船票等级、性别、年龄、船上兄弟或配偶人数、船上子女或父母人数、船票编号、票价、船舱编号和出发港口。乘客的生死是要最终展示的目标，船票等级、性别、年龄、船上兄弟或配偶人数都是能够影响乘客生死的重要因素。船票编号、船舱编号和出发港口都不是划分乘客的好选择，票价可以由船票等级替代，船上子女或父母人数在探索性展示中区分度并不是很好也没有选用。
* 在救援过程中首要遵循女士优先原则，不论何种人群女性都应该得到优先获救的机会，也就是男女的存活率会有很大的不同，所以我对所有其他分类进行展示时，都是男女并列的。
* 数据集中的年龄是数字，并不太适宜分类。我主观的把年龄分成了四类儿童（13岁以下）、青少年（13岁~18岁）、成人（19岁~60岁）和老人（60岁以上）。数据集中年龄数据有一些缺失，针对年龄的可视化并不包括缺失年龄的乘客。
* 可以通过点击下方不同的按钮，转换对不同特征的可视化。

## 反馈
* 你在这个可视化中注意到什么？
* 你对这个可视化有什么问题吗？
* 你是否注意到数据关系？
* 你觉得这个可视化主要表达了什么？
* 这个图形中你有什么不明白的地方吗？


## 资源

* [数据添加年龄分类](http://pandas.pydata.org/pandas-docs/stable/generated/pandas.cut.html)
* [按钮居中](https://stackoverflow.com/questions/17629788/aligning-buttons-in-css-html-in-one-line-horizontally-w-text)
* [按钮生成](https://stackoverflow.com/questions/15244182/d3-create-buttons-from-an-array-of-string-containing-names)
* [SVG居中](https://stackoverflow.com/questions/28232333/how-to-move-svgs-position-in-d3)
* [直方图中添加数据](https://stackoverflow.com/questions/30788524/d3-bar-chart-append-text-to-bar)