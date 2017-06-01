# Go语言入门第五天（二）

### 集合


```
定义格式
var map_variable map[key_data_type]value_data_type
map_variable = make(map[key_data_type]value_data_type)
```


```
package main

func main() {
    var countryMap map[string]string
    countryMap = map[string]string
    
    countryMap["France"] = "Pairs"
    countryMap["China"] = "Beijing"
    
    for country, city := range countryMap {
        println(country, city)
    }
    
    delete(countryMap, "France")
    for country, city := range countryMap {
        println(country, city)
    }
}
```

