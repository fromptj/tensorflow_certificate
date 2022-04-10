# 493.607 Core Software: Assignment 1
### Sangkyu Rhim ([sk.rhim@snu.ac.kr](mailto:sk.rhim@snu.ac.kr "student's email address"))  

## Directories & Files
- ./gold_results: contains the original answer text
- ./test: contains test files that were used to test the functionality of the code
- wordCountSort.cpp: the main scripts which include details of the implementation
- check_text_same.py: script for checking if the output result and answer result are identical

## Clean project
```
$ make clean
```

## Compile & Run
```
$ make all
```
### Expected Results 
Standard Output:
```
the: 780
simba: 510
a: 374
...
```
and a `results.txt` file which includes the outputs line-by-line.

## Checking the results
If you want to check whether if output `results.txt` is the same as the answer,
```
$ make check
```
### Expected Result (Standard Output):
```
The following are texts that do not have a pair:
From the input text, ['qu: 1\n']
From the gold text, ['qué: 1\n']
The rest of input texts are identical to the gold ones

cpplint wordCountSort.cpp
wordCountSort.cpp:10:  <regex> is an unapproved C++11 header.  [build/c++11] [5]
Done processing wordCountSort.cpp
Total errors found: 1
make: *** [check] Error 1
```
From this result, only 'qué' is not parsed correctly. However, this is considered valid according to this [announcement](http://etl.snu.ac.kr/mod/ubboard/article.php?id=1812180&bwid=2819749 "Assignment 1 수정사항( 3.18 update)").

According to `cpplint`, the only problem with this code is the use of `regex`, which is not approved. 

## Others
This project also includes the `test` command used for testing the functionalities of the main script. If you are interested you can use this by:
```
$ make test
```
