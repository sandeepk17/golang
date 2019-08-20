
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


**_Help_** 
```
godoc fmt Println
```
**_constants_**: variable whose value cannot be changed once assigned.

```
package main
import ("fmt")

func main() {
	const b =10
	fmt.Println(b)
    // Throws Error when it is again assigned to the variable.
	b = 30
	fmt.Println(b)
}
```

**_Loops_**

- Loops
    - **_For Loop_**
Loops are used to execute a block of statements repeatedly based on a condition. 
Most of the programming languages provide 3 types of loops - _for, while, do while_. But **Go supports only for loop**.
- _syntax_

```
for initialisation_expression; evaluation_expression; iteration_expression{
   // one or more statement
}
```
Initialisation expression is execcuted first(and only once)
Then, evaluation_expression is executed and if thats is True then the code is executed.

iteration_expression is executed and the evaluation_expression is evaluated again and if its true the statement block gets executed again . this will continue until the evaluation_expression is false.

```
package main
import "fmt"

func main() {  
var i int
for i = 1; i <= 5; i++ {
fmt.Println(i)
    }
}
```
    - **_If else_**
- _syntax_

```
if condition{
// statements1
}else{
// statements2
}
```
condition is evaluated and if true statement1 is executed else statement2 will be executed.
- **can also use _if statements without else also_ & _chained if else statements_**

- **If example** : if the value is greater than 10 the statement inside block condition will not be executed.
```
package main
import "fmt"

func main() {  
    var x = 50
    if x < 10 {
        //Executes if x < 10
        fmt.Println("x is less than 10")
    } 
}
```
- **If-Else Example**: if block is false the the else block gets executed.
```
package main
import "fmt"

func main() {  
    var x = 50
    if x < 10 {
        //Executes if x is less than 10
        fmt.Println("x is less than 10")
    } else {
        //Executes if x >= 10
        fmt.Println("x is greater than or equals 10")
    }
}

```