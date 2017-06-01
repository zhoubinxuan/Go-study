# Go入门第四天（三）

### 数组


```
//格式
var variable_name [SIZE] variable_type
```


```
package main

func main() {
    var a1 = [10]int{1, 2, 3, 4, 5, 6}
    var a2 = []int{1, 2, 3, 4, 5}
    
    for i, x := range a1 {
        println(i, x)
    }
    
    println(a2[3])

    var avg float32
    avg = getAverage(a2, len(a2))
    println(avg, a2[3])
    
}

func getAverage(arr []int, size int) {
    var sum, i int
    var avg float32
    
    for i = 0; i < size; i ++ {
        sum += arr[i]
    }
    
    arr[3] = 100
    
    avg = float32(sum / size)
    return avg
}
```





