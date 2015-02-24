# SED

##
Switch | Description
--------------------
-i | Apply changes to the file, without -i the changes will be applied on the stream

## Delete
### Delete lines between two patterns
Delete everething between two patterns including the rows where the pattern reciedes.
```bash
sed -i '/PATTERN1/,/PATTERN2/d' <file>
```

