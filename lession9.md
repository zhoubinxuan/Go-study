# Go入门第四天（四）

### 指针

```
定义格式
var var_name *var-type
```



```
package main

import "fmt"

func main() {
    var ptr *int
    var a = 10;
    
    ptr = &a
    println(ptr)
    fmt.Println(*ptr)
    
    var b = 20
    swap(&a, &b)
    println(a, b)
    
    var ptrArr [3] *int
    var arr = [3]int
    
    for i := 0; i < 3; i++ {
        ptrArr[i] = &arr[i]
    }
    
    for i := 0; i < 3; i ++ {
        println(*ptrArr[i])
    }
    
}

func swap(a *int, b *int) {
    var tmp int
    tmp = *a
    *a = *b
    *b = tmp
}
```
