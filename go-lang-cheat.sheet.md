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
Types:
	bool byte complex64 complex128 error float32 float64
	int int8 int16 int32 int64 rune string
	uint uint8 uint16 uint32 uint64 uintptr

Constants:
	true false iota

Zero value:
	nil

Functions:
	append cap close complex copy delete imag len
	make new panic print println real recover
```

#### Composite Types
```
array, struct, pointer, function, interface, slice, map, and channel
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

#### Arrays & Slices
```
var w [5]float64
x := [3]int{1,2,3}
y := [...]int{4,5}
z := make([]float64, 5, 10)
```

#### Starting GoDoc HTTP Server
```
godoc -http=:6060
```
