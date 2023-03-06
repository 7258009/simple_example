# simple_example
to stady Go with simple example
Plan:
1) The first program will print the classic “hello world”

add the code to the file hello-world.goand run go run

package main
import "fmt"
func main() {
    fmt.Println("hello world")
}

$ go run hello-world.go
hello world

$ go build hello-world.go
$ ls
hello-world    hello-world.go

$ ./hello-world
hello world

2) Data Types (Values)

package  main
import  "fmt"
func  main ()  {

    fmt . println ( "go"  +  "lang" )

    fmt . Println ( "1+1 =" ,  1 + 1 ) 
    fmt . println ( "7.0/3.0=" ,  7.0 / 3.0 )

    fmt . Println ( true  &&  false ) 
    fmt . Println ( true  ||  false ) 
    fmt . println (! true ) 
}

$ go run values.go
 golang 
1+1 = 2 
7.0/3.0 = 2.3333333333333335 
false 
true 
false

3) Variables

package  main
import  "fmt"
func  main ()  {

    var  a  =  "initial" 
    fmt . println ( a )
    
    var  b ,  c  int  =  1 ,  2 
    fmt . println ( b ,  c )

    var  d  =  true 
    fmt . println ( d )

    var  e  int 
    fmt . println ( e )

    f  :=  "apple" 
    fmt . println ( f ) 
}

$ go run variables.go
 initial 
1 2 
true 
0 
apple

4) Constants

package  main
import  ( 
    "fmt" 
    "math" 
)

const  s  string  =  "constant"

func  main ()  { 
    fmt . println ( s )

    const  n  =  500000000

    const  d  =  3e20  /  n 
    fmt . println ( d )

    fmt . println ( int64 ( d ))

    fmt . println ( math . sin ( n )) 
}

	
$ go run constant.go


5) "For"

package  main
import  "fmt"
func  main ()  {

func main() {

    i := 1
    for i <= 3 {
        fmt.Println(i)
        i = i + 1
    }

    for j := 7; j <= 9; j++ {
        fmt.Println(j)
    }

    for {
        fmt.Println("loop")
        break
    }

    for n := 0; n <= 5; n++ {
        if n%2 == 0 {
            continue
        }
        fmt.Println(n)
    }
}

$ go run for.go
1
2
3
7
8
9
loop
1
3
5


6) "If"

package  main
import  "fmt"
func  main ()  {

if  7 % 2  ==  0  { 
        fmt . Println ( "7 is even" ) 
    }  else  { 
        fmt . Println ( "7 is odd" ) 
    }

    if  8 % 4  ==  0  { 
        fmt . Println ( "8 is divisible by 4" ) 
    }

    if  num  :=  9 ;  num  <  0  { 
        fmt . Println ( num ,  "is negative" ) 
    }  else  if  num  <  10  { 
        fmt . Println ( num ,  "has 1 digit" ) 
    }  else  { 
        fmt . Println ( num ,  "has multiple digits" ) 
    } 
}

$ go run if -else.go 
 7 is odd 
8 is divisible by 4 
9 has 1 digit


7) "Switch"

package main
	
import (
    "fmt"
    "time"
)

func main() {
    i := 2
    fmt.Print("Write ", i, " as ")
    switch i {
    case 1:
        fmt.Println("one")
    case 2:
        fmt.Println("two")
    case 3:
        fmt.Println("three")
    }

     switch time.Now().Weekday() {
    case time.Saturday, time.Sunday:
        fmt.Println("It's the weekend")
    default:
        fmt.Println("It's a weekday")
    }

    t := time.Now()
    switch {
    case t.Hour() < 12:
        fmt.Println("It's before noon")
    default:
        fmt.Println("It's after noon")
    }

    whatAmI := func(i interface{}) {
        switch t := i.(type) {
        case bool:
            fmt.Println("I'm a bool")
        case int:
            fmt.Println("I'm an int")
        default:
            fmt.Printf("Don't know type %T\n", t)
        }
    }
    whatAmI(true)
    whatAmI(1)
    whatAmI("hey")
}

$ go run switch.go 
Write 2 as two
It's a weekday
It's after noon
I'm a bool
I'm an int
Don't know type string


8) "Arrays"

package main

import "fmt"

func main() {

var a [5]int
