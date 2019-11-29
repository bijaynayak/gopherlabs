# Accessing program arguments

The most simple way to parameterize the program run is to use the command-line arguments as program parameters. 

Simply, the parameterized program call could look like this: ./parsecsv user.csv role.csv. In this case, parsecsv is the name of the executed binary and user.csv and role.csv are the arguments, that modify the program call (in this case it refers to files to be parsed).

- How to do it...

Create the main.go file with the following content:
```
package main

import (
	"fmt"
	"os"
)

func main() {

	args := os.Args

	// This call will print
	// all command line arguments.
	fmt.Println(args)

	// The first argument, zero item from slice,
	// is the name of the called binary.
	programName := args[0]
	fmt.Printf("The binary name is: %s \n", programName)

	// The rest of the arguments could be obtained
	// by omitting the first argument.
	otherArgs := args[1:]
	fmt.Println(otherArgs)

	for idx, arg := range otherArgs {
		fmt.Printf("Arg %d = %s \n", idx, arg)
	}
}


```

output 

```
Biradars-MacBook-Air-4:golang-daily sangam$ go build -o test
Biradars-MacBook-Air-4:golang-daily sangam$ ./test arg1 arg2
[./test arg1 arg2]
The binary name is: ./test 
[arg1 arg2]
Arg 0 = arg1 
Arg 1 = arg2 
Biradars-MacBook-Air-4:golang-daily sangam$ 

```
