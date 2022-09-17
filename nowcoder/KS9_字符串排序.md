# 知识点
- sort()
```python
# narr表示一个数组列表

# 从小到大
narr.sort()
# 从大到小
narr.sort(reverse=True)
```

# myCode
- sort()：30ms	4620KB
```python
import sys

lines = sys.stdin.readlines()
M = int(lines[0].strip())
arr = []
for i in range(1,len(lines)):
    x = lines[i].strip()
    s = x[-6:]
    arr.append(int(s))
arr.sort()
for i in arr:
    print(i,end = '\n')
```

- 遍历：39ms	4600KB
```python
import sys

lines = sys.stdin.readlines()
M = int(lines[0].strip())
arr = []
for i in range(1,len(lines)):
    x = lines[i].strip()
    s = x[-6:]
    arr.append(int(s))

for i in range(0,len(arr)-1):
    for j in range(i+1,len(arr)):
        if arr[i] > arr[j]:
            arr[i], arr[j] = arr[j], arr[i]

for i in arr:
    print(i,end = '\n')

```
