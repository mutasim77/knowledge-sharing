<p align="center">
  <img alt="Go PNG" src="https://github.com/mutasim77/knowledge-sharing/assets/96326525/b58a68a9-afb0-495f-ab19-6acb446f3271"/>
</p>
<br/>

# Go Programming Language 🐹

This repository is dedicated to everything Go - an open-source programming language designed for simplicity, efficiency, and ease of use. Whether you're a seasoned Go developer or just getting started, this repository aims to be a helpful resource. 🚀

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
  - [Constructor 🛠️ 🌐](#constructor-)
- [Web Development with Go 🌐](#web-development-with-go-)
  - [HTTP Server and Routing 🛣️](#http-server-and-routing-)
  - [Middleware and Authentication 🔑](#middleware-and-authentication-)
  - [Database Integration 📊](#database-integration-)
- [Authentication and Authorization in Go 🛡️](#authentication-and-authorization-in-go-)
  - [Understanding Authentication 🔒](#understanding-authentication-)
  - [Implementing Authentication in Go 🛠️](#implementing-authentication-in-go-)
  - [Understanding Authorization 🔑](#understanding-authorization-)
  - [Implementing Authorization in Go 🚪](#implementing-authorization-in-go-)
- [Pointers ⛓️](#pointers-)
  
## Introduction to GO 🐹
Go, created by Google in 2007 and open-sourced in 2009, is a relatively new programming language. It was developed to tackle challenges in modern infrastructure, where applications can benefit from multi-core processors and cloud servers. 📈

The motivation behind Go was to make it easier to write applications that can perform multiple tasks simultaneously, known as concurrency. In traditional programming, tasks are executed one after the other, but with improved infrastructure, applications can run tasks in parallel, making them faster and more user-friendly. 🚀

Consider using Google Drive or watching a video on YouTube – you can upload files, download content, and navigate the user interface concurrently. However, managing simultaneous tasks can lead to conflicts, like when multiple users edit a document simultaneously or try to book the last available ticket. 🚧
 
This is where Go shines. While many languages support concurrency, Go was designed to simplify the process. It provides features like goroutines to handle parallel tasks more easily. Its main use case is for building high-performance applications that run on modern, scalable infrastructure with hundreds or thousands of servers, often on cloud platforms. 💡

### Characteristics of Go and Go Use Cases 
Go aims to combine the simplicity of high-level languages like Python with the speed of lower-level languages such as C++. It is primarily used on the server side for applications ranging from microservices to web and database services. Many leading cloud technologies like Docker, HashiCorp Vault, Kubernetes, and CockroachDB are written in Go.🚀

Go's advantages include a straightforward syntax, rapid application development, fast startup times, and efficient resource usage. As a compiled language, Go produces a single binary, ensuring consistent deployment across platforms. Its portability makes it popular for writing automation tools and command-line interfaces for DevOps and SRE tasks. 💻🔧

Now that we understand why Go was created and what sets it apart from other languages, let's dive into learning its core concepts and syntax. 🌟

# Basics 💎
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
```go
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

# OOP in Go 📦
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
func (p Person) Describe() {
    fmt.Sprintf("%s %s, Age: %d", p.FirstName, p.LastName, p.Age)
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
func (e Employee) Describe() {
     fmt.Sprintf("%s, %s, Job Title: %s", e.Person.Describe(), e.Address.City, e.JobTitle)
}
```

### Inheritance ↗
Go doesn't have `traditional inheritance`. Composition and embedding are used to achieve similar effects, allowing types to reuse and extend functionality.

> In our case it achieved through `composition and embedding`. `Employee` struct "inherits" characteristics from both `Person` and `Address`.

### Polymorphism 🔀
Polymorphism allows objects of different types to be treated as objects of a common type, enabling flexibility and code abstraction.
```go
func (p Person) Describe() {
    fmt.Sprintf("%s %s, Age: %d", p.FirstName, p.LastName, p.Age)
}

func (e Employee) Describe() {
    fmt.Sprintf("%s, %s, Job Title: %s", e.Person.Describe(), e.Address.City, e.JobTitle)
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


# Web Development with Go 🌐
Web development with Go involves using the Go programming language to create web applications, APIs (Application Programming Interfaces), and services. Go provides a robust standard library for handling HTTP requests and responses, making it a popular choice for building scalable and efficient web applications.

One of the key features of Go for web development is its built-in HTTP server capabilities. With just a few lines of code, you can create a fully functional web server to handle incoming HTTP requests and serve responses. Go's simplicity and performance make it well-suited for handling high loads and concurrent requests.

In addition to its HTTP server capabilities, Go supports routing, middleware, authentication, and database integration, allowing developers to build full-fledged web applications with ease. Whether you're building a simple website, a RESTful API, or a complex web service, Go provides the tools and flexibility needed to get the job done efficiently.

## HTTP Server and Routing 🛣
An HTTP server is like a virtual receptionist for your web application. It listens for incoming requests from web browsers or other clients, processes those requests, and sends back appropriate responses.

```go
package main

import (
    "fmt"
    "net/http"
)

func handler(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "Hello, World!")
}

func main() {
    http.HandleFunc("/", handler)
    http.ListenAndServe(":8080", nil)
}
```
In this example:
- We define a handler function that takes an `http.ResponseWriter` and an `http.Request` as arguments. This function writes "Hello, World!" to the response.
- We use `http.HandleFunc` to associate the `handler` function with the root URL ("/").
- We start the HTTP server on port `8080` using `http.ListenAndServe`.

When you run this program and visit `http://localhost:8080` in your web browser, you'll see "Hello, World!" displayed on the page.

#### Routing Requests 🔗
Routing in Go allows you to direct incoming HTTP requests to different parts of your application based on the URL path. This is useful for organizing your code and handling different types of requests.
Here's an example of routing multiple URLs to different handler functions:

```go
func homeHandler(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "Welcome to the homepage!")
}

func aboutHandler(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "About Us")
}

func contactHandler(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "Contact Us")
}

func main() {
    http.HandleFunc("/", homeHandler)
    http.HandleFunc("/about", aboutHandler)
    http.HandleFunc("/contact", contactHandler)
    http.ListenAndServe(":8080", nil)
}
```

In this example:

- The `/` URL is routed to the `homeHandler` function, which displays a welcome message.
- The `/about` URL is routed to the `aboutHandler` function, which displays information about the company.
- The `/contact` URL is routed to the `contactHandler` function, which provides contact information.

When a user visits `http://localhost:8080/about`, for example, they'll see the "About Us" message.


## Middleware and Authentication 🔑
Middleware and authentication are crucial components in web development with Go. Middleware allows you to intercept and process incoming HTTP requests before they reach the final handler, while authentication ensures that only authorized users can access protected resources. Let's explore these concepts further.

### Middleware Basics 👻
Middleware acts as a bridge between the HTTP server and your application's handlers. It allows you to perform common tasks such as logging, authentication, authorization, and request preprocessing. Middleware functions are executed sequentially, with each function having the option to modify the request or response before passing them to the next middleware or handler.

Here's a simple example of a logging middleware in Go:
```go
func loggingMiddleware(next http.Handler) http.Handler {
    return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
        log.Println("Incoming request:", r.Method, r.URL.Path)
        next.ServeHTTP(w, r)
    })
}

func main() {
    // Use loggingMiddleware for all routes
    http.Handle("/", loggingMiddleware(http.HandlerFunc(handler)))
    http.ListenAndServe(":8080", nil)
}
```
In this example:

- We define a `loggingMiddleware` function that takes a `http.Handler` as input and returns a new http.Handler.
- Inside the middleware function, we log information about the incoming request, such as the HTTP method and URL path.
- We then call the `ServeHTTP` method on the next handler in the chain to pass the request along.

### Authentication 🛅
Authentication is the process of verifying the identity of users accessing your application. It ensures that only authenticated users can access certain parts of your application or perform specific actions. There are various authentication methods available, such as username/password, API keys, JSON Web Tokens (JWT), OAuth, and more.

Here's a basic example of implementing username/password authentication in Go:
```go
func authMiddleware(next http.Handler) http.Handler {
    return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
        username, password, ok := r.BasicAuth()
        if !ok || !checkCredentials(username, password) {
            http.Error(w, "Unauthorized", http.StatusUnauthorized)
            return
        }
        next.ServeHTTP(w, r)
    })
}

func checkCredentials(username, password string) bool {
    // Check if username and password are valid
    // This could involve querying a database or validating against a predefined list
    // For simplicity, we'll hardcode a username/password combination
    return username == "admin" && password == "password"
}

func main() {
    // Use authMiddleware for protected routes
    http.Handle("/admin", authMiddleware(http.HandlerFunc(adminHandler)))
    http.ListenAndServe(":8080", nil)
}
```
In this example:

- We define an `authMiddleware` function that checks the username and password sent in the request's Basic Authentication header.
- If the credentials are valid, the request is passed to the next handler. Otherwise, an `HTTP 401` Unauthorized response is returned.
- We use the `checkCredentials` function to verify the username and password against a predefined list (or a database).

> [!IMPORTANT]
> By leveraging middleware, you can modularize your application's logic and handle common tasks efficiently. Authentication ensures that your application's resources are protected and only accessible to authorized users. Understanding and implementing these concepts will help you build secure and scalable web applications in Go.

## Database Integration 📊
Go provides excellent support for interacting with various databases, including SQL databases like MySQL, PostgreSQL, SQLite, and NoSQL databases like MongoDB. Database integration typically involves the following steps:

1. Importing the appropriate database driver package.
2. Establishing a connection to the database.
3. Executing queries or commands to interact with the database.

Let's look at an example of integrating Go with a MySQL database:
```go
package main

import (
    "database/sql"
    "fmt"
    _ "github.com/go-sql-driver/mysql"
)

func main() {
    // Open a connection to the MySQL database
    db, err := sql.Open("mysql", "username:password@tcp(localhost:3306)/dbname")
    if err != nil {
        fmt.Println("Error connecting to database:", err)
        return
    }
    defer db.Close()

    // Perform database operations
    // Example: Querying all rows from a table
    rows, err := db.Query("SELECT * FROM users")
    if err != nil {
        fmt.Println("Error querying database:", err)
        return
    }
    defer rows.Close()

    // Process query results
    for rows.Next() {
        // Process each row
    }
}
```
Replace "username", "password", "localhost", "3306", and "dbname" with your MySQL credentials and database details.

In this example:
- We import the `database/sql` package for working with databases and the MySQL driver package (github.com/go-sql-driver/mysql).
- We open a connection to the MySQL database using `sql.Open`.
- We execute a query to select all rows from the users table and process the query results.

> [!TIP]
> By understanding how to connect and interact with databases using Go, you can build powerful and scalable web applications that persist and manipulate data effectively.

# Authentication and Authorization in Go 🛡
Authentication and authorization are fundamental concepts in web development, especially when it comes to securing applications and protecting user data. Let's dive into what authentication and authorization mean in the context of Go programming.

## Understanding Authentication 🔒
Authentication is a fundamental aspect of web development, ensuring that users are `who` they claim to be before granting access to protected resources. In the context of Go programming, understanding authentication involves grasping the mechanisms used to verify user identities. Let's explore this concept in detail:

1. Purpose of Authentication:
  - Authentication serves to confirm the identity of users or systems attempting to access an application or its resources.
  - It prevents unauthorized access to sensitive data and functionalities, thus enhancing security.

2. Authentication Methods:
  - **Username/Password Authentication:** Users provide a username and password, which are compared against stored credentials in a database.
  - **Token-based Authentication:** Clients obtain a token (e.g., JWT) after successful authentication and include it in subsequent requests for access.
  - **OAuth Authentication:** Users grant limited access to third-party applications without sharing their credentials directly.
  - **Biometric Authentication:** Users authenticate using unique biological traits like fingerprints, facial recognition, or iris scans.

3. Authentication Process:
  - When a user attempts to access a protected resource, they provide their credentials.
  - The application verifies these credentials against a known source, such as a database or an authentication service.
  - If the credentials match, the user is considered authenticated and granted access; otherwise, access is denied.

## Implementing Authentication in Go 🛠
Implementing authentication involves using various techniques and libraries to verify user identities. Let's explore three common methods of authentication in Go: Basic Authentication, JSON Web Tokens (JWT), and OAuth Integration.

### Basic Authentication 🐌
- Basic Authentication involves clients providing their credentials (username and password) with each request.
- In Go, Basic Authentication can be implemented using HTTP's built-in authentication mechanisms or custom middleware.
- Upon receiving a request, the server verifies the provided credentials against a stored source, such as a database.
  
```go
package main

import (
    "net/http"
    "strings"
)

func BasicAuth(next http.HandlerFunc) http.HandlerFunc {
    return func(w http.ResponseWriter, r *http.Request) {
        username, password, ok := r.BasicAuth()
        if !ok || !checkCredentials(username, password) {
            http.Error(w, "Unauthorized", http.StatusUnauthorized)
            return
        }
        next.ServeHTTP(w, r)
    }
}

func checkCredentials(username, password string) bool {
    // Check username and password against stored credentials
    return username == "admin" && password == "password"
}

func main() {
    http.HandleFunc("/", BasicAuth(func(w http.ResponseWriter, r *http.Request) {
        w.Write([]byte("Authenticated successfully"))
    }))

    http.ListenAndServe(":8080", nil)
}
```

### JSON Web Tokens (JWT) 🌚
- JSON Web Tokens (JWT) are compact, URL-safe tokens that contain user claims and are digitally signed for authentication and authorization.
- In Go, JWT can be generated upon successful authentication and included in subsequent requests for access.
- The server verifies the JWT's signature and claims to authenticate users and authorize their actions.

```go
package main

import (
    "github.com/gofiber/fiber/v2"
    "github.com/dgrijalva/jwt-go"
    "golang.org/x/crypto/bcrypt"
    "time"
    "strconv"
)

const SecretKey = "your-secret-key"

func Login(c *fiber.Ctx) error {
    var data map[string]string

    if err := c.BodyParser(&data); err != nil {
        return err
    }

    // TODO HERE: Check the sent data with the actual one from database and continue if the user exists;
	
    // Create JWT token
    token := jwt.New(jwt.SigningMethodHS256)
    claims := token.Claims.(jwt.MapClaims)
    claims["id"] = strconv.Itoa(user.Id)
    claims["exp"] = time.Now().Add(time.Hour * 24).Unix() // Expires in 24 hours

    // Sign token with secret key
    signedToken, err := token.SignedString([]byte(SecretKey))
    if err != nil {
        return c.Status(fiber.StatusInternalServerError).JSON(fiber.Map{
            "message": "Could not login",
        })
    }

    // Set JWT token as cookie
    c.Cookie(&fiber.Cookie{
        Name:     "jwt",
        Value:    signedToken,
        Expires:  time.Now().Add(24 * time.Hour),
        HTTPOnly: true,
    })

    return c.JSON(fiber.Map{
        "message": "Success",
    })
}

func main() {
    app := fiber.New()
    app.Post("/login", Login)

    app.Listen(":3000")
}
```

### OAuth Integration 👻
- OAuth is an open-standard authorization protocol that allows users to grant limited access to their resources without sharing their credentials.
- In Go, OAuth integration involves implementing OAuth flows (e.g., Authorization Code, Implicit, Client Credentials) to authenticate and authorize users with third-party services.
- OAuth libraries in Go, such as golang.org/x/oauth2, facilitate the integration of OAuth providers like Google, Facebook, and GitHub.

> [!IMPORTANT]
> - The code will be a bit lengthy; here, I will provide some resources and blogs to read about OAuth2
> - [OAuth 2.0 Implementation in Golang](https://dev.to/siddheshk02/oauth-20-implementation-in-golang-3mj1)
> - [Getting Started with OAuth2 in Go](https://medium.com/@pliutau/getting-started-with-oauth2-in-go-2c9fae55d187)
> - [Creating an OAuth2 Client in Golang](https://www.sohamkamani.com/golang/oauth/)

> Implementing authentication requires understanding and choosing the appropriate method for your application's security and usability needs. Whether it's Basic Authentication, JSON Web Tokens (JWT), or OAuth Integration, each method offers its advantages and trade-offs. By effectively implementing authentication mechanisms, developers can ensure the integrity and security of their apps.

## Understanding Authorization 🔑
Authorization is a critical aspect of web development, determining `what` actions a user is allowed to perform within an application after their identity has been authenticated. In simpler terms, it controls access to different functionalities or resources based on the user's permissions or roles. Let's explore the concept of authorization in more detail:

1. **Purpose of Authorization: 🔗**
  - Authorization ensures that users can only access the parts of an application or resources that they are allowed to.
  - It prevents unauthorized users from performing sensitive operations or accessing restricted data.

3. **Authorization Methods: 👀**
  - **Role-Based Access Control (RBAC):** Users are assigned roles, and access rights are granted based on these roles. For example, an "admin" role might have full access to all functionalities, while a "user" role might have limited access.
  - **Attribute-Based Access Control (ABAC):** Access rights are determined based on various attributes associated with the user, the resource, and the environment. This approach allows for more fine-grained access control.
  
4. **Authorization Process: 🧯**
  - Once a user's identity is authenticated, the application determines the user's permissions or roles.
  - Based on these permissions or roles, the application decides whether to grant or deny access to specific functionalities or resources.
  - If access is granted, the user can proceed with the requested operation; otherwise, access is denied, and an appropriate error message is returned.

## Implementing Authorization in Go 🚪
Authorization is ensuring that users have appropriate access to resources and functionalities based on their roles or permissions. Implementing authorization involves defining access control rules and enforcing them within the application. Let's see: 

### Role-Based Authorization 🥑
- **Define Roles and Permissions:** Identify different user roles and the corresponding permissions they have within the application. For example, "admin" users might have full access to all functionalities, while "user" users might have restricted access.
- **Authorize Requests:** Upon receiving a request, verify the user's role and permissions against the required access level for the requested resource or functionality.
- **Enforce Access Control:** Allow or deny access to the resource based on the user's role and permissions. Ensure that unauthorized users receive appropriate error messages or responses.

Example of Authorization using Middleware::
> Implement middleware functions that intercept incoming requests and check the user's role and permissions before allowing access to specific endpoints or functionalities.

```go
func AdminOnlyMiddleware(next http.HandlerFunc) http.HandlerFunc {
    return func(w http.ResponseWriter, r *http.Request) {
        // Check if user is authenticated and has "admin" role
        if isAuthenticated(r) && hasAdminRole(r) {
            next.ServeHTTP(w, r)
            return
        }
        http.Error(w, "Unauthorized", http.StatusUnauthorized)
    }
}

func isAuthenticated(r *http.Request) bool {
    // Check if user is authenticated based on session or token
    return true // Placeholder implementation
}

func hasAdminRole(r *http.Request) bool {
    // Check if user has "admin" role
    return true // Placeholder implementation
}
```

### Attribute-Based Authorization 🥐
- **Define Attributes:** Determine the attributes associated with users, resources, and the environment that influence access control decisions. These attributes could include user roles, resource types, ownership, or other contextual information.
- **Evaluate Policies:** Establish policies that govern access based on the attributes. For example, users with the "manager" role may only access resources owned by their department.
- **Apply Policies:** Evaluate the attributes of the user, the requested resource, and the environment against the defined policies to determine access rights.

> [!TIP]
> Implementing Authorization in Go involves defining access control rules based on user roles, permissions, and attributes, and enforcing them within the application using middleware or custom logic. By implementing robust authorization mechanisms, developers can ensure that users have appropriate access to resources and functionalities while maintaining the security and integrity of the application.


# Pointers ⛓
Pointers are a fundamental concept in Go and many other programming languages. They provide a way to directly access and manipulate memory addresses, which can lead to more efficient and powerful code. Understanding pointers is crucial for tasks such as optimizing performance, managing memory efficiently, and working with data structures.

### 1. What Are Pointers? 👻
 - Definition: A pointer is a variable that holds the memory address of another variable. Instead of storing a value directly, a pointer stores the location where the value is stored.
 - Syntax: In Go, the * operator is used to declare a pointer, and the & operator is used to get the address of a variable.
 ```go 
   var x int = 10
   var p *int = &x // p now holds the memory address of x
   ```
