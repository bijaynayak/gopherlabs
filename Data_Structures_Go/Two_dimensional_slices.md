# Two-dimensional slices

Two-dimensional slices are descriptors of a two-dimensional array.
A two-dimensional slice is a contiguous section of an array that is stored away from the slice itself. 
It holds references to an underlying array. A two-dimensional slice will be an array of arrays, 
while the capacity of a slice can be increased by creating a new slice and copying the contents of the initial 
slice into the new one. This is also referred to as a slice of slices. The following is an example of a two-dimensional array.
A 2D array is created and the array elements are initialized with values.

```

package main
// importing fmt package
import (
"fmt"
)
// main method
func main() {
var TwoDArray [8][8]int
TwoDArray[3][6] = 18
TwoDArray[7][4] = 3
fmt.Println(TwoDArray)
}


```
output :-
```
 sangam$ go run 2darray.go
[[0 0 0 0 0 0 0 0] [0 0 0 0 0 0 0 0] [0 0 0 0 0 0 0 0] [0 0 0 0 0 0 18 0] 
[0 0 0 0 0 0 0 0] [0 0 0 0 0 0 0 0] [0 0 0 0 0 0 0 0] [0 0 0 0 3 0 0 0]]
```

For dynamic allocation, we use slice of slices. 
In the following code, slice of slices is explained as two-dimensional slices— twodslices.go:
```
sangam$ cat twodslices.go

package main

// importing fmt package
import (
	"fmt"
)

// main method
func main() {

	var rows int
	var cols int

	rows = 7
	cols = 9
	var twodslices = make([][]int, rows)

	var i int

	for i = range twodslices {

		twodslices[i] = make([]int, cols)
	}

	fmt.Println(twodslices)
}

```
output :
```
sangam:Chapter02 sangam$ go run twodslices.go
[[0 0 0 0 0 0 0 0 0] [0 0 0 0 0 0 0 0 0] [0 0 0 0 0 0 0 0 0] [0 0 0 0 0 0 0 0 0] [0 0 0 0 0 0 0 0 0] [0 0 0 0 0 0 0 0 0] [0 0 0 0 0 0 0 0 0]]


```
