# DSND-project--Recommendations_with_IBM
## Background
分析用户与 IBM Watson Studio 平台上的文章进行的互动，并向他们推荐他们可能会喜欢的文章。

## Required Libraries
* python 3.6
* pandas
* numpy
* matplotlib
* pickle

## task process
1.Explore and Analyze the data
* 通过探索并分析数据，初步了解数据规律，如：用户与数据集中的文章的交互、数据分布。

2.基于排名的推荐方法
* 通过用户与文章的互动频率来判断文章的热门程度。

3.基于user-user的协同过滤方法：
* create_user_item_matrix函数：用户与某篇文章互动了，则在该文章所在的列与用户行形成的单元格中填充 1。无论用户与文章互动了多少次，都填充 1；如果用户与文章没有互动，则在该文章所在的列与用户行形成的单元格中填充 0。
* find_similar_users函数：接受 user_id，并提供与该用户最相似的有序用户列表（从最相似到最不相似）。
* user_user_recs、get_article_names函数：使用用户查找可以推荐的文章，返回向每个用户推荐的文章。
* get_top_sorted_users函数：按总互动次数从多到少对用户进行排名。

4.基于content的推荐方法：
* 对与某个术语相关的文章进行从高到低排名。

5.SVD-矩阵分解
* 使用SVD预测排名。
