# 解析学术论文的引用，并提取其超链接进行自由组合

1. 使用`pdfminer`解析出引用所在的矩形位置和文本，但超链接只有矩形位置和文本，没有实际链接

2. 使用`pypdf2`解析出超链接的矩形位置和实际链接

3. 将两者的输出，基于简单的双指针+嵌套比对算法合并

4. 将合并后的json数据结构`RefItem`，输出成markdown