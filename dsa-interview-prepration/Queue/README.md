## What is a queue?
Queue is the linear data structure that follows **First In First Out** (FIFO) principle, means that the element added into the queue will be the first one to be removed. For example people waiting in the line to get movie ticket.

## What are the main operations of a queue?
The main operation of a queue are:
- enqueue() : Adds an element on the back of queue
- dequeue() : Removes an element from the front of the queue
- peek() : Returns the front element without removing it
- isEmpty() : Check it the queue is empty
- size() : return the number of elements in a queue

## Can a queue be resized at runtime?
The resizing of queue at runtime depends upon the data structure use to implement queue.
#### Array-based Queue
Array based queue can not be resized at runtime, because size is fixed when the queue is created as array has a predefined size.
#### Linked List-based Queue
Linked List based queue can grow and shrink dynamically at runtime. since linked list doesn't require contiguous memory, nodes can be added or removed freely. <br>
note: Collection framework for java also allow dynamically resizing of queue at runtime.

## What is the time complexity for enqueue and dequeue operations?
- enqueue() : O(n)
- dequeue() : O(n)

## What are the applications of a queue?
Queue offers wide range of its application in real world scenario:
- Task scheduling: Operating systems uses queue to manage various tasks.
- Breath-First-Search(BFS) : Queue is used to explore graph nodes level by level at the time of traversal.
- Network Buffers : Queue manage data packets in the network for proper order of delivery.

## What is priority queue, and how is it different from a normal queue?
It is a queue with a special feature of priority, means that every element of the queue has assign a priority.
- Element with higher priority dequeued before the elements with the least priority.
- Elements are enqueued anywhere based on the priority.
- Used for CPU scheduling, dijkstra's Algorithms.

##  How would you implement a priority queue?
The data structure is most efficient and widely used for the implementation of priority queue is Heap(usually min-heap or max-heap). Some programming language also provides the built-in methods for the priority queue like in `java` we have Java's `PriorityQueue` class.

## What is the time complexity for searching in a queue?
The time complexity for searching in queue is `O(n)`.

## What is a blocking queue?
A Blocking Queue is a thread-safe data structure used in multi-threaded environment where one thread may wait for another thread to provide data. <br>
For example:
- Producers add items to the queue.
- Consumers remove items from the queue.
- If the queue is full, the producer thread is blocked (waits) until space is available.
- If the queue is empty, the consumer thread is blocked (waits) until an item is available.

