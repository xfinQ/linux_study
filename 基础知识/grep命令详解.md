+ grep：文本搜索工具，根据用户指定的“模式”对目标文本逐行进行批评检查：打印匹配到的行
+ 模式：由正则表达式字符及文本字符所编写的过滤条件
#### 用法
+ ==**grep [options] PATTERN [file..]**==

|用法|含义|
|-|-|-|
|grep root /etc/passwd|针对指定字符进行搜索|
|grep "$USER"  /etc/passwd|针对变量进行搜索|
|grep '$USER' /etc/passwd| 针对字符进行搜索|
|grep `whoami` /etc/passwd| 可以调用别的命令输出的结果进行搜索|

#### grep选项

|选项|含义|
|-|-|-|
|--color=auto|对匹配到的文本着色显示|
|-v|显示不被pattern匹配到的行|
|-i|忽略字符大小写|
|-n|显示匹配到的行号|
|-c|统计匹配到的行号|
|-o|仅显示匹配到的字符串|
|-q|静默模式，不输出任何信息|
|-A #|after， 输出匹配到的后#行|
|-B #|before，输出匹配到的前#行|
|-C #|context，输出匹配到的前后#行|
|-e|实现多个选项间的逻辑关系or关系  grep -e 'cat' -e 'dog' file|
|-w |匹配整个单词，单词以空格分割|
|-E|egrep命令，支持扩展的正则表达式|
|-F|fgrep,不支持正则表达式|

