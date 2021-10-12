
# 谷腾堡小说数据：识别故事中隐藏的社会偏见


![image](https://user-images.githubusercontent.com/543384/131449340-a7be1c92-fb3c-4497-b318-e3d880dc8ed2.png)

- 开始 9.01
- 第一阶段 9.01-11.05
- 结束 11.05

https://www.heywhale.com/org/art_nju/competition/area/612a4eff39efe300170cdaf2/content/2

## 一、题目描述
### 赛题题目
识别故事中隐藏的社会偏见

### 赛题背景
社会偏见在现实社会当中根深蒂固，文化产品的创作和传播不断强化这这些社会偏见。社会偏见的表现形式多种多样，涉及人类生活的各个方面。如果故事当中嵌入了结构化的社会偏见，基于这些文化产品作为语料训练机器学习模型就会学习到这些偏见，并通过推荐系统等各种方式对社会现实产生影响。从文化产品当中识别出具体的社会偏见，揭示这些文化创作是如何以一种不易察觉但是强有力的方式来加深对性别、种族、社会阶层等方面的刻板印象，刻画其所带来的的潜在危险，有助于人们设计更好地机器学习模型和智能产品。

### 赛题任务
以平台数据为主要数据源，选手可自行增加其它来源数据（需在报告中注明数据来源，数据规模，来源归属等）。
本次任务提供来自谷腾堡网站（www.gutenburg.org) 的小说文本数据，参赛者需要合理运用文本处理技术与自然语言处理技术，对于提供的信息进行分析。通过分析小说的文本，总结叙事中的社会偏见的变化趋势，结合叙事相关的信息，讨论包括但不限于如下问题（一个或多个）：

- 叙事中的性别偏见
- 叙事中的文化偏见
- 叙事中的社会阶层偏见
- 叙事中的国家偏见
- 叙事中的种族偏见

探究此类问题鼓励参赛队伍深入了解小说的特点与社会偏见，获取其他公开数据进行综合分析，利用数据做观点支持，对于识别文本中的社会偏见提出建设性方案。本次任务原则上鼓励参赛队伍大胆创新，采纳新的方法、视角、理论，敢于对相关的数据与信息在相关性和因果性上进行大胆的假设和严谨的探究与论证。）

 

## 二、数据说明
竞赛数据来自谷腾堡网站 （www.gutenburg.org) 当中小说类型文本。数据提取由南京大学新闻传播学院计算传播学实验中心完成。数据包括两部分：1.小说的元数据；2. 小说文本数据。

![image](https://user-images.githubusercontent.com/543384/130960327-12332e96-c111-4862-8ecd-e8e928a21693.png)

![image](https://user-images.githubusercontent.com/543384/131466955-21c02153-7f07-4ed5-9b39-035973e5cd6b.png)

https://www.heywhale.com/mw-org/art_nju/project/612db3f9c9c30f001877f3a4

![image](https://user-images.githubusercontent.com/543384/131467241-7a7be6c1-764c-4223-92b2-8abfe9918ff5.png)

## Data Cleaning

https://github.com/kiasar/gutenberg_cleaner

> pip install gutenberg-cleaner

```Python
# Just removes lines that are part of the Project Gutenberg header or footer. 
# Doesnt go deeply in the text to remove other things like titles or footnotes or etc...
import glob

filenames = glob.glob('*.txt')

with open('filenames[0], 'r', encoding = 'utf8') as f:
    lines = f.readlines()
    
fiction = gutenberg_cleaner.simple_cleaner(' '.join(lines))
```

## Word Pairs for Affluence, Race, and Gender

https://github.com/KnowledgeLab/GeometryofCulture/tree/master/code/word_pairs


![image](https://user-images.githubusercontent.com/543384/131626146-c869c392-de7b-439f-b81d-a2c1223699c9.png)

## More information

A standardized Project Gutenberg corpus for statistical analysis of natural language and quantitative linguistics

Pipeline to generate the Standardized Project Gutenberg Corpus

- https://github.com/pgcorpus/gutenberg
- https://arxiv.org/pdf/1812.08092.pdf
- https://zenodo.org/record/2422561

## 问题反馈

1.赛题要求的“分析变化趋势”这个要求，是一定要呈现出来吗？是用提供的数据来分析趋势还是可以用给出的数据跟现有研究结果/数据库来分析？
   - 如果有更好。
   - 根据提供的数据分析趋势
2.最终提交文件的具体要求（内容，格式这些）
   - 提供一个PDF格式的文件
   - 内容包括：标题、摘要、简介、发现、结论、文献

