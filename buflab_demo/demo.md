# Make yourself a cookie
```
./buflab-handout/makecookie 2018012345
```

# Convert hex hack code into binary
```
./buflab-handout/hex2raw < fake_bomb.txt > fake_bomb.raw
```

# Test the power of your bomb

```
./buflab-handout/bufbomb -u 2018012345 < fake_bomb.raw
```

# Usage of GDB
You can always use abbreviations for efficiency when free of ambiguity. For example, use `b` for `break` (set a breakpoint), `bt` for `backtrace` (show call stack) and `ni` for `nexti` (execute next instruction).

## Attach debugger to process
```
gdb ./buflab-handout/bufbomb
```

## Set breakpoint
```
b main
b fizz
set disassemble-next-line on
```

## Run program from stdin with arguments
```
run -u 2018012345 < real_bomb.raw
```

## Show assembly around the breakpoint
```
disassemble
```

## Execute next instruction
```
stepi
nexti
continue
```

## Display registers, values in memory, and call stack
```
info reg
print $esp
print (unsigned)0x804a5cb
backtrace
```

## Stop debugging
```
quit
```