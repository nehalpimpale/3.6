# 3.6


Q1.

The return value alone is not sufficient for the compiler to figure out which function to call:

public int foo() 
{

  ...
} 
public float foo() 

{

  ..
} 
  ... 
foo();     // which method to call? 

So while overloading a method the return type should be same. We can overload method in 2 ways 
1.different type of method arguments 
2.different number of method arguments

To avoid the ambiguity of compiler the return type of overloaded method should be same.

overloading with different return type will give following error

class A
{ 

  static int add(int a,int b)
  {
  
    return a+b;
  } 
  static double add(int a,int b)
  {
  
    return a+b;
  } 
} 

class B
{

  public static void main(String[] args)
  { 
  
    System.out.println(Adder.add(11,11));     //ambiguity 
  }
  
} 

In this when code is compiled it will show error as: 
Overloading3.java:3: error: method add(int,int) is already defined in class A static double add(int a,int b){return a+b;}

Q2.

import java.util.Arrays; import java.util.Scanner;

public class acad { public static void main(String[] args) { Scanner sc=new Scanner(System.in); int n=sc.nextInt(); //size of array int[] arr=new int[n]; int[] arr1=new int[n]; for(int i=0;i=0;i--) { arr1[j]=arr[i]; //Storing elements in reverse order(Descending) j++; } for(int x : arr1) System.out.println(x); //Displaying array elements in descending order sc.close(); } }
