Lab Report 3
=======
_Sravya Chittuluri_

I chose the `find` command to explore for this lab. 

***iname***

`-iname`: just like the name command but case insensitive. This is useful to find files without worrying about having to use the exact cases in the file name.

```
find non-fiction/OUP/Berk -iname 'ch4*'
```
Output: 
```
non-fiction/OUP/Berk/CH4.txt
```

Here, the find command locates the CH4.txt file in Berk even without using the correct case.

```
find travel_guides/berlitz1 -iname 'handrhawaii.txt'
```
Output: 
```
travel_guides/berlitz1/HandRHawaii.txt
```

Here, the find command locates the HandRHawaii.txt file in berlitz1 even without using the correct case.

***atime***

`-atime`: returns true if a file was accessed n * 24 hours ago. This is useful to check what files you've visited at certain points in time.

```
find . -atime -1 
```
Output:
```
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Berk
./non-fiction/OUP/Castro
./non-fiction/OUP/Fletcher
./non-fiction/OUP/Kauffman
./non-fiction/OUP/Rybczynski
./travel_guides
./travel_guides/berlitz1
./travel_guides/berlitz2
```
Here, the find command returns a list of files that I accessed in the last day. The -1 in the command means in the last 24 hours.

```
find . -atime 6 
```
Output: 

Here, the output is blank because 6 days ago, I didn't clone the written_2 directory into the remote server yet. This lets me know that none of the files were touched that day.

***size***

`-size`: returns true if a file uses n units of space on the disk. This is useful to figure out the sizes of files.

```
find . -size +500b -type f
```
Output: 
```
./travel_guides/berlitz1/WhereToItaly.txt
```

Here, the only txt file that is bigger than 500 bytes is the WhereToItaly.txt file.

```
find . -size -3b -type f
```
Output: 
```
./travel_guides/berlitz1/HandRIbiza.txt
./travel_guides/berlitz1/HandRIstanbul.txt
```
Here, the files that are less than 3 bytes are HandRIbiza.txt and HandRIstanbul.txt.

***depth***

`-depth`: limits the search to a specified level of directories. This is useful to reduce the amount of time spent searching through numerous directories, and is more useful in large directories with large depths.

```
find . -maxdepth 2 -iname 'berlitz2*'
```
Output: 
```
./travel_guides/berlitz2
``` 
Here, the output is the relative path to get to berlitz2.

```
find . -maxdepth 3 -iname 'Bermuda*'
```
Output:
```
./travel_guides/berlitz2/Bermuda-WhatToDo.txt
./travel_guides/berlitz2/Bermuda-WhereToGo.txt
./travel_guides/berlitz2/Bermuda-history.txt
```
Here, the output is the relative paths for files containing Bermuda in their name.
