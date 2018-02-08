# vi命令示例大全
## 进入vi     
* vi filename   
  > 打开或新建文件，并将光标置于第一行首    
* vi +n filename    
  > 打开文件，并将光标置于第n行首     
* vi + filename
  > 打开文件，并将光标置于最后一行首
* vi +/pattern filename
  > 打开文件，并将光标置于第一个与pattern匹配的串处
* vi -r filename
  > 在上次正用vi编辑时发生系统崩溃，恢复filename
* vi filename....filename
  > 打开多个文件，依次进行编辑
## 保存退出
* w
  > 保存当前文件
* w /tmp1
  > 另存为/tmp1 
* 20,59w /tmp1
  > 仅将20-59行之间的内存另存为/tmp1
* x 或 wq
  > 保存退出
* q
  > 退出vi
* q!
  > 退出不保存
* !command
  > 执行shell命令command
* n1,n2 w !command
  > 将文件中n1行至n2行的内容作为command的输入并执行之，若不指定n1，n2，则表示将整个文件内容作为command的输入
* r !command
  > 将命令command的输出结果放到当前行
* w !sudo tee %
  > 保存没权限时，可获取权限再保存
## 光标移动
* h
  > 光标左移一个字符
* l
  > 光标右移一个字符
* space
  > 光标右移一个字符 
* Backspace
  > 光标左移一个字符
* k 或 Ctrl+p
  > 光标上移一行
* j 或 Ctrl+n
  > 光标下移一行
* Enter
  > 光标下移一行
* w 或 W
  > 光标右移一个字至字首
* b 或 B
  > 光标左移一个字至字首
* e 或 E
  > 光标右移一个字至字尾
