# Activity-1 Blocks
## Instruction ## 
* Define a class called Test.java
* Add main method.
* Write System.out.println statement inside method with some message.
* Define 2 static blocks with some statements inside it.
* Define 2 static blocks with some staement inside it.
* Create object of Test class inside main method using new. Run the Test class. See the output.

***solution***

```java
package org.activity.Block;

class Test{
    static int num;

    static{
        System.out.println("Static Block 1");
        num = 100;
    }

    static{
        System.out.println("Static Block 2");
        num = 200;
    }
    public static void main(String args[])
    {
        Test t = new Test();
        System.out.println("Value of num: "+num);
        //System.out.println(t.num);
       // System.out.println(Test.num);


    }
}


```

***output***  
Static Block 1  
Static Block 2  
Value of num: 200  


# Activity 2 : Static Methods
## Instruction ##
* Define a class called Test.java
* Define main method.
* Define 2 static methods called as m1() and m2() with both having void return type. Add some statements in both of the methods.
* Call m1() from m2()
* From main method call m1() without creating object.
* Add a static block. call m1() from static block without using object. verify the output.
***solution***
```java

public class Test {

    public static void m1()
    {
        System.out.println("Inside m1()");
    }
    public static void m2()
    {
      System.out.println("Inside m2()");
      m1();
        System.out.println("After calling m1(),Inside m2().");
    }
    static
    {
        System.out.println("Inside static block");
        m1();
        System.out.println("After calling m1(),Inside static block.");
    }
    public static void main(String[] args)
    {
       // Test.m1();
        m1();
        m2();
    }
}

```
***output***  
Inside static block  
Inside m1()  
After calling m1(),Inside static block.  
Inside m1()  
Inside m2()  
Inside m1()  
After calling m1(),Inside m2().  


# Activity 3 : Non Static Methods
## Instructions ##
* Define a class called Test.java
* Define main method.
* Define 2 non-static methods called as m1() and m2() with both having void retunr type. Ass some statements in both of the methods.
* call m1() from m2().
* inside main method create object of Test using new. Test var = new Test().
* using above reference variable of Test call m1()
* Add a non static block. call m1() from non static block. verify the outout.
***solution***
```java

public class Test {
    {
        m1();
    }
    public void m1()
    {
        System.out.println("Inside m1()");
    }
    public void m2()
    {
        System.out.println("Inside m2()");
        m1();
        System.out.println("after calling m1() inside m2()");
    }
    public static void main(String[] args) {
        Test var= new Test();
        var.m1();
        var.m2();

    }
}
```
***output***  
Inside m1()  
Inside m1()  
Inside m2()  
Inside m1()  
after calling m1() inside m2()  
# Activity 4 : Parameterized Methods
## Instruction ##
* Define a class called Test.java
* Define a main method.
* Create a static method sum(int x, int y) and having return type as int. This should give sum of x + y
* Call sum(10, 20) from main method and print the result inside main method
 
***solution***
```java
public class Test{
    static int total=0;
    static int sum(int x,int y)
    {
        total=x+y;
        return total;
    }

    public static void main(String[] args)
    {
        sum(10,20);
        System.out.println("sum="+total);

    }
}


```
***output***  
sum=30  


# Activity 5 : Variable Declaration
## Instructions ##
* You may see compilation error with this activity. Define a class called Test.java
* Define a main method.
* Declare a static variable x of type int at the class level. Declare a non static varaible y of type String at the class level. Run the class. Verify output.
* Define a static block. print the value of x & y inside static block. Run the class. Verify output.
* Define a non-static block. print the value of x & y inside non-static block. Run the class. Verify output.
* Define a static method m1() with void return type. print the value of x & y inside static method. Run the class. Verify output.
* Define a non-static method m2() with void return type. print the value of x & y inside non-static method. Run the class. Verify output.
* print the value of x & y inside main method. Run the class. Verify output.
* Inside main method create object of Test class using new. Test var = new Test();
* call m2() using the reference variable var. Run the class. Verify output.
* Inside main method call m1() without object. Run the class. Verify output.
* What is the default value for x and y you are getting here?
***solution***
```java
public class Test {
    static int x;
    public String y;
    static
    {
        System.out.println("Inside static block");
        System.out.println("value of x="+x);
       // System.out.println("value of y="+y);
    }
    {
        System.out.println("Inside non static block");
        System.out.println("value of x="+x);
        System.out.println("value of y="+y);
    }
   public static void m1()
    {
        System.out.println("Inside static method");
        System.out.println("value of x="+x);
       // System.out.println("value of y="+y);
    }
    public void m2()
    {
        System.out.println("Inside non static method");
        System.out.println("value of x="+x);
        System.out.println("value of y="+y);
    }

    public static void main(String[] args) {
        Test var =new Test();
        m1();
        var.m2();
        System.out.println("Inside main method");
        System.out.println("value of x="+x);
      // System.out.println("value of y="+y);

    }
}


```
***output***  
Inside static block  
value of x=0  
Inside non static block  
value of x=0  
value of y=null  
Inside static method  
value of x=0  
Inside non static method  
value of x=0  
value of y=null  
Inside main method  
value of x=0  


# Activity 6 : Variable Declaration & Intialization
## Instruction ##
* You may see compilation error with this activity. Define a class called Test.java
* Define a main method.
* Declare a static variable x of type int at the class level. Declare a non static varaible y of type String at the class level. Run the class. Verify output.
* Define a static block. Initialize x = 20; and print x. Run the class. Verify output.
* Define a static method m1(). Initialize x = 30; and print x. Run the class. Verify output.
* From the main method call m1() without object. Run the class. Verify output.
* Define a non static block. Initialize y = "hello"; and print y. Run the class. Verify output.
* Define a non static method m2(). Initialize y = "bye"; and print y. Run the class. Verify output.
* Inside main method create object of Test using new. Test var = new Test(); From the main method call var.m2(). Run the class. Verify output.
***solution***
```java
public class Test {
    private static int x;
    public String y;

    static { // static blocks executes at the time of class load
        x = 20;
        System.out.println(x);
    }

    { // non static block will not be executed until the creation of object
        y = "hello";
        System.out.println(y);
    }

    public static void m1(){// method will not be executed until the method call - no need of object to call static met.
        x = 30;
        System.out.println(x);
    }

    public void m2(){ // method will not be executed until the method call - need a object to call the non static method
        y = "bye";
        System.out.println(y);
    }

    public static void main(String[] args) {
        System.out.println(x);
        Test var = new Test(); // this will invoke non static block
        var.m2(); // call m2() and execute it

    }
}
```
***output***  
20  
20  
hello  
bye  




# Activity 7 : Final Variables or Constants
## Instructions ##
* Define a class called Test.java
* Define a main method.
* Declare a final static variable x of int type. Try to initialize this 2 times.
* Declare a final non static variable y of int type. Try to initialize this 2 times.
***solution***
```java
class Test {
    final static String name = "saismita";

    int rollno;
    public
    static void main(String[] args)
    {
        Test ob = new Test();

      //  ob.name="anushka";  //Name should be constant..

        ob.rollno = 020;

        System.out.println(ob.name);

        System.out.println(ob.rollno);
    }
}
```
***output***  
saismita  
16  


