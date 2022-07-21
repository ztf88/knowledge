[uiautomator2@github](https://github.com/openatx/uiautomator2)

uiautomator2可以轻松实现一些手机操作，完成打卡，或其他定时任务。

或者直接使用adb操作`os.system('adb <command>')`

```python
import uiautomator2 as u2

d = u2.connect()
print(d.info)
```


---
#python
#pythonlib