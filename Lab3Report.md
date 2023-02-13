# Options for Find

## Option 1: Find -name

The find - name option is useful because it helps us find the name of the files that contain the name you want.

Example 1: 

Input: 

```
find . -name "ch5.txt"
```

Output: 
```
./written_2/non-fiction/OUP/Kauffman/ch5.txt
./written_2/non-fiction/OUP/Fletcher/ch5.txt
```

Here, the find - name command helps us find any file that contains ch5.txt.

Example 2:

```
find . -name "ch4.txt"
```

Output:

```
./written_2/non-fiction/OUP/Abernathy/ch3.txt
./written_2/non-fiction/OUP/Rybczynski/ch3.txt
./written_2/non-fiction/OUP/Kauffman/ch3.txt
```

Herem the find - name command helps us find any file that contains ch3.txt.


## Option 2: Find - size

The find - size option is useful because it helps us find any files that are bigger than the size you specify.


Example 1:

Input:
```
find ./non-fiction/OUP/Abernathy -size +50k
```

Output:
```
./non-fiction/OUP/Abernathy/ch8.txt
```

Here, the find - size +50k helps us find any txt file in the Abernathy file that is bigger than 50 KB.

Example 2:

Input: 
```
find ./non-fiction/OUP/Abernathy -size +10k 
```

Output:
```
./non-fiction/OUP/Abernathy/ch2.txt
./non-fiction/OUP/Abernathy/ch3.txt
./non-fiction/OUP/Abernathy/ch1.txt
./non-fiction/OUP/Abernathy/ch7.txt
./non-fiction/OUP/Abernathy/ch6.txt
./non-fiction/OUP/Abernathy/ch8.txt
./non-fiction/OUP/Abernathy/ch9.txt
./non-fiction/OUP/Abernathy/ch15.txt
./non-fiction/OUP/Abernathy/ch14.txt
```

Here, the find - size +10k returns any txt file in the Abernathy file that is bigger than 10 KB.


## Option 3: Find - type

The find - type command helps us find files of a specific type.

Example 1:

Input: 
```
find . -type d 
```

Output: 
```
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Berk
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Rybczynski
./non-fiction/OUP/Kauffman
./non-fiction/OUP/Fletcher
./non-fiction/OUP/Castro
./travel_guides
./travel_guides/berlitz1
./travel_guides/berlitz2
```

Here, the command find . -type d helps us find any directories.

Example 2: 

Input:
```
find ./non-fiction/OUP/Abernathy -type f
```

Output: 
```
./non-fiction/OUP/Abernathy/ch2.txt
./non-fiction/OUP/Abernathy/ch3.txt
./non-fiction/OUP/Abernathy/ch1.txt
./non-fiction/OUP/Abernathy/ch7.txt
./non-fiction/OUP/Abernathy/ch6.txt
./non-fiction/OUP/Abernathy/ch8.txt
./non-fiction/OUP/Abernathy/ch9.txt
./non-fiction/OUP/Abernathy/ch15.txt
./non-fiction/OUP/Abernathy/ch14.txt
```

Here, the command find -type f helps us find the files under the Abernathy file.

## Option 4: 
