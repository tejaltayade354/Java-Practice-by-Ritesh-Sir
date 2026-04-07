Java lecture(4-09-2025)



 



METHODS:



-A method can be defined as set of statements which are meant to perform certain operations.

-Benefits of methods:

1\.	reuse the code: we can avoid duplicate code.

2\.	The code length will be less.

3\.	the memory consumption is less.

4\.	will take less time for execution.

5\.	speed will be fast.



SYNTAX OF METHOD:



\[ACCESS MODIFIERS]\[MODIFIERS] RETURN TYPE        METHOD NAME(\[VARIABLES/ARGUMENTS/PARAMETER])

{

\[RETURN]



}



-Methods can be categorized into two types:

1\.	Static Methods

2\.	Non-static Methods





Return statement:



* The return statement is meant to return the control back to the caller method.
* To access static methods within a single class there are 3 approaches: directly, classname, object creation.
* The return statement should always be the last statement within the method.
* there should be only 1 return statement at the end of the method. ( example 3 error denar tyat 2 veda return state,ent use kel ahe )





program1:

class example1

{ // caller

 	public static void main(String\[] args)

 	{

 		System.out.println("START@ MY SUCCESS");

 		m1();   // directly

 		example1.m1();    // classname

 		                  // also there is 3 rd approach ---->object creation

        System.out.println("STOP@ MY overthinking");

 

 	}

 

 	//called

 	static void m1()

 		{

 	System.out.println("INSIDE m1 method");

 

 	}

}



output:



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac example1.java



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>java example1

START@ MY SUCCESS

INSIDE m1 method

INSIDE m1 method

STOP@ MY overthinking



program2:



class example2

{

 	public static void main(String\[] args)

 	{

 		System.out.println("ssssssssssssssstart");

 		test1();

 		System.out.println("sstop");

 

 	}

    static void test1()

 	{

 		return;   // threows error as unreachable statement.

 		System.out.println("inside test");

 

 	}



}



o/p:



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac example2.java

example2.java:13: error: unreachable statement

                System.out.println("inside test");

                ^

1 error



program 3:









program 4:



if we do not write the return statement, then the compiler will set the return statement.

-the main method after the execution, will also have to return the control back to the JVM.

-A method will use void as a return type, Whenever it is only used to return the control, without any data or information.

In java program, minimum we can create 1 method or multiple methods.



example 5:



class example5

{

 	public static void main(String\[] args)

 	{

 		System.out.println("start");

 		int a=100;

 		System.out.println("inside main " +a);

 		test1(a);

 		System.out.println("stop");

 

 	}

 	static void test1(int a){

 		System.out.println("INSIDE test1 method " +a);

 

 	}

}





output:



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac example5.java



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>java example5

start

inside main 100

INSIDE test1 method 100

stop





dddddddddxNote:

whever we declare a local variable within method, constructor, block, that variable can only be accessed **directly** within the same method area, constructor area, block area.





QUES: How do u access local variable from one area to another area?

--->  passing by value approach

QUES:     when will u go in real time pass by value?

---->

 



LOCAL VARIABE UPDATED DEFINITION: VARIABLES DECLARED WITHIN A METHOD, OR PART OF METHOD, CONSTRUCTOR, BLOCKS SUCH VARIABLES ARE CALLED AS LOCAL VARIABLE.



class example5

{

 	public static void main(String\[] args)

 	{

 		System.out.println("start");

 		int a=100;

 		System.out.println("inside main " +a);

 		test1(a);

 		System.out.println("stop");

 

 	}

 	static void test1(int a){  // a is local variable

 		System.out.println("INSIDE test1 method " +a);

 

 	}

}





output:



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac example5.java



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>java example5

start

inside main 100

INSIDE test1 method 100

stop



FINAL keyword:



iq: How do make a variable as a constant?

-->  By prefixing the modifier called as final, we can ensure that a variable can behave as a constant.







example 6:



class  example6

{

 	public static void main(String\[] args)

 	{ final int a=100;   // final means we declared the variable a =100 as constant

 	a=200; // a value will not get updated.

 

 		System.out.println(a);

 	}

}



o/p:

C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac example6.java

example6.java:5: error: cannot assign a value to final variable a

        a=200; // a value will not get updated.

        ^

1 error





ques:

// write a java program to calculate area of rectangle.

class example7



{

&nbsp;	public static void main(String\[] args) 

&nbsp;	{

&nbsp;		System.out.println("start");

&nbsp;		int length= 5;

&nbsp;		int breath= 7;

&nbsp;		arearec(length, breath);

&nbsp;	}

&nbsp;	static void arearec( int length, int breath)

&nbsp;	{

&nbsp;		int result=length\*breath;

&nbsp;		System.out.println("area" +result);

&nbsp;		

&nbsp;	}

}





ASSIGNMENTS:



calculate the 1)area of triangle,

              2)the area of circle,

              3)area of square. /// HINT declare variables in main and use formula in other method  .



1)AREA OF TRIANGLE



PROGRAM8:



class example8

{public static void main(String\[] args){

&nbsp;	int length=5;

&nbsp;	int breath= 6;

&nbsp;	area\_of\_triangle(length, breath);

}

&nbsp;	

static void area\_of\_triangle(int length,int breath)

&nbsp;	{ 

&nbsp;	double result=0.5 \* length \* breath;

&nbsp;    System.out.println("The area of triangle: "+result);

&nbsp;	}



}





C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac example8.java



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>java example8

The area of triangle: 15.0







2)the area of circle





class example9 

{

&nbsp;	public static void main(String\[] args) 

&nbsp;	{

&nbsp;		int radius=2;

&nbsp;		

&nbsp;		areaofcircle( radius );

&nbsp;		

&nbsp;	}

&nbsp;	static void areaofcircle(int radius){

&nbsp;		double result= 3.14\*radius\*radius;

&nbsp;		

&nbsp;		System.out.println("The area of circle is:" +result);

&nbsp;		

&nbsp;	}

}



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac example9.java



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>java example9

The area of circle is:12.56



class example10 

{

&nbsp;	public static void main(String\[] args) 

&nbsp;	{

&nbsp;	  int side= 9;

&nbsp;	  area\_of\_square(side);

&nbsp;	  

&nbsp;	}

&nbsp;	static void area\_of\_square(int side) {

&nbsp;		int result=side\*side;

&nbsp;		System.out.println("The Area Of Square: " +result);

&nbsp;	}

}



output:



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>javac example10.java



C:\\Users\\Tejal\\CCSP12 J AUGUST\\BASICS>java example10

The Area Of Square: 81

