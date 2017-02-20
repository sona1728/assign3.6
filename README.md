1.)
ques:  Can you overload a method with same return type.? Explain your answer with proper logic.
ans:

Yes, the method can be overloaded with same return type.

The method should be overloaded with the same return type in order to
avoid ambiguity.
For example,
class A{
static int add(int a,int b){return a+b;}
static double add(int a,int b){return a+b;}
}
class B{
public static void main(String[] args){
System.out.println(Adder.add(11,11));//ambiguity
}}
In this when code is compiled it will show error as:
Overloading3.java:3: error: method add(int,int) is already defined in class A
static double add(int a,int b){return a+b;}

To overcome this problem method should be overloaded with the same return type.


2.)
ques: Write a program in java using Arrays, that sorts the element in descending order.

ans:

import java.util.Arrays;
import java.util.Scanner;


public class acad {
public static void main(String[] args){
Scanner sc=new Scanner(System.in);
int n=sc.nextInt(); //size of array
int[] arr=new int[n];
for(int i=0;i<n;i++){
arr[i]=sc.nextInt();
}
Arrays.sort(arr);               //sorting array
for(int i=arr.length-1;i>=0;i--){
System.out.print(arr[i]+" "); // displaying sorted reverse ordered
array elements
}
}
}
