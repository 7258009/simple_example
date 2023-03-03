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
//vardeclares 1 or more variables
    var  a  =  "initial" 
    fmt . println ( a )
    
    
//You can declare multiple variables at once
    var  b ,  c  int  =  1 ,  2 
    fmt . println ( b ,  c )

//Go will determine the type from the initialized variable.
    var  d  =  true 
    fmt . println ( d )

//Variables declared without proper initialization are null . For example, a null value for intequals 0.
    var  e  int 
    fmt . println ( e )

//Go has a short statement :=for declaring and initializing a variable. For example, var f string = "apple"in shorthand it will turn into
    f  :=  "apple" 
    fmt . println ( f ) 
}
