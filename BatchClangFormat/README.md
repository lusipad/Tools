# BatchClangFormat

对指定文件夹下的文件进行批量格式化



## 开始

1. 将 LLVM 的 bin 添加到环境变量
2. 打开 Bash（比如说 Git Bash）
3. 筛选后缀并且格式化

```cpp
find /d/repos/plcopen -iname '*.h' -o -iname '*.cpp' | xargs clang-format -i
```



**使用指定配置文件**

将文件命名为 `.clang-format`，并且 cd 到文件所在路径

```
find /d/repos/plcopen -iname '*.h' -o -iname '*.cpp' | xargs clang-format -style=file -i
```



## 参考资料

1. [Clang-Format Style Options — Clang 20.0.0git documentation (llvm.org)](https://clang.llvm.org/docs/ClangFormatStyleOptions.html)
