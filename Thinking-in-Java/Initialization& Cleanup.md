###Overloading  

1. Primitive type narrowings and widenings  
![Java Primitive type Narrowings and Widenings](https://github.com/adrrrrrrrian/ReadingNotes/blob/master/Thinking-in-Java/I%26C-1.java%20primitive%20type%20widenings%20and%20narrowings.PNG)  
If you have a data type that is smaller than the argument in the method, that data type will be promoted. **char** is a bit different, 
if it does not find an excat **char**match, it is promoted to **int**.  
If you have a wider data type than the argument in the method, you need to perform a narrowing conversion with a cast. Or, 
you will have an error message.  

2. We can not use return values to distinguish overloaded methods, usually we use class names and argument lists (even the order is different is okay). Because we can call the methods and ignore 
the return value, and in that case Java would not be able to determine which method to be called.  

3. If you don't have a contructor in your class, Java will create a default one for you; But if you have a constructor or more than one, 
Java will not create that default constructor for you.   

4. Normally when you use **this**, it means "this object" or "the current object". But in a constructor, **this** keyword means differently 
when you give it an argument list. That will make an explicit call to the constructor matching the argument list.  
Notification: Don't use this(aaa) in a non constructor. Don't call two constructors using **this**. In addition, the constructor must be 
the first thing to do, or you will get a compiler error message.  

5. You can not call non-static methods inside a static method. There is no **this**.  



