---
layout: post
title: Minimalistic Shell Scripting Tutorial 
---
<p>The absolute basics ...</p>

## Control Structures 
### if / elseif / else
#### Syntax
``` bash 
if condition; then
	command 1
elif condition; then
	command 2
else
	command 3
fi 
```
#### Example
``` bash 
#!/bin/bash  
echo -n "Enter 1 or 2 > "
read x
if [ $x = 1 ]; then
        echo "you entered 1"
elif [ $x = 2 ]; then
        echo "you entered 2"
else
        echo "you entered $x"
fi
 ``` 
### Loops
#### for Syntax
``` bash 
for variable in list
do
	command 1
	...
	command n
done
``` 
#### for Example
``` bash
items=("x" "y" "z")
for v in "${items[@]}"
do
        echo $v
done

``` 
#### while Syntax
``` bash 
for variable in list
do
	command 1
	...
	command n
done
``` 
#### while Example
``` bash
items=("x" "y" "z") 
i=0 
while [ $i -lt "${#items[@]}" ]; do 
        echo ${items[$i]} 
        i=$(($i+1)) 
done
``` 

