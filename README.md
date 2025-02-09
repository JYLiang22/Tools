# Tools

# gitpush v2.0

计划升级gitpush v1.0，因为这个脚本确实鸡肋！<br>

思路：

1. git status 获取所有更改的文件，并可以用下标获取更改的文件，例如0代表readme、1代表fig/、2代表drawio/
2. 询问是否需要git add，否则退出，需要则输入上述下标索引
3. git add 索引对应的文件
4. 是否需要继续git add，还是需要把已经git add的文件放回工作区，因为第二步输入的索引可能有误
5. 执行git commit -m ""，备注由输入的信息获取
6. 是否git push，因为第五步的m可能输错
7. 输出当前git status，并询问是否需要继续操作，如果需要则循环这个步骤