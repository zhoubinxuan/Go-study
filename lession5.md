# Go语言入门第三天（一）

1. if...else if...else语句

```
package main
import "fmt"

func main() {
	var i int = 102;
	if i <= 100 {
		fmt.Println("第一位");
	} else if i > 100 && i <= 101 {
		fmt.Println("第二位")
	} else {
		fmt.Println("第三位")
	}
}
```

2. switch....case....default 语句

```
package main
import "fmt"

func main() {
    i := 1001
    
    switch i { 
        case 1001:
            fmt.Println("第一位")
        case 1002：
            fmt.Println("第二位")
        default:
            fmt.Println("第三位")
    }
    
    switch {
        case i == 1001:
            fmt.Println("第四位")
        case i == 1002：
            fmt.Println("第五位")
        default
            fmt.Println("第六位")
    }
    
    var x interface()
    
    switch z := x.(type) {
        case nil:
            fmt.Println("nil类型")
        case int:
            fmt.Println("int类型")
        default:
            fmt.Println("未知")
    }
	
	var c1, c2, c3 chan int
	var i1, i2 int
	select {
		case i1 = <-c1:
			fmt.Printf("recevied ", i1, " from c1\n")
		case c2 <- i2:
			fmt.Printf("sent ", i2, " to c2\n")
		case i3, ok := (<-c3):
			if ok {
				fmt.Printf("recevied ", i3, " from c3\n")
			} else {
				fmt.Printf("c3 is closed\n")
			}
		default:
			fmt.Printf("no communication\n")
	}
}
```
