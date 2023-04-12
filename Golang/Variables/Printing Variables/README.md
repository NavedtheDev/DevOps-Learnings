## Printing a string ##

```
package main
import "fmt"

func main(){
    fmt.Print("Hey Everyone")
}

Output,
Hey Everyone
```

## Printing a variable ## 

```
package main
import "fmt"

func main(){
    var sport string = "Cricket"
    fmt.Println(sport)
}

Output,
Cricket
```

## Printing string and variable together ##

```
package main
import "fmt"

func main(){
    var sport string = "Cricket"
    var player string = "Alex"
    fmt.Println(player, "is playing", sport)
}

Output is, 
Alex is playing Cricket
```
