
_run go programme:_

`go run <filename>`

_go structure_

```
package main
import ("fmt")

func main() {
	fmt.Println("Hello World! This is my first Go program\n")
}
```

**_Data Types_**
_three basic types_
- Numeric types: integers,floating points, complex values.
    - int8 - 8 bit signed integers.

    - int16 - 16 bit signed integers.

    - int32 - 32 bit signed integers.

    - int64 - 64 bit signed integers.

    - uint8 - 8 bit unsigned integers.

    - uint16 - 16 bit unsigned integers.

    - uint32 - 32 bit unsigned integers.

    - uint64 - 64 bit unsigned integers.

    - float32 - 32 bit floating point numbers.

    - float64 - 64 bit floating point numbers.

    - complex64 – has float32 real and imaginary parts.

    - complex128 - has float32 real and imaginary parts.

- String types: string concatenation, substring etc.
- Boolean types: 

**_Variables_**

`var <variable_name> <type>`

`var <variable_name> <type> = <value>`

`var <variable_name> = <value>`

_You can declare multiple variables with the syntax_

`var <variable_name1>, <variable_name2>  = <value1>, <value2>`

```
package main
import "fmt"

func main() {
    //declaring a integer variable x
    var x int
    x=3 //assigning x the value 3 
    fmt.Println("x:", x) //prints 3
    
    //declaring a integer variable y with value 20 in a single statement and prints it
    var y int=20
    fmt.Println("y:", y)
    
    //declaring a variable z with value 50 and prints it
    //Here type int is not explicitly mentioned 
    var z=50
    fmt.Println("z:", z)
    
    //Multiple variables are assigned in single line- i with an integer and j with a string
    var i, j = 100,"hello"
    fmt.Println("i and j:", i,j)
}

```

easy way of declaring the variables with value by omitting the var keyword using

You cannot use := just to assign a value to a variable which is already declared. := is used to declare and assign value.

```
<variable_name> := <value>
```
- Example
```
package main
import ("fmt")

func main() {
	a := 20
	fmt.Println(a)

	//gives error since a is already declared
	a := 30
	fmt.Println(a)
}
```


- **Help** 
`
godoc fmt Println
`
- **constants**: variable whose value cannot be changed once assigned.

`
package main
import ("fmt")

func main() {
	const b =10
	fmt.Println(b)
    // Throws Error when it is again assigned to the variable.
	b = 30
	fmt.Println(b)
}
`

- **Loops**

Loops
Loops are used to execute a block of statements repeatedly based on a condition. 
Most of the programming languages provide 3 types of loops - _for, while, do while_. But **Go supports only for loop**.
_syntax_

`
for initialisation_expression; evaluation_expression; iteration_expression{
   // one or more statement
}
`