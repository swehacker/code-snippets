# Sed

## Sed command args
Flag | Description
-------|-------------
-i | Modify the file itself instead of the file stream
-r | Turn on extended regexp (gnu)
-E | Turn on extended regexp (Mac OS X, FreeBSD)
-e | Use multiple commands (use -e before each command)
-n | No printing
-f | Use script file

## Sed pattern flags
Flag | Description
-------|-------------
/g | Global replacement
/I | Ignore Case
/p | Print
/w | Write to file

## Sed commands
Flag | Description
-------|-------------
: | Label
# | Comment
{}| Block
= | Print line number
a | Append
b | Label
c | Change
d | Delete
g | Get (g and G)
h | Hold
n | Next (n and N)
i | Insert
I | Look
s | Substitut
p | Print (p and P)
q | Quit
t | Label
r | Read file
w | Write to file
x | Exchange
y | Transform

### Essential sed commands
Most people only learn the substitute command
#### Substitution

#### Delete

##### Delete everything after the pattern
```bash
sed '/PATTERN-1/,$d' <file>
```

##### Delete lines by its linenumber
Delete lines 2 to 4
```bash
sed '2,4d' <file>
```

##### Delete lines from a specific row
E.g row 11 - forward
```bash
sed '11,$ d' <file>
```

##### Delete lines between two patterns
Delete everething between two patterns including the rows where the pattern reciedes.
```bash
sed '/PATTERN1/,/PATTERN2/d' <file>
```

##### Delete all lines excluding between patterns
```bash
sed '/PATTERN-1/,/PATTERN-2/{//!d}' <file>
```
