**关于闭包的定义**

​       在计算机科学中，闭包（Closure），又称为词法闭包（Lexical Closure）或者函数闭包（function closures），是引用了自由变量的函数。这个被引用的自由变量将和这个函数一同存在，即使已经离开了创造它的环境也不例外。

---

**python中元类一般的使用方式**

[Python 中的元编程](<https://www.ibm.com/developerworks/cn/analytics/library/ba-metaprogramming-python/index.html>)

- 抽象基类

  ```python
  class Vehicle(metaclass=ABCMeta):
      
      @abstractmethod
      def refill_tank(self, litres):
          pass
      
      @abstractmethod
      def move_ahead(self):
          pass
  ```

- 类的注册

  ```python
  handlers = {}
  class CustomMetaclass(type):
  	def __new__(meta, name, bases, attrs):
          cls = type.__new__(meta, name, bases, attrs)
          for ext in attrs["formats"]:
              handlers[ext] = cls
          return cls
      
  class Handler(metaclass=CustomMetaclass):
      formats = []
      
  class ImageHandler(Handler):
      formats = ["jpeg", "png"]
      
  class AudioHandler(Handler):
      formats = ["mp3", "wav"]
  ```

  

- 在库和框架中创建API

---

**一个简单的类装饰器**

```python
from functools import wraps
import random
import time

def wait_random(min_wait=1, max_wait=30):
    def inner_function(func):
        @warps(func)
        def wrapper(*args, **kwargs):
            time.sleep(random.randint(min_wait, max_wait))
            return func(*args, **kwargs)
        return wrapper
    return inner_function

def classwrapper(cls):
    for name, cal in vars(cls).items():
        if callable(val):
            setattr(cls, name, wait_random()(val))
     return cls
```

