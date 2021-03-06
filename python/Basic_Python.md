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
1. string is immutable
2. list is mutable
	1. delete some elements: 
	```
	alist = ['a', 'b', 'c', 'd']
	alist[1:3] = [] # delete elements from index 1 up to not including index 3 
	```
	2. can also delete by `del alist[1:3]`
3. objects and references
	1. 2 variable names pointed to the same value -- a is b is True (# a is alias of b)
	2. ``` 
	   a = [1, 2, 3]
	   b = [1, 2, 3]
	   print(a is b) # False
	   print(a == b) # True
	   # a and b are different list with same values
	   print(id(a)) 
	   print(id(b)) # the id of a and b are different
	```
4. aliasing
	1. the same list has two different names, a and b, we say that it is aliased. Changes made with one alias affect the other
	2. ``` 
	   a = [81, 82, 83]
	   b = [81, 82, 83]
	   print(a is b) # False

	   b = a #the value of b has been reassigned to the value of a.
	   b[0] = 5
	   print(a) # [5, 82, 83]
	   ```
5. cloning list
	1. ``` 
	   a = [81, 82, 83]
	   b = a[:] # cloining
	   print(a is b) # False
	   pritn(a == b) # True

	   b[0] = 5
	   print(a) # [81, 82, 83]
	   print(b) # [5, 82, 83]
	   ```
### methods on lists
1. append
	1. mylist.append(value)
	2. append vs concatenate: append add to the original list, concatenate create a new list
	```
	origlist = [45,32,88]
 	aliaslist = origlist
 	origlist += ["cat"] # aliaslist is also been added with ["cat"]
 	origlist = origlist + ["cow"] # now origlist is different with the aliaslist
	```
2. insert
	1. mylist.insert(index, value)
3. count
	1. mylist.count(value) #count how many elements == value
4. index
	1. mylist.index(value) # tell which index is the value
5. reverse
	1. mylist.reverse() # take the order and reverse
6. sort
	1. mylist.sort() # sort from small to big
7. remove
	1. mylist.remove(value) #specify the value, diff from del mylist[index]
8. pop
	1. mylist.pop() # remove the last item


### methods on strings
1. upper(), lower()
	1. ss.upper() # don't mutate ss
2. count() ss.count("l")
3. strip
	1. ss.strip() # get rid of white spaces at the start and end
4. replace #replace substring with substring
	1. ss.replace("l", "ls")
| Method | Parameters | Description |
| upper | none | Returns a string in all uppercase|
| lower | none | Returns a string in all lowercase|
| count | item | Returns the number of occurrences of item|
| index | item | Returns the leftmost index where the substring item is found and causes a runtime error if item is not found|
| strip | none | Returns a string with the leading and trailing whitespace removed|
| replace | old, new | Replaces all occurrences of old substring with new|
| format | substitutions | makes substitutions into places in a string enclosed in braces|
