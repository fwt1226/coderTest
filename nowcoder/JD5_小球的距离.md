# 核心代码模式
- 输出格式
```python
return xxx
```

# myCode
- 等比数列：24ms	6328KB
第一次下落距离：A+B+C+D
第二次开始依次减半，加上回弹有两倍运动距离：(1/2+1/4+...+1/n)*2
等比数列(1/2+1/4+...+1/n)求和为1
```python
# -*- coding:utf-8 -*-

class Balls:
    def calcDistance(self, A, B, C, D):
        # write code here
        return 3*(A+B+C+D)
```


