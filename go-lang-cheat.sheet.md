# Go language cheat sheet

#### Links
- [The Spec](http://golang.org/ref/spec)
- [Effective Go](http://golang.org/doc/effective_go.html)
- [Packages](http://golang.org/pkg/)
- [The Source](https://go.googlesource.com/go/)

#### Reserved Words
```
break        default      func         interface    select
case         defer        go           map          struct
chan         else         goto         package      switch
const        fallthrough  if           range        type
continue     for          import       return       var
```

#### Operators
```
+    &     +=    &=     &&    ==    !=    (    )
-    |     -=    |=     ||    <     <=    [    ]
*    ^     *=    ^=     <-    >     >=    {    }
/    <<    /=    <<=    ++    =     :=    ,    ;
%    >>    %=    >>=    --    !     ...   .    :
     &^          &^=
```

#### Predeclared identifiers
```
Constants:
	true false iota

Zero value:
	nil

Functions:
	append cap close complex copy delete imag len
	make new panic print println real recover
```

#### Control Structures
```
if, switch, for # all have local memory initializers, no parens
```

#### Memory Allocation
```
new  - allocates zeroed storage memory and returns a pointer
make - creates slices, maps, and channels only. it returns an initialized (not zeroed) value
```

#### Primitive Types
```
bool byte complex64 complex128 error float32 float64
int int8 int16 int32 int64 rune string
uint uint8 uint16 uint32 uint64 uintptr
```

#### Composite Types
```
array slice map struct pointer function interface channel
```

#### Initialization
```
# creating an int with zero value
var a int
b := 0
c := new(int)

# creating an empty string
var a string
b := ""
c := new(string)

# creating an int array of zeros
var a [3]int
b := [3]int{0, 0, 0}
c := [...]int{0, 0, 0}
d := new([3]int)

# creating an empty slice of ints
var a []int
b := []int{}
c := new([]int)
d := make([]int, 0, 0)

# creating an empty map
a := map[string]int{}
b := make(map[string]int, 0)

# creating an point with x:0, y:0
var a point
b := point{}
c := new(point)

# using make, for slices, maps, and channels
a := make([]float64, 5, 10)    # creates slice float64, len 5, capacity 10
b := make(map[bool]byte, 100)  # creates map with 100 capacity
c := make(chan int, 10)        # creates buffered channel of integers

```

#### Methods
- Use pointer. No expensive array copy. No need for return value. Modify in place.
- Caller can be either pointer or value, go will convert type.
```
func (p *Point) Scale(x int, y string) float64 {}
```

#### Starting GoDoc HTTP Server
```
godoc -http=:6060
```

#### Get Max CPU Count
```
p := runtime.GOMAXPROCS(0)
```
