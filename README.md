# Python vs Go: Syntax and Control Structures

While I am brushing up Go programming language from a Pythonista perspective, I am relearning everything from zero. I documented the cheatsheet here as a side by side comparison, 
focusing on variables, control structures, functions, collections, and more.


## Hello World

#### Python
```python
print("Hello, World!")
```

#### Go
```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```

## Variables and Data Types
In Python, you declare variables and their types dynamically:
#### Python
```python
x = 10
y = 3.14
name = "Budi"
is_valid = True
```

#### Go
```go
package main

import "fmt"

func main() {
    var x int = 10
    var y float64 = 3.14
    name := "Budi"
    isValid := true
    fmt.Println(x, y, name, isValid)
}

```

## If-Else Statement
#### Python
```python
x = 10
if x > 5:
    print("x is greater than 5")
else:
    print("x is 5 or less")
```

#### Go
```go
x := 10
if x > 5 {
    fmt.Println("x is greater than 5")
} else {
    fmt.Println("x is 5 or less")
}
```

## For Loop
#### Python
```python
for i in range(5):
    print(i)
```
#### Go
```go
for i := 0; i < 5; i++ {
    fmt.Println(i)
}
```

## While Loop
#### Python
```python
i = 0
while i < 5:
    print(i)
    i += 1

```
#### Go
```go
i := 0
for i < 5 {
    fmt.Println(i)
    i++
}
```


## Switch/Case Statement
#### Python
```python
day = 'My day'
match day:
    case "Saturday" | "Sunday":
        print(f"{day} is a weekend.")
    case "Monday" | "Tuesday" | "Wednesday" | "Thursday" | "Friday":
        print(f"{day} is a weekday.")
    case _:
        print("That's not a valid day of the week.")
```
#### Go
```go
 day := "my day"

switch day {
    case "Saturday", "Sunday":
        fmt.Printf("%s is a weekend.\n", day)
    case "Monday", "Tuesday", "Wednesday", "Thursday", "Friday":
        fmt.Printf("%s is a weekday.\n", day)
    default:
        fmt.Println("That's not a valid day of the week.")
}
```


## Functions
#### Python
```python
def add(x, y):
    return x + y

result = add(3, 4)
print(result)

```

#### Go
```go
package main

import "fmt"

func add(x int, y int) int {
    return x + y
}

func main() {
    result := add(3, 4)
    fmt.Println(result)
}

```


## Lists/Slices
#### Python
```python
numbers = [1, 2, 3, 4, 5]
numbers.append(6)

```

#### Go
```go
numbers := []int{1, 2, 3, 4, 5}
numbers = append(numbers, 6)
fmt.Println(numbers)
```


## Dictionaries/Maps
#### Python
```python
ages = {"Budi": 39, "Ahmar": 28}
ages["Ahmar"] = 35
```

#### Go
```go
package main

import "fmt"

func main() {
    ages := map[string]int{"Budi": 30, "Ahmar": 25}
    ages["Budi"] = 35
    fmt.Println(ages)
}
```


## Classes/Structs

#### Python
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hello, {self.name}"

person = Person("Budi", 30)
print(person.greet())

```
#### Go
```go
package main

import "fmt"

type Person struct {
    Name string
    Age  int
}

func (p Person) Greet() string {
    return "Hello, " + p.Name
}

func main() {
    person := Person{Name: "Alice", Age: 30}
    fmt.Println(person.Greet())
}
```


## Error Handling
#### Python
```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

#### Go
```go
package main

import (
    "errors"
    "fmt"
)

func divide(a, b float64) (float64, error) {
    if b == 0 {
        return 0, errors.New("cannot divide by zero")
    }
    return a / b, nil
}
```

Enjoy and Happy Learning!