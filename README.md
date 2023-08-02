# backtrace

Latest Change:
    Used libunwind library to get more function information
 
Command to Compile and Run: 
    <br/>
    `g++ *.cpp -g -o backtrace`
    <br/>
    `./backtrace`
    <br/>
    `dot -Tpng tree.dot -o tree.png`


Visualization: 

![Visualization](./tree.png)


Output:

main

True
main
0
1

main
test_1

139809273187024
main
test_1
test_2

main
test_1
test_2
test_3

main
test_1
test_2
test_3

True
main
1
2

main
test_1
test_2
test_3

139809273187024
main
test_1
test_2
test_3

main
test_1
test_2
test_3

main
test_1
test_2
test_3

True
main
2
3

main
test_1
test_2
test_3

139809273187024
main
test_1
test_2
test_3

main
test_1
test_2
test_3

main
test_1
test_2
test_3

True
main
3
4

main
test_1
test_2
test_3

139809273187024
main
test_1
test_2
test_3

main
test_1
test_2
test_3

main
test_1
test_2
test_3

True
main
4
5

main
test_1
test_2
test_3

139809273187024
main
test_1
test_2
test_3

main
test_1
test_2
test_3

main
test_1
test_2
test_3

True
main
5
6

main
test_1
test_2
test_3

139809273187024
main
test_1
test_2
test_3

main
test_1
test_2
test_3

main
test_1
test_2
test_3