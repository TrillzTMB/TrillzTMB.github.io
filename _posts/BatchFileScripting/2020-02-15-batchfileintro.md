---
title: Batch Scripting - For/Loops
categories:
  - Programming
  - Batch File Scripts

published: true
toc: false
---

### Useful Windows for/loop examples

The following are some basic examples of useful batch file commands;

 - The following loops forever :
   ```bash
	for /L %i in (1,0,2) do echo test 
	```
 - Loop from 1 to 255 :
   ```bash
	for /L %i in (1,1,255) do echo %i - 1 to 255 items
	```
 - The following pings localhost 255 times:
   ```bash
	for /L %i in (1,1,255) do echo %i & ping -n 5 127.0.0.1
	```
 - ping and nslookup :
   ```bash
	for /L %i in (1,1,25) do echo 10.10.10.%i: & @nslookup 10.10.10.%i 2>nul | find "Name"
	```


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5ODIwMzQ5NywtMTE1MDQ0NDQ0MCwzNj
A1MDY4OV19
-->