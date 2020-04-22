## GDB基本命令

b 设置断点

r 执行程序到下一个断点

disas 查看汇编代码

stepi si 执行一次汇编代码

info register

x /s 查看寄存器中的值



### GDB的指令

| 命令                          | 功能                                          |
| ----------------------------- | --------------------------------------------- |
| quit                          | 退出                                          |
| run                           | 开始程序                                      |
| kill                          | 停止程序                                      |
| break                         | 断点                                          |
| break functionname            | 在functionname 处打断点                       |
| break *0x111111               | 在 0x111111 处打断点                          |
| delete 1                      | 删除 1号断点                                  |
| delete                        | 删除所有断点                                  |
| stepi                         | 单步调试（汇编级）                            |
| stepi 4                       | 单步调试4次                                   |
| nexti                         | 程序级别下一条指令                            |
| continue                      | 继续执行                                      |
| finish                        | 运行直到程序返回                              |
| disas                         | 反汇编当前函数                                |
| disas functionname            | 反汇编functionname函数                        |
| disas 0x11111111              | 反汇编0x11111111的函数                        |
| disas 0x11111111， 0x22222222 | 反汇编两个地址范围的函数                      |
| print /x $rip                 | 十六进制打印程序计数器                        |
| print $rax                    | 打印$rax寄存器的内容                          |
| print /x $rax                 | 十六进制打印$rax的内容                        |
| print /t $rax                 | 二进制形式打印 $rax 的内容                    |
| print 0x100                   | 打印0x100的十进制                             |
| print /x 555                  | 16进制打印 555                                |
| print /x ($rsp+8)             | 十六进制打印 $rsp+8 地址的内容                |
| print *(long *) 0x11111111    | long 整型形式打印 0x11111111 地址的内容       |
| print *(long *) ($rsp + 8)    | long 整形形式打印 $rsp +8 地址的内容          |
| x/2g 0x11111111               | 输出从 0x11111111地址 开始 2 word 长度的内容  |
| x/20b functioname             | 输出从 functionname 地址开始的 20 byte 的内容 |
| info frame                    | 当前栈帧的信息                                |
| info registers                | 当前寄存器信息                                |
| help                          | 帮助                                          |



寄存器参数存放顺序：rsi,rdi,rdx,rcx,r8,r9