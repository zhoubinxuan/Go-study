# Go学习第一天（二）

- 关键词或保留字

break | default | func | interface | select
---|---|---|---|---
case | defer | go | map | struct
chan | else | goto | package | switch
const | fallthrough | if | range | type
continue | for | inport | return | var

- 预定义标识符

append | bool | byte | cap | close | complex
---|---|---|---|---|---
complex64 | complex128 | unit16 | copy | false | float32
float64 | imag | int | int8 | int16 | uint32
int32 | int64 | iota | len | make | new
nil | panic | uint64 | print | println | real
recover | string | true | uint | unit8 | unitptr

- 标识符访问权限
1. 当标识符以一个大写字母开头，那么使用这种形式的标识符的对象可以被外部包的代码所使用，类似于public
2. 当标识符以一个小写字母开头，则仅对包内部可见并可用,类似于protected


-数据类型
1. 布尔型
2. 数字类型 位的运算采用补码
3. 字符类型 字符串的字节使用UTF-8编码表示Unicode文本
4. 派生类型
    1. 指针类型
    2. 数组类型
    3. 结构化类型
    4. Channel类型
    5. 函数类型
    6. 切片类型
    7. 接口类型
    8. Map类型
