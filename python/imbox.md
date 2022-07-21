[imbox@github](https://github.com/martinrusev/imbox)

imbox是一个好用的读取邮件的python库

```python
from imbox import Imbox

# SSL Context docs https://docs.python.org/3/library/ssl.html#ssl.create_default_context

with Imbox('imap.gmail.com',
        username='username',
        password='password',
        ssl=True,
        ssl_context=None,
        starttls=False) as imbox:

    # Gets all messages from the inbox
    all_inbox_messages = imbox.messages()

    # Unread messages
    unread_inbox_messages = imbox.messages(unread=True)

	 for uid, message in all_inbox_messages:
    # Every message is an object with the following keys

        message.sent_from
        message.sent_to
        message.subject
        message.headers
        message.message_id
        message.date
        message.body.plain
```

---
#python
#pythonlib