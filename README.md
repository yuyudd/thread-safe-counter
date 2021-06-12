# thread-safe-counter

Project #2 (thread-safety by semaphore)
OS environment WSL2 Ubuntu Linux Window10

Compare performance(mutex vs semaphore)


To use time command

-mutex-
  
![mutux ex](https://user-images.githubusercontent.com/84024206/121779078-e1661100-cbd4-11eb-86d2-783771202e23.JPG)

-semaphore-

![semaphore ex](https://user-images.githubusercontent.com/84024206/121779204-7ec14500-cbd5-11eb-96c1-ad5c7c8fc8f3.JPG)

Mutex is faster than semaphore.

A mutex allows a single thread to consume a resource or critical section. With a mutex, other threads trying to access a resource have to wait in a queue until the current thread has finished using the resource. Semaphores, on the other hand, allow a limited number of concurrent access to a resource. That is, in a semaphore, a shared resource can be accessed by as many processes (or threads) as the semaphore variables, and a mutex can only be accessed by one process (or thread). But semaphore need to check and change the semaphore value. Since the semaphore is constantly being changed, the execution time will be long. However, since a mutex cannot be used by two threads at the same time, it can act as the next thread without wasting time.

