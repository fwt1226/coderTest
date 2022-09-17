# 题干
- 描述  
月神拿到一个新的数据集，其中每个样本都是一个字符串，样本的的后六位是纯数字，  
月神需要将所有样本的后六位数字提出来，转换成数字，并排序输出。  
注意：这里的排序并不是针对每个字符串的后六位，而是需要按数字大小顺序输出所有样本的后六位数字。  
月神要实现这样一个很简单的功能确没有时间，作为好朋友的你，一定能解决月神的烦恼，对吧。  
数据范围：字符串长度满足 1 \le n \le 100 \1≤n≤100  ，  
每组测试中包含 1 \le m \le 100 \1≤m≤100  个字符串
- 输入描述：  
每个测试用例的第一行是一个正整数 M ，表示数据集的样本数目；  
接下来输入 M 行，每行是数据集的一个样本，每个样本均是字符串，且后六位是数字字符。
- 输出描述：  
对每个数据集，输出所有样本的后六位构成的数字排序后的结果（每行输出一个样本的结果）

# 示例
- 输入：  
```
4
abc123455
cba312456
boyxx213456
cdwxa654321
```
- 输出：  
```
123455
213456
312456
654321
```


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
