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
