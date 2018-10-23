### python file operations summary

#### open file
```python
    # using with 可以避免文件未关闭导致的问题, 虽然我从没遇到过有什么问题 我估计是多线程的时候可能会有冲突吧
    with open(filePath, "w") as outPutFile:
        outPutFile.write("Venom")
```

#### read all files in directory
```python
# 遍寻根目录下的所有文件
import os
for dirs, paths, files in os.walk("."):
    for f in files:
        # 打开文件所需的地址需要此函数来赋予
        filePath = os.path.join(dirs, f)

```