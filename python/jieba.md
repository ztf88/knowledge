[jieba@github](https://github.com/fxsjy/jieba)

jieba是一个中文分词的python库，用于分析一些文本

```python
# encoding=utf-8
import jieba

seg_list = jieba.cut("我来到北京清华大学", cut_all=True)
print("Full Mode: " + "/ ".join(seg_list))  # 全模式
```

以下是使用jieba分析十九六中全会全文的脚本，同时也用到了[[wordcloud]]

```python
#!/usr/bin/python

# -*- coding:UTF-8 -*-

  

import jieba

from collections import Counter

from wordcloud import WordCloud

from PIL import Image

import numpy as np

  

text = open('./19th6.txt', 'r', encoding='UTF-8').read()

words = jieba.cut(text)

  

keywords = []

for word in words:

    if len(word) >= 4:

        keywords.append(word)

  

#result = Counter(keywords).most_common(50)

  

background_pic = './china.jpeg'

images = Image.open(background_pic)

maskImages = np.array(images)

  

content = ' '.join(keywords)

wc = WordCloud(

              font_path='./FZDBSJW.TTF',

              background_color='white',

              width=1600,

              height=900,

              mask=maskImages

              ).generate(content)

  

wc.to_file('ci.png')

  

print('Sucessed!')
```

---
#python
#pythonlib