![image](https://github.com/vlantonakos/Java/assets/107072477/ddc8cf60-23c3-4285-a8f7-f400298e2872)

##Blocking vs. Non-blocking I/O

Blocking I/O

Blocking IO wait for the data to be write or read before returning. 
Java IO's various streams are blocking. 
It means when the thread invoke a write() or read(), then the thread is blocked until there is some data available for read, or the data is fully written.

Non blocking I/O

Non blocking IO does not wait for the data to be read or write before returning. 
Java NIO non- blocking mode allows the thread to request writing data to a channel, but not wait for it to be fully written. The thread is allowed to go on and do something else in a mean time.

##Stream Oriented vs. Buffer Oriented

Stream Oriented

Java IO is stream oriented I/O means we need to read one or more bytes at a time from a stream. 
It uses streams for transferring the data between a data source/sink and a java program. 
The I/O operation using this approach is slow.

Buffer Oriented

Java NIO is buffer oriented I/O approach. Data is read into a buffer from which it is further processed using a channel. 
In NIO we deal with the channel and buffer for I/O operation.
The major difference between a channel and a stream is:
    A stream can be used for one-way data transfer.
    A channel provides a two-way data transfer facility.
Therefore with the introduction of channel in java NIO, the non-blocking I/O operation can be performed.
