# Producer-Consumer in C
**Program fully written in PT-BR!**


Two processes share the same memory area (in this case they share the same file).
One process will write to the end of the file a random value r ∈ [0, 99]. This process is called the producer. The
other process, the consumer, will remove the values from the beginning of the file. The producer will insert a value into the file and wait s seconds, where s is a random
integer s ∈ [1, 3]. The consumer will also use the same waiting logic to remove elements from the file. The name of the
file will be buffer.txt and it will be initialized with 10 integers (one integer per line). To avoid problems with
concurrency when accessing the buffer.txt file, before writing or reading, the processes must create
a buffer.txt.lock file that indicates that the buffer.txt is being used. When you finish writing or reading you must
erase it. Thus, before writing or reading a file one must check if the file buffer.txt.lock exists. If this file
exists then the process must wait until it is available to read or write to buffer.txt. Must be done using the
fork call. 

### Execution example:
```
$ ./producer-consumer
[Consumer] 91
[Consumer] 10
[Producer] 62
[Consumer] 33
[Consumer] 79
[Producer] 9
[Producer] 52
[Producer] 34
...
```
