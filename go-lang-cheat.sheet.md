# Go language cheat sheet

#### Links
- [The Spec](http://golang.org/ref/spec)
- [Effective Go](http://golang.org/doc/effective_go.html)
- [Packages](http://golang.org/pkg/)

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

#### Data Structures
```
Primitive Types
  bool byte complex64 complex128 error float32 float64
  int int8 int16 int32 int64 rune string
  uint uint8 uint16 uint32 uint64 uintptr
Composite Types
  array slice map struct pointer function interface channel
Initialization Literal
  a := 3                    # integer
  b := 3.14                 # float64
  c := `hello` + "world"    # string
  d := [2]int{5, 6}         # array
  e := [...]string{"a"}     # array for unknown list size
  f := []int{}              # slice creates new array
  g := list[2:5]            # slice from exiting array
  h := map[string]int{}     # map
  i := Point{}              # struct
Initialization Make
  a := make([]float64, 5, 10)    # creates slice float64, len 5, capacity 10
  b := make(map[bool]byte, 100)  # creates map with 100 capacity
```

#### Starting GoDoc HTTP Server
```
godoc -http=:6060
```
