# myCode
- 遍历：41ms	4664KB
```python
import sys

lines = sys.stdin.readlines()
sums = []
for line in lines:
    line.strip()
    a = line.split()
    for i in range(len(a)):
        if a[i] not in sums:
            sums.append(a[i])
        else:
            continue
print(len(sums))
```



