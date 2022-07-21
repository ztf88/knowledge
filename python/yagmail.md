[yagmail@github](https://github.com/kootenpv/yagmail)

yagmail是一个发送邮件的python库

```python
import yagmail
yag = yagmail.SMTP('mygmailusername', 'mygmailpassword')
contents = ['This is the body, and here is just text http://somedomain/image.png',
            'You can find an audio file attached.', '/local/path/song.mp3']
yag.send('to@someone.com', 'subject', contents)
```

---
#python
#pythonlib