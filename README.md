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
