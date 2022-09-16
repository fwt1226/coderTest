# sys.stdin
sys.stdin == open（'XX.txt','r'）
## 读取方法
- 读取单行
```python
# 输出为字符串
line = sys.stdin.readline()
```
- 读取全部
```python
# 输出为字符串
line = sys.stdin.readlines()
```
- strip()
```python
# 删除输出字符串首位字符（\n，\t等
line = sys.stdin.readline().strip()
```
- split()
```python
# 以空白为间隔拆分，输出字符串列表
line = sys.stdin.readline().split()
```
- split('x')
```python
# 以'x'为间隔拆分，输出字符串列表
line = sys.stdin.readline().split('x')
```
