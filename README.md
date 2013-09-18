03_Queue_Lab
============

Implement an array-based queue in C++

Note: When you create your project, do NOT add ArrayQueue.ipp to the list of source files, add it to the list of include files. You will see that ArrayQueue.ipp is #included at the bottom of ArrayQueue.h. See ArrayQueue.h for more explanation.

Requirements
------------

1. remove takes O(1) time
2. add takes O(1) time, unless it calls grow (in that case O(n) is okay)
3. grow is only called if the number of items == backingArraySize, and the size of the array is doubled during grow
4. grow takes O(n) time
5. Do not leak memory (make sure grow and the destructor do the right thing)
6. getNumItems is O(1) time
7. add and remove throw excpetions as appropriate
8. You must use the array in a circular fashion. If you don't do this you probably won't be able to get #1, #2 and #3 to all be true.

Reading
=======
"Open Data Structures," Chapter 2, up through section 2.4 (ArrayDequeue). http://opendatastructures.org/ods-cpp/2_Array_Based_Lists.html

Questions
=========

#### 1. Which of the above requirements work, and which do not? For each requirement, write a brief response.

1. Works it should only take 0(1) to remove an item
2. Works it should only take 0(1) to add an item unless there is not enough space and you must grow the array
then it will take 0(n)
3. Works takes a new array and makes its size double the old one then adds the items from the old array to the new one.
4. Works it only takes 0(n);
5. Works needed to make sure in the destrcutor to call delete[] on backingArray before reinitializing it.
6. Works it is one simple call.
7. Works they through exceptions according to when the instructions ask to throw.
8. Works done by using the % as explained in the readings.

#### 2. If we did a Stack instead of a Queue, which of the private methods and variables would we need to keep, and which could we get rid of? Explain your answer.

#### 3. None I think overal this was a pretty good lab to get the hang of how Queues qork using modulus.

#### 4. #include "filename"

#### 5. What is the purpose of "templates" in C++?

#### 6. What would the syntax be for dynamically allocating an array of 10 ints, in C++?

#### 7. What is the purpose of a class destructor in C++? Why don't you need them in Java?