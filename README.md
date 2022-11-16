## Java Top Interview ques & ans

__Q.1 How string immutable in java?__

Ans: When the below statement is executed, the VM takes the value of String str, i.e. “knowledge” and appends ” base”, giving us the value “knowledge base”. Now, since Strings are immutable, the VM can’t assign this value to str, so it creates a new String object, gives it a value “knowledge base”, and gives it reference str.
```
String str = "knowledge";
System.out.println(str+" "+str.hashCode());
str=str.concat("base");
System.out.println(str+" "+str.hashCode());

Output:
knowledge 1549887614
knowledge base 1993134797
```

__Q.2 Difference between Comparable and Comparator?__

Ans:Comparable and Comparator both are interfaces and can be used to sort collection elements.
![compare diff](https://user-images.githubusercontent.com/41982681/202136286-ff0d5565-ee18-40a9-a610-2e4a954bc20e.PNG)

__Q.3 What is hashing in java?__

Ans:Hashing is a technique or process of mapping keys, and values into the hash table by using a hash function. It is done for faster access to elements. The efficiency of mapping depends on the efficiency of the hash function used.
__Modular Hash function:__
Let a hash function H(x) maps the value x at the index x%10 in an Array. For example if the list of values is [11,12,13,14,15] it will be stored at positions {1,2,3,4,5} in the array or Hash table respectively.

![hashing](https://user-images.githubusercontent.com/41982681/202137622-f2a533f1-2fd7-468e-b2af-3cd57519e2b8.PNG)

__Q.4 What is Hashing Collision & its Handling?__ 

Ans: Since a hash function gets us a small number for a big key, there is possibility that two keys result in same value. The situation where a newly inserted key maps to an already occupied slot in hash table is called collision and must be handled using some collision handling technique. 
Following are the ways to handle collisions: 
* __Chaining:__ The idea is to make each cell of hash table point to a linked list of records that have same hash function value. Chaining is simple, but requires additional memory outside the table.
* __Open Addressing:__ In open addressing, all elements are stored in the hash table itself. Each table entry contains either a record or NIL. When searching for an element, we examine the table slots one by one until the desired element is found or it is clear that the element is not in the table.

__Q.5 Difference b/w Parcelable and Serializable interface?__

Ans:
__Serializable__
Serializable is a standard Java interface. You can just implement Serializable interface and add override methods. The problem with this approach is that reflection is used and it is a slow process. This method creates a lot of temporary objects and causes quite a bit of garbage collection. However, Serializable interface is easier to implement.

__Parcelable__
Parcelable is a standard android sdk interface. Parcelable process is much faster than Serializable. One of the reasons for this is that we are being explicit about the serialization process instead of using reflection to infer it. It also stands to reason that the code has been heavily optimized for this purpose.

__Q.6 Does method overloding possible in case of inheritance?__
Ans: yes,but parent class and properties hides in this case.

