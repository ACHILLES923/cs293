Produced by aditya gautam.

Lets see how i implemented linearqueue.cpp. An array is used to implement.==>

isEmpty()=> A linear queue is empty only when head of the queue is same as tail of the queue.

isFull()==> After some insertions and deletions, til will be N. After that no more element can the inserted into the queue. Hence the queue is full at tail == N.

grow()=> In a linearQueue, the queue can become full in two conditions. first if size() of queue is N, that means all elements are present into the queue.Second head is not equal to 0 and tail is N. In the second case,queue is not actually full, so we dont need to resize, we can just shift elements.

For the first cae, create a new array of large size using newSize() . Then copy all elements from original array to new array. Then make original array point to new array and change N=newSize.

For the second case, we just need to shift all elements such that they start from head=0. then make head = 0 and tail = currSize.

size()=>The number of elements at any tim in the wueue is tail-head.

Qinsert()=>First check if queue is full(). If it is then grow the array using grow function. THen insert element at tail and increment tail by 1.

Qdelete()=>first check if queue is empty. If it is then just return false. else put the element at head of the queue in x.Increment head and return true.

Lets see how i implemented circularQueue.cpp. Again an array is used for implementation.==>

IMPORTANT- At any point of time, we will only insert n elements in a n sized array to ensure that head==tail means that array is empty only.

isEmpty()=> if head and tail are same, then array is empty.

isFull()=> if size()==N-1 , then it is full. Because we insert only n-1 elements, so we have to resize if n elements are present.

grow()=> here queue is full only in one case when size()=N-1. if thatts the case, then just create new array and copy elements starting at head till tail to new array. then make original array point to new array and change n.

size()=> The number of elements in the queue is (N-head+tail)%N when if head is before tail, then head -tail is negative which means whole paranthesis is greater than N. else we subtract number of elements from N.

Qinsert()=>check if a queue is full. if it is then grow. ELse insert element at tail. then increment tail modularly by 1.

Qdelete()=>check if empty. if it is , then return false. Else put address of A[head]  in x.increment head by 1 modulo N. then return.
