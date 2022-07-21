[pyecharts](https://github.com/pyecharts/pyecharts)

pyecharts是一个制作动态图表的python库


截止2021年底全国B型保税区分布

```python
from pyecharts.globals import CurrentConfig, NotebookType
CurrentConfig.NOTEBOOK_TYPE = NotebookType.JUPYTER_LAB

from pyecharts import options as opts
from pyecharts.charts import Map

lists = [['北京', '1'],
 ['天津', '2'],
 ['河北', '3'],
 ['山西', '3'],
 ['内蒙古', '4'],
 ['辽宁', '4'],
 ['吉林', '2'],
 ['黑龙江', '2'],
 ['上海', '2'],
 ['江苏', '8'],
 ['浙江', '6'],
 ['安徽', '5'],
 ['福建', '4'],
 ['江西', '1'],
 ['山东', '6'],
 ['河南', '4'],
 ['湖北', '5'],
 ['湖南', '2'],
 ['广东', '7'],
 ['广西', '2'],
 ['海南', '1'],
 ['重庆', '3'],
 ['四川', '4'],
 ['云南', '2'],
 ['甘肃', '1'],
 ['青海', '1'],
 ['宁夏', '1'],
 ['新疆', '2']]


c = (
    Map()
    .add("全国B型保税区分布",lists, "china")
    .set_global_opts(
        title_opts=opts.TitleOpts(title="全国B型保税区分布"),
        visualmap_opts=opts.VisualMapOpts(max_=10),
    )
)

c.load_javascript()

c.render_notebook()
```

---
#python
#pythonlib