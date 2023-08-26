---
title: "Day 5 - Shell Scripting using loops"
datePublished: Sat Aug 26 2023 15:04:26 GMT+0000 (Coordinated Universal Time)
cuid: clls5k59f000f0amgeche2y5t
slug: day-5-shell-scripting-using-loops
tags: 90daysofdevops, day5, day5of-90dayofdevops-advanced-shell-scripting

---

## Task 1 -

Write a bash script [createDirectories.sh](http://createDirectories.sh) that when the script is executed with three given arguments (one is directory name and second is start number of directories and third is the end number of directories ) it creates specified number of directories with a dynamic directory name.

Example 1: When the script is executed as

`./`[`createDirectories.sh`](http://createDirectories.sh) `day 1 90`

then it creates 90 directories as `day1 day2 day3 .... day90`

Example 2: When the script is executed as

`./`[`createDirectories.sh`](http://createDirectories.sh) `Movie 20 50` then it creates 50 directories as `Movie20 Movie21 Movie23 ...Movie50`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693062047519/a138934f-b12a-41f7-a453-c51747911fa7.png align="center")

```powershell
#!/bin/bash

#################################
# Author : Riya Vyas
#
# Date : 26/08/2023
#
# This is a script that takes the base name for directories and range to make a list of directories using a for loop
##################################


echo "Enter the Directory base name: "
read base
echo "Enter the starting number :"
read start_num
echo "Enter the ending number: "
read end_num

#for i in {$start..$end}
for (( i = start_num; i <= end_num ; i++ ));
do
        mkdir $base$i
done
```

**Output -**

Sample run 1 -

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693062140767/78f457a9-4733-4092-88cc-1a7182d582d9.png align="center")

Sample run 2 -

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693062189926/75099e94-a818-43e9-a861-928f0ebec92c.png align="center")