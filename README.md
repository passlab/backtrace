# backtrace

Latest Change:
    Started using the libunwind library to get more information on functions to accurately build tree. 

 
Command to Compile and Run: 
    <br/>
    `g++ *.cpp -g -rdynamic -lunwind -lunwind-x86_64 -o backtrace`
     added flags for program to link to libunwind library
    <br/>
    `./backtrace`

    

Output when run:

    2
    works

    ./backtrace(_start+0x2d) [0x7f78cb60347d]
    /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0xf2) [0x7f78cb1a4082]
    ./backtrace(main+0x25) [0x7f78cb6049c5]
    ./backtrace(_Z3fooi+0x33) [0x7f78cb604ab5]
    ./backtrace(_Z3barv+0x53) [0x7f78cb604b0c]
    ./backtrace(_Z15printStackTraceii+0x48) [0x7f78cb60436d]
    callee
    _Z15printStackTraceii
    caller
    _Z3barv
    test2
    6
    ./backtrace(_Z9otherTestv+0x5d) [0x7f78cb604b72]
    ./backtrace(_Z14otherOtherTestv+0x33) [0x7f78cb604ba9]
    callee
    _Z15printStackTraceii
    caller
    _Z14otherOtherTestv
    context tree works

    _start 0x7f78cb60347d 0x7fffd128f0d0
    __libc_start_main 0x7f78cb1a4082 0x7fffd128f210
    main 0x7f78cb6049c5 0x7fffd128f150
    _Z3fooi 0x7f78cb604ab5 0x7fffd128f2f0
    _Z3barv 0x7f78cb604b0c 0x7fffd128f350
    _Z15printStackTraceii 0x7f78cb60436d 0x7fffd128f450
    _Z9otherTestv 0x7f78cb604b72 0x7fffd128f720
    _Z14otherOtherTestv 0x7f78cb604ba9 0x7fffd128f780
