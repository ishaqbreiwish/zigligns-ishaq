## Ishaq Notes

### Exercise 1 - hello

- zig functions are private by default, but main must be public

### Exercise 2 - std

- we import using @import
- we should store the import in a const variable

### Exercise 3 - assignment

```zig
const foo: u8 = 20;
```

- 'const': constant, can't be changed
- 'u': unsigned, can't be negative
- '8': 8-bits

### Exercise 4 - Arrays

- The most verbose way to declare an array is

```zig
var foo: [3]u32 = [3]u32{ 42, 108, 5423 };
```

- instead, we can allow zig to infer both type and size

```zig
var foo: [_]u32{42, 108, 5423};
```

- we can get values using index notation

```zig
const bar = foo[2];
```

- we can get length using len

```zig
const length = foo.len;
```

### Exercise 5 - Arrays 2

- zig only has one array operator
- you can use ++ to concatenate two arrays

```zig
    const a = [_]u8{ 1,2 };
    const b = [_]u8{ 3,4 };
    const c = a ++ b ++ [_]u8{ 5 }; // equals 1 2 3 4 5
```

- note: zig only operates on your array when your code is being compiled (comptime)

### Exercise 6 - Strings

- zig stores strings as an array of bytes
- much like c, single chars are wrapped with `''` and quotes are wrapped with `""`

### Exercise 7 - Strings 2

- you can do multi line strings by putting "\\" at the beginning of each line

```zig
const two_lines =
         \\Line One
         \\Line Two
     ;
```

### Exercise 9 - if

- basically normal lol
- most special thing is that it **only** accepts boolean values
- It won't coerce numbers or other types of data to true and false

### Exercise 10 - if2

- if statements can be valid statements

```zig
 const foo: u8 = if (a) 2 else 3;
```

### Exercise 11-14 - While

- Again, nothing super special here, but condition does need to be a boolean like w/ if
- while loops do have some interesitng additions, like a `continue` expression, which runs every time th eloop continues (either at the en of the loop or when an explicit `continue` is invoked)

```zig
 var foo = 2;
while (foo < 10) : (foo += 2) {
    // blah blah
}
```
