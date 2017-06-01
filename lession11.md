# Go入门语言第五天（一）

### 切片（slice）


```
定义格式
var idenitifier [] type
var idenitifier [] type = make([]type, len, cap)
idenitifier := make([type], len, cap)
```


```
package main

import (
    "fmt"
    "reflect"
)

func main() {
    var numbers1 = [10]int{1, 2, 3, 4, 5, 6, 7, 8}
    var numbers2 = numbers1[:5]
    fmt.Println(reflect.TypeOf(numbers2))
    numbers2[1] = 10
    print(numbers2[1])
    print(numbers1[1])
    
    numbers2 = append(numbers2, 100, 1000)
    print(numbers1[5])
    print(numbers1[6])
    
    var numbers = make([]int, 4, 6)
    numbers = append(numbers, 1, 2)
    printScanf(numbers)
    
    copy(numbers, numbers2)
    printScanf(numbers)
}

func printScanf(arr []int) {
    fmt.Printf("%d, %d, %v\n", len(arr), cap(arr), arr)
}
```

