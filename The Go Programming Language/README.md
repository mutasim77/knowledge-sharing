<p align="center">
  <img alt="Go PNG" src="https://github.com/mutasim77/knowledge-sharing/assets/96326525/b58a68a9-afb0-495f-ab19-6acb446f3271"/>
</p>
<br/>

# Welcome to the Go Programming Language repository! 🚀

This repository is dedicated to everything Go - an open-source programming language designed for simplicity, efficiency, and ease of use. Whether you're a seasoned Go developer or just getting started, this repository aims to be a helpful resource.

# Table of Contents 📜
Explore various topics related to Go programming:

- [Introduction to GO 🐹](#introduction-to-go-)
- [Basics 💎](#basics-)
  - [Variables and Data Types 👀](#variables-and-data-types-)
  - [Control Structures ⛓️](#control-structures-)
  - [Arrays, Slices, Maps 📦](#arrays-slices-maps-)
  - [Functions 🛠️](#functions-)
- [OOP in Go 📦](#oop-in-go-)
  - [Struct 🏗️](#struct-)
  - [Interface 🔄](#interface-)
  - [Embedding and Composition 🧩🔄](#embedding-and-composition-)
  - [Inheritance ↗️](#inheritance-)
  - [Polymorphism 🔀](#polymorphism-)
  - [constructor 🛠️ 🌐](#constructor-)

  
## Introduction to GO 🐹
Go, created by Google in 2007 and open-sourced in 2009, is a relatively new programming language. It was developed to tackle challenges in modern infrastructure, where applications can benefit from multi-core processors and cloud servers. 📈

The motivation behind Go was to make it easier to write applications that can perform multiple tasks simultaneously, known as concurrency. In traditional programming, tasks are executed one after the other, but with improved infrastructure, applications can run tasks in parallel, making them faster and more user-friendly. 🚀

Consider using Google Drive or watching a video on YouTube – you can upload files, download content, and navigate the user interface concurrently. However, managing simultaneous tasks can lead to conflicts, like when multiple users edit a document simultaneously or try to book the last available ticket. 🚧
 
This is where Go shines. While many languages support concurrency, Go was designed to simplify the process. It provides features like goroutines to handle parallel tasks more easily. Its main use case is for building high-performance applications that run on modern, scalable infrastructure with hundreds or thousands of servers, often on cloud platforms. 💡

### Characteristics of Go and Go Use Cases 
Go aims to combine the simplicity of high-level languages like Python with the speed of lower-level languages such as C++. It is primarily used on the server side for applications ranging from microservices to web and database services. Many leading cloud technologies like Docker, HashiCorp Vault, Kubernetes, and CockroachDB are written in Go.🚀

Go's advantages include a straightforward syntax, rapid application development, fast startup times, and efficient resource usage. As a compiled language, Go produces a single binary, ensuring consistent deployment across platforms. Its portability makes it popular for writing automation tools and command-line interfaces for DevOps and SRE tasks. 💻🔧

Now that we understand why Go was created and what sets it apart from other languages, let's dive into learning its core concepts and syntax. 🌟

## Basics 💎
Let's not forget tradition and start by simply printing 'Hello, World!' 😁

### Hello World 🌍 
```go
// main.go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```
1. The `package main` line declares that this is the main package of the program.
2. `import "fmt"` includes the `"fmt"` package, which provides formatted `I/O` functions.

### Variables and Data Types 👀
Let's go through different examples for each type of variable declaration and initialization in Go:

#### Variable and constant declaration and initialization 🛠️
```go
// Declaration without Initialization
var counter int

// Declaration with Initialization
var temperature int = 72

// Declare and Initialize Multiple Variables at Once
var width, height int = 100, 50

// Type Omitted, Inferred Type
var message = "Hello, Go!"

// Shorthand Declaration (Only in Func Bodies)
count := 10

// Constant Declaration
const pi = 3.1416
```

#### Data Types 🧱

```go
// Integer Types
var integer int = 42 
var signedInt int8 = 127 // => 8-bit signed^ integer
var unsignedInt uint = 42 // => unsigned^ either 32 or 64 bit

// Floating-point Types
var floatValue float32 = 3.14
var doubleValue float64 = 3.14159265359

// String Type
var message string = "Hello, Go!"

// Boolean Type
var isTrue bool = true

// Complex Types
var complexValue complex64 = 1 + 2i // contain float32 as a real and imaginary component
var anotherComplex complex128 = 3 + 4i // contain float64 as a real and imaginary component
```

> An int is signed by default, meaning it can represent both positive and negative values. An unsigned is an integer that can never be negative.

### Control Structures ⛓
Learn how to control the flow of your code with conditionals, loops, switches and defers.

#### If statements ➡️❓
```go
package main

import "fmt"

func main() {
    // Basic one
    x := 15
    if x > 10 {
        fmt.Println("x is greater than 10")
    } else if x == 10 {
        fmt.Println("x is equal to 10")
    } else {
        fmt.Println("x is less than 10")
    }

    // You can put one statement before the condition
    b, c := 20, 15
    if a := b + c; a < 42 {
        fmt.Println("Sum is less than 42:", a)
    } else {
        fmt.Println("Sum is greater than or equal to 42:", a-42)
    }

}
```
#### Switch statement 🔀
```go
package main

import "fmt"

func main() {
	// Basic switch with different cases
	day := "Friday"
	switch day {
	case "Monday":
		fmt.Println("It's the start of the week")
	case "Friday":
		fmt.Println("TGIF!")
	default:
		fmt.Println("Just another day")
	}

	// Switch with comparison in cases
	number := 7
	switch {
	case number < 5:
		fmt.Println("Less than 5")
	case number >= 5 && number <= 10:
		fmt.Println("Between 5 and 10")
	default:
		fmt.Println("Greater than 10")
	}

	// Switch with cases presented in a comma-separated list
	grade := 'A'
	switch grade {
	case 'A', 'B':
		fmt.Println("Good grades")
	case 'C', 'D':
		fmt.Println("Passing grades")
	default:
		fmt.Println("Not a passing grade")
	}

	// Switch with cases presented in a comma-separated list
	char := '?'
	switch char {
	case ' ', '?', '&', '=', '#', '+', '%':
		fmt.Println("Special character")
	}

}
```

#### Loops 🔄
> Fun fact: Go has only one looping construct, and it's the `for` loop. There is no equivalent to constructs like `while` or `do-while` in Go.

```go
package main

import "fmt"

func main() {

    // Basic for loop
    for i := 1; i < 10; i++ {
        fmt.Print(i, " ")
    }
    fmt.Println()

    // For loop as while loop -> while(i < 10)
    i := 1
    for i < 10 {
        fmt.Print(i, " ")
        i++
    }
    fmt.Println()

    // Infinite loop with break --> while(true)
    for {
        fmt.Println("Infinite loop")
        break
    }

    // Using break & continue
    for i := 0; i < 2; i++ {
        for j := i + 1; j < 3; j++ {
            if i == 0 {
                continue
            }
            fmt.Print(j, " ")
            if j == 2 {
                break 
            }
        }
    }

}
```

#### Defer ⏭️
> the `defer` keyword is used to schedule the execution of certain statements until the surrounding function (`main` in this case) completes. The deferred statements are executed in reverse order, providing a convenient way to ensure that certain tasks, such as cleanup operations, are performed even if the function encounters an error or returns early.

```go
package main

import "fmt"

func main() {
    fmt.Println("Start of the program")

    // Using defer to schedule a function call to be executed later, usually for cleanup tasks
    defer fmt.Println("Deferred statement executed")

    fmt.Println("Middle of the program")

    // Multiple defer statements are executed in a LIFO order
    defer fmt.Println("Another deferred statement")

    fmt.Println("End of the program")
}

/*       Output:
  Start of the program
  Middle of the program
  End of the program
  Another deferred statement
  Deferred statement executed
*/
```

### Arrays, Slices, Maps 📦

#### Arrays 🗃️ 
```go
//-----Arrays------
var scores [10]int       // length of 10
scores[3] = 42           // set and update by index
playerScore := scores[3] // get by index

// Declare and initialize
highScores := [2]int{98, 87}            // equal to -> const x = [98, 87]; in js
shorthandScores := [...]int{91, 88, 95} // Compiler will define the length for us
```

#### Slices 🍕
```go
//-----Slices------
var grades []int                                             // Slices -> like dynamic-sized array
gradeList := []int{85, 92, 78, 94}                           // Initialize a slice with grade data
subjects := []string{0: "Math", 2: "English", 1: "Science"}  // Subjects in order
```

#### Operations on Arrays and Slices ⚒
```go
package main

import "fmt"

func main() {

	// Arrays & Slices operations
	quizScores := highScores[1:2]                  // Slice high scores for quizzes
	midtermScores := shorthandScores[:2]           // All Scores till 2 index (excluding 2)
	finalScores := shorthandScores[2:]             // All Scores after 2 index (including 2)
	grades = append(grades, 79, 88)                // Add new grades to the list
	combinedScores := append(grades, gradeList...) // Combine scores

	// Create a slice with make()
	byteSlice := make([]byte, 5, 5) // Make a byte slice with capacity 5

	// Convert array to slice
	planets := [3]string{"Earth", "Mars", "Venus"}
	nearbyPlanets := planets[:] // A slice referencing nearby planets

	// Print results
	fmt.Println("\nArrays Examples: ")
	fmt.Println("Player Scores:", scores, "Player 3 Score:", playerScore)
	fmt.Println("High Scores:", highScores)
	fmt.Println("Grades:", grades)
	fmt.Println("Quiz Scores:", quizScores)
	fmt.Println("Midterm Scores:", midtermScores)
	fmt.Println("Final Scores:", finalScores)
	fmt.Println("Combined Scores:", combinedScores)
	fmt.Println("Byte Slice:", byteSlice)
	fmt.Println("Nearby Planets:", nearbyPlanets)

	// Print Subjects using a loop
	fmt.Println("Subject: ")
	for i := 0; i < len(subjects); i++ {                // len(a) gives you the length of an array/a slice
		fmt.Printf("Subject %v: %v\n", i+1, subjects[i])
	}

	// Print using Range
	fmt.Println("High Scores:")
	for i, score := range highScores {
		fmt.Printf("Player %d: %d\n", i+1, score)
	}
}
```
#### Maps 🗺️
```go
package main

import "fmt"

func main() {
    // Example 1: Basic Map Operations
    m := make(map[string]int)   // Create a new map using `make()` with string keys and int values
    m["key"] = 42               // Assign a value to the key "key" --> set,update
    fmt.Println(m["key"])       // Retrieve and print the value associated with "key" --> get
 
    // Example 2: Check if a Key Exists and Delete
    delete(m, "key")                     // Delete the key "key" from the map --> delete
    element, exists := m["key"]         // Test if key "key" is present and retrieve its value, if so
    fmt.Println(element, exists)        // Print the value and a boolean indicating key presence -> [0, false] (cuz we delete key "key")

    // Example 3: Map Literal
    var cityPopulation = map[string]int{
        "New York":    8336817,
        "Los Angeles": 3979576,
        "Chicago":     2716000,
    }
    fmt.Println(cityPopulation) // map[Chicago:2716000 Los Angeles:3979576 New York:8336817]
 
    // Example 4: Iterate Over Map
    for city, population := range cityPopulation {
        fmt.Printf("%s has a population of %d\n", city, population) // New York has a population of 8336817 and etc...
    }
}
```

### Functions 🛠️
```
package main

import "fmt"

// Example 1: Simple Function
func greet() {
    fmt.Println("Hello, Gopher!")
}

// Example 2: Function with Parameters
func add(x, y int) {                    // x and y are the same type
    result := x + y
    fmt.Println("Sum:", result)
}

// Example 3: Return Type Declaration
func multiply(x, y int) int {         // int return type
    result := x * y
    return result
}

// Example 4: Can Return Multiple Values at Once
func divideAndRemainder(x, y int) (int, int) {
    quotient := x / y
    remainder := x % y
    return quotient, remainder
}

// Example 5: Return Multiple Named Results Simply by Return
func divide(x, y int) (quotient, remainder int) {
    quotient = x / y
    remainder = x % y
    return           // No explicit return values, using named return values
}

// Example 6: Functions As Values
func applyOperation(x, y int, operation func(int, int) int) int {
    result := operation(x, y)
    return result
}

// Example 7: Closures
func multiplyBy(factor int) func(int) int {
    return func(x int) int {
        return x * factor
    }
}

// Example 8: Variadic Functions
func sum(numbers ...int) int {       // // Variadic function that takes multiple integers
    total := 0
    for _, num := range numbers {
        total += num
    }
    return total
}


func main() {
    // Example 1
    greet()

    // Example 2
    add(5, 7)

    // Example 3
    product := multiply(3, 4)
    fmt.Println("Product:", product)

    // Example 4
    q, r := divideAndRemainder(10, 3)
    fmt.Printf("Quotient: %d, Remainder: %d\n", q, r)

    // Example 5
    q, r = divide(15, 4)
    fmt.Printf("Quotient: %d, Remainder: %d\n", q, r)

    // Example 6
    addition := func(a, b int) int {
        return a + b
    }
    result := applyOperation(3, 4, addition)
    fmt.Println("Result of addition:", result)

    // Example 7
    double := multiplyBy(2)
    triple := multiplyBy(3)
    fmt.Println("Double of 5:", double(5))
    fmt.Println("Triple of 5:", triple(5))

    // Example 8
    result = sum(1, 2, 3, 4, 5)
    fmt.Println("Sum:", result)
}
```

## OOP in Go 📦
**Go OOP Basics** involve using structs for data, interfaces for behavior, embedding for reuse, methods for type-specific functions, and encapsulation for clarity. Although Go lacks traditional inheritance, it achieves similar results through composition and initialization functions. These fundamentals help create modular and flexible code in Go.

### Struct 🏗
Structs allow you to define custom data types by grouping together variables of different types under a single name.
```go
// Define a struct 'Person' with fields and a method
type Person struct {
    FirstName string
    LastName  string
    Age       int
}
```

### Interface 🔄
Interfaces define a set of method signatures, and types implement these methods to satisfy the interface. They provide a way to achieve polymorphism in Go.

```go
// Define a simple interface 'Describer'
type Describer interface {
    Describe() string
}

// Implement the 'Describer' interface for the 'Person' struct
func (p Person) Describe() string {
    return fmt.Sprintf("%s %s, Age: %d", p.FirstName, p.LastName, p.Age)
}
```

### Embedding and Composition 🧩🔄
- **Embedding**: Embedding involves including one struct type as a field in another, promoting the embedded type's fields and methods.
- **Composition**: Combining multiple struct types to create a new type, achieving code reuse and flexibility.

```go
// Define another struct 'Address' with fields
type Address struct {
    City  string
    State string
}

// Define a struct 'Employee' embedding 'Person' and 'Address' structs
type Employee struct {
    Person // Embed 'Person' struct for composition
    Address // Embed 'Address' struct for composition
    JobTitle string
    salary uint // this one is `encapsulated field`
}

// Implement the 'Describer' interface for the 'Employee' struct
func (e Employee) Describe() string {
    return fmt.Sprintf("%s, %s, Job Title: %s", e.Person.Describe(), e.Address.City, e.JobTitle)
}
```

### Inheritance ↗
Go doesn't have `traditional inheritance`. Composition and embedding are used to achieve similar effects, allowing types to reuse and extend functionality.

> In our case it achieved through `composition and embedding`. `Employee` struct "inherits" characteristics from both `Person` and `Address`.

### Polymorphism 🔀
Polymorphism allows objects of different types to be treated as objects of a common type, enabling flexibility and code abstraction.
```
func (p Person) Describe() string {
    return fmt.Sprintf("%s %s, Age: %d", p.FirstName, p.LastName, p.Age)
}

func (e Employee) Describe() string {
    return fmt.Sprintf("%s, %s, Job Title: %s", e.Person.Describe(), e.Address.City, e.JobTitle)
```
> Implemented the `Describer` interface for both `Person` and `Employee` structs. In this example both of them are describing, but in different ways.

### Encapsulation 🌐
Encapsulation involves hiding the internal details of a type and exposing only what is necessary. In Go, fields and methods can be encapsulated within a `struct`.

```go
// Employee struct with encapsulated fields
type Employee struct {
    ... // other fields

    salary uint    // salary is `encapsulated field` -> cuz of starting with lowercase
}
```

**In GO** we use `lowercase initial letters` for encapsulation. However, it's crucial to understand that Go relies on package-level visibility rather than explicit access modifiers. Fields with `lowercase initials` are still accessible within the same package.

If you were to use the `Employee` struct in a different package, you wouldn't be able to access the `salary` directly. The idea is to encourage encapsulation by convention. However, we can achieve this by creating an `exported function` that functions as a `getter` and `setter`, returning the `salary`.

### Constructor 🛠
**In Go**: While Go lacks explicit constructors, it's common to use functions that return an instance of a struct, initializing it with desired values.
```go
// Define a function 'NewPerson' as a constructor for 'Person'
func NewPerson(firstName, lastName string, age int) Person {
    return Person{
        FirstName: firstName,
        LastName:  lastName,
        Age:       age,
    }
}
```
> Created a function `NewPerson` as a constructor for the `Person` struct.
