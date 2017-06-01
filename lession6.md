# Go语言入门第四天（一）

### 循环语句

```
//语句格式
for init; condition; post {}
for condition {}
for {}
for key, value := range oldMap {
    newMap[key] = value
}
```



```
/**
    例子
*/
package main

import "fmt"

func main() {
    var b int = 15
    var a int
    
    var numbers [6]int{1, 3, 5, 7}
    
    for a:=0; a <= 10; a++ {
        if a == 5 {
            continue;
        }
        
        fmt.Printf("a的值为：%d\n", a)
    }
    
    for a < b {
        if a == 5 {
            break;
        }
        fmt.Printf("a的值为：%d\n", a)
        a ++
    }
    
    for i, x := range numbers {
        if i == 3 {
            goto endPoint
        }
        fmt.Printf("第 %d 位值为 %d\n", i, x)
    }
    
    endPoint:
    print("end")
}

```



