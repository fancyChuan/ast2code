# ast2code
解析python抽象语法树并还原为python代码


使用示例：
```
import ast
import ast2code

txt = "x = 6 * 5"
rootNode = ast.parse(txt)

code = ast2code.to_source(rootNode)

exec(code, globals(), locals()) # 执行该代码

print locals()["x"]  # 此时x变量已经在命名空间中了
```
