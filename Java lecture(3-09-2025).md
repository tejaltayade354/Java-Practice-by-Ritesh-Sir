Java lecture(3-09-2025)



IQ :Is it mandatory to initialize the local variables before printing?

->  yes



class  localvariable2

{

 	public static void main(String\[] args)

 	{

 		int a;

 		System.out.println(a);    // error

 	}

}



o/p:

C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac localvar.java

localvar.java:5: error: variable a might not have been initialized

      System.out.println(a);

                         ^

1 error





2\) static variables:

\- variables which are **declared** outside the method, constructors and blocks but within the class  and is prefixed static ,such variable are called static variables.



NOTE:

-THE dot operator in java is also called as access operator.

-the access operator is used  to access a member within a specific area(classname)



IQ: How many ways are there to access static members in a single class?

---> Total 3 ways to access static members- directly, classname(DOT OPERATOR), object creation.



class  staticvar1

{

 	public static void main(String\[] args)

 	{

 		 static int a = 100;

 		System.out.println(a);    // directly

                System.out.println(staticvar1.a);    // classname

                System.out.println(a);    // object creation



 	}

}



O/P:

C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>java staticvar1

100

100



EXAMPLE 2)



class  staticvar2

{

   static int a = 100;

   static float b=200.5f;



 	public static void main(String\[] args)

 	{

                float result;

                result= a+Staticvar2.b;

                System.out.println("The result" +result);    // directly

 

 	}

}



o/p:

C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac staticvar2.java



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>java staticvar2

The Result: 300.5



Example 3)



class staticvar3

 {

   static int a=100;

   static float result;

   public static void main(String\[] args){

 	   float b=200.5f;

 	   staticvar3.result=staticvar3.a+b;

 	   System.out.println("RESULT: " +staticvar3.result);

   }

 }



o/p:

C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac staticvar3.java



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>java staticvar3

RESULT: 300.5





IQ:   how do we access static members from another class?

----> There are total 2 approaches, classname, object creation.



eg:



class Demo{

 	static int x=100;

}

class staticvar4

{

 	public static void main(String\[] args)

 	{

 		// directly accessing is invalid

 		System.out.println(Demo.x); //valid, object creation pn valid asel

 	}

}



IQ:



class Cyber

{ static float x=100.5f;



}

class Success

{ static int y=200;

}

class staticvar5

{ static float result;



 	public static void main(String\[] args)

 	{

 		int z= 300;

 		staticvar5.result=Cyber.x+Success.y+z;

 		System.out.println(result);

 	}

}

C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac staticvar5.java



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>java staticvar5

600.5





IQ: is it mandatory to initialize static variables before printing?

--> No, if we do not initialize static variables, then the compiler will initialize the static variables with default values.

 

prog:



class staticvar6

{static int a;

static float b;

 	public static void main(String\[] args)

 	{

 		System.out.println(a);

 		System.out.println(b);

 	}

}



op:



/\* C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>java staticvar6

0

0.0\*    /



assignment: what are the default values of byte. short, long, double, char, Boolean?

----------> PROG:



class staticvar7

{static byte a;

static short b;

static double c;

static boolean d;

static long e;

static char name;

 	public static void main(String\[] args)

 	{

 		System.out.println(a);

 		System.out.println(b);

 		System.out.println(c);

 		System.out.println(d);

 		System.out.println(e);

 		System.out.println(name);

 

 	}

}







O/P:



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac staticvar7.java



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>java staticvar7

0

0

0.0

false

0







IQ:  can we use static variables in method?

---> we cannot make a local variable as static.

 



METHODS:



-A method can be defined as set of statements which are meant to perform certain operations.

-Benefits of methods:

1. reuse the code: we can avoid duplicate code.
2. The code length will be less.
3. the memory consumption is less.
4. will take less time for execution.
5. speed will be fast.



SYNTAX OF METHOD:



\[ACCESS MODIFIERS] \[MODIFIERS]   RETURN TYPE     METHOD NAME(\[VARIABLES/ARGUMENTS/PARAMETER])

{

RETURN



}



-Methods can be categorized into two types:

1. Static Methods
2. Non-static Methods



Return statement:

* the return statement is meant to return the control back to the caller method.
