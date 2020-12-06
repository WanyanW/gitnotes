###  string and list
1. string, list, tuple are sequence types
	1. sequence is a ordered collection
	2. can be "" or '' 
	3. if the string contains multiple lines, use """... """ or '''...'''
	4. convert string to intger - int(string) or float - float(string)
2. list - sequence of any type of value
	1. [..., ..., ...]
	2. can contain diff types  
3. Tuple
	1. inmutable
	2. (..., ..., ...)
	3. if the tuple only have one element, e.g. myTuple = (100,); otherwise if myTuple = (100), type(myTuple) is int
	4. can contain diff types
4. index operator
	1. list[index] = list[-(len(list)-index)]
	2. string[index]
	3. len(str/list)
5. slice operator
	1. list[a, b] is extracting from list[index a] to list[index b-1]
6. concatenationa nd repetition
	1. [1, 2] + [3, 4] 
	2. ["apple", "pear", "banana"] + [1, 2]
	3. [0, 1] * 4 get [0,1,0,1,0,1,0,1]
7. call method on sequence
	1. seq_name.method_name() e.g. count()
	`a = "i have had an apple on my desk before!"`
	`print(a.count("e")` will get 5
	2. e.g. index()
	`music = "Pull out your music and dancing can begin"`
	`print(music.index("m")` will get 14
	if I am searching for substrings, it search for where it starts
	`print(music.index("us")` will get 15
8. splitting and joining strings
	1. string.split() -- a list of seperated substrings, default splitor is space
	2. can also designate splitor string.split("e")
	3. "/".join(["leaders", "and", "best"]) -- get "leaders/and/best"

### Iteration
1. for *loop_variable* in *list*:
	loop code block
2. accumulator pattern
	1. interate through a list of number and added each to accum variable 
3. Range function
	1. range(x) equals to [0, 1, 2, ... , x-1] up to not including x
	2. range(0, 5) equals to range(5)
	3. range() don't produce a list, you have to cast `range` to the list by list(range(5))

### Boolean expression
1. ==, !=
2. and, or, not
3. in, not in
	1. 'p' in 'apple' -- True (substring in string)
	2. '' in 'a' -- True

### conditional execution
```
if *condition*:
	do something
else:
	do other thing
```
1. omitting the cluse: unary selection
2. nested conditionals
```
if *condition*:
	do something
else:
	if *sub-condition*:
		do other thing 1
	else:
		do other thing 2
```
3. elif
```
if *condition 1*:
	do something
elif: *condition 2*:
	do other thing 1
else:
	do other thing 2
```
4. examples - combina accumulator pattern with conditionals
```
#count char number excluding space)
for char in pharse:
		if char !=" "
			num += 1
```
```
# track the highest value
best_num = nums[0]
for n in nums:
	if n > best_num:
		best_num = n
```

### sequence mutation
1. string is immut