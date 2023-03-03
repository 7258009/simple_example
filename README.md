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

