# Go语言学习第二天（一）
- 语言常量
    1. 常量的定义格式

        ```
        const identifier [type] = value
        ```
    2. 多个常量定义
        
        ```
        const c_name1, c_name2 = value1, value2
        ```
    3. 枚举定义常量
        const (
            Unknown = 0
            Female = 1
            Male = 2
        )
        
    4. 常量表达式可以使用函数 不过函数必须是内置函数（不建议使用）
    5. iota 特殊常量 可以认为是一个可以被编译器修改的常量 在枚举定义常量中使用才有效果
    6. 示例代码
        
        ```
        package main
        
        import "fmt"
        import "unsafe"
        
        const (
            x = 3
            y = len(x)
            z = unsafe.Sizeof(x)
        )
        
        const (
            e = iota
            f
            g
            h = 100
            i
            j = iota
            k
        )
        
        const (
            c1 = 2 * iota
            c2
            c3
            c4
        )
        
        func main () {
            const LENGTH = 10
            const WIDTH = 5
            var area int
            const a, b, c = 1, false, "str"
            
            
            fmt.Printf("面积为：%d", $area)
            println();
            println(a, b, c)
            println(x, y, z)
            println(e, f, g, h, i, j, k)
            println(c1, c2, c3, c4)
        }
        ```
    
