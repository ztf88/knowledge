

[easyocr@pypi](https://pypi.org/project/easyocr/)

easyocr是一个免费开源的ocr识别python库
```python
import easyocr
reader = easyocr.Reader(['ch_sim','en']) # this needs to run only once to load the model into memory
result = reader.readtext('chinese.jpg')
```

---
#python
#pythonlib