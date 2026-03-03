# java-lab-cseg-5en
experiments
## Experiment 1
## Title:1a(Implement Default Primitive Type)
```
class DefaultPrimitiveType {
    byte primbyte;
    short primshort;
    int primint;
    double primdouble;
    char primchar;
    float primfloat;
    long primlong;
    boolean primboolean;
    public static void main(String args[]) {
        DefaultPrimitiveType dDpt = new DefaultPrimitiveType();
        System.out.println("default value of byte:" + dDpt.primbyte);
        System.out.println("default value of short:" + dDpt.primshort);
        System.out.println("default value of int:" + dDpt.primint);
        System.out.println("default value of double:" + dDpt.primdouble);
        System.out.println("default value of char:" + dDpt.primchar + " '");
        System.out.println("default value of float:" + dDpt.primfloat);
        System.out.println("default value of long:" + dDpt.primlong);
        System.out.println("default value of boolean:" + dDpt.primboolean);
    }
}
```
## Output:
![Output for 1a](https://github.com/MEENUGA-VISHNUPRIYA/java-lab-cseg-5en/blob/1ff701e93cf5123f4db7a41c539a64565d12f382/1a.png)
## Title:1b(Implement Quadratic Equation Solution)
```
import java.util.Scanner;
class Quadraticequation{
     public static void main(String args[]){
         Scanner sc=new Scanner(System.in);
         System.out.println("Enter value of a:");
         double a=sc.nextDouble();
          System.out.println("Enter value of b:");
         double b=sc.nextDouble();
          System.out.println("Enter value of c:");
         double c=sc.nextDouble();
         double D=b*b-4*a*c;
         if(D>0){
            System.out.println("Roots are real and distinct");
            double root1=(-b+Math.sqrt(D))/(2*a);
            double root2=(-b-Math.sqrt(D))/(2*a);
            System.out.println("Root1:"+root1);
            System.out.println("Root2:"+root2);
            }
         else if(D==0){
            System.out.println("Roots are equal and real");
            double root=-b/(2*a);
            System.out.println("Root:"+root);
            }
         else{
            System.out.println("Roots are complex and imaginary");
            double realpart=-b/(2*a);
            double imaginarypart=Math.sqrt(-D)/(2*a);
            System.out.println("Roots are complex and imaginary");
            System.out.println("Root1="+realpart+"+i"+imaginarypart);
            System.out.println("Root2="+realpart+"-i"+imaginarypart);
            }
        sc.close();
        }
   }
```
## Output:
![Output for 1b](https://github.com/MEENUGA-VISHNUPRIYA/java-lab-cseg-5en/blob/086ac9070df1c48f8f6e6441bf04f1a1464bce35/1b.png)
## Title:2a(Implement class mechanism)
```
class Rectangle{
  double l;
  double b;
  double area(){
    return l*b;
  }
  double perimeter(){
   return 2*(l+b);
   }
 }
class main{
  public static void main(String args[]){
    Rectangle rect =new Rectangle();
    rect.l=6;
    rect.b=12;
    double area = rect.area();
    double perimeter =rect.perimeter();
    System.out.println("area is:" +area);
    System.out.println("perimeter is:" +perimeter);
    }
  }
```
## Output:
![Output for 2a](https://github.com/MEENUGA-VISHNUPRIYA/java-lab-cseg-5en/blob/8fabdba666381491eddfc334b43eb37279bc0ff2/2a.png)
## Title:2b(Implementing overloading method)
```
class sum{
  int sum(int a ,int b){
    return a+b;
  }
  int sum(int a ,int b,int c){
  return a+b+c;
  }
  double sum(double a ,double b){
   return a+b;
  }
}
class main{
 public static void main(String args[]){
   sum s= new sum();
   System.out.println("sum of 2 integers:"+s.sum(20,16));
   System.out.println("sum of 3 integers:"+s.sum(20,16,17));
   System.out.println("sum of two real numbers:"+s.sum(30.465,15.675));
  }
}
```
## Output:
![Output for 2b](https://github.com/MEENUGA-VISHNUPRIYA/java-lab-cseg-5en/blob/2560466f9fa3c408b9a5167c5f69a544f9ea4532/2b.png)
## Title:2c(Implement Constructor)
```
class student{
 String sname;
 int sage;
 double smarks;
 student(String name,int age,double marks){
   sname=name;
   sage=age;
   smarks=marks;
  }
 void display(){
  System.out.println("student name is :"+sname);
  System.out.println("student age is :"+sage);
  System.out.println("stduent marks is:"+smarks);
  }
}
class main{
 public static void main(String args[]){
  student std= new student("sree",12,960);
  std.display();
  }
}
```
## Output:
![Output for 2c](https://github.com/MEENUGA-VISHNUPRIYA/java-lab-cseg-5en/blob/0042e36fa7655f2d05523c53f62ec9a7bba3796b/2c.png)
## Additional Experiment:2(Fibonacci series)
```
class Fibonacis {

    int firstnumber;
    int secondnumber;
    int thirdnumber;
    int sum;
    int size_of_fibsequence;

    Fibonacis(int size) {
        firstnumber = 0;
        secondnumber = 1;
        thirdnumber = 0;
        sum = 0;
        size_of_fibsequence = size;
    }

    void generate_fibsequence() {

        while (size_of_fibsequence > 0) {

            if (size_of_fibsequence == 1)
                System.out.print(firstnumber + " ");
            else
                System.out.print(firstnumber + " ");

            sum += firstnumber;

            thirdnumber = firstnumber + secondnumber;
            firstnumber = secondnumber;
            secondnumber = thirdnumber;

            size_of_fibsequence--;
        }
    }
    int getfibsum(){
      return sum;
  }
 }
import java.util.Scanner;
class main{
  public static void main(String args[]){
     System.out.println("Enter size of fibsequence:");
     Scanner sc=new Scanner(System.in);
     int size=sc.nextInt();
     if(size>0){
     Fibonacis fib=new Fibonacis(size);
     System.out.println("Fibonacci series are:");
     fib.generate_fibsequence();
     System.out.println("The sum of fibonacci series:"+fib.getfibsum());
     }
     else{
     System.out.println("Fibonacci sequence and sum cannot be calculated");
     }
}
}
```
## Output:
![Output for addexp 2](https://github.com/MEENUGA-VISHNUPRIYA/java-lab-cseg-5en/blob/4b74aefac99961b5c506b2cdd9eeebd31d173cd9/addexp-2.png)
## Title:3a(Implement Constructor Overload)
```
class student{
 String name;
 int age;
 double marks;
 student(){
 }
 student(String name,int age,double marks){
  this.name=name;
  this.age=age;
  this.marks=marks;
}
void display(){
  System.out.println("name:"+name);
  System.out.println("age:"+age);
  System.out.println("marks:"+marks);
  }
}

class main{
 public static void main(String args[]){
   student std= new student();
   std.display();
   student std1=new student ("sree",19,60);
   std1.display();
 }
}
```
## Output:
![Output for 3a](https://github.com/MEENUGA-VISHNUPRIYA/java-lab-cseg-5en/blob/108293e4bd5ecb235d279dcfbc3ab3b3bfbc6ecb/3a.png)
## Title:3b(Implement Binary Search)
```
import java.util.Scanner;
class Binary {
    int list[];
    int size;
    Binary(int size) {
        this.size = size;
        list = new int[size];
    }
    void setList() {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter items in ascending order:");
        for (int i = 0; i < size; i++) {
            System.out.println("Enter value of " + (i + 1) + ":");
            list[i] = sc.nextInt();
        }
    }
    void getList() {
        System.out.println("List elements:");
        for (int i = 0; i < size; i++) {
            System.out.print(list[i] + " ");
        }
        System.out.println();
    }
    int binary(int key) {
        int low = 0;
        int high = size - 1;
        while (low <= high) {
            int mid = (low + high) / 2;
            if (list[mid] == key)
                return mid;
            else if (list[mid] < key)
                low = mid + 1;
            else
                high = mid - 1;
        }
        return -1;
    }
}
class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter size of list:");
        int size = sc.nextInt();
        Binary b = new Binary(size);
        b.setList();
        b.getList();
        System.out.println("Enter a key to search:");
        int key = sc.nextInt();
        int index = b.binary(key);
        if (index == -1) {
            System.out.println("Key item does not exist");
        } else {
            System.out.println("Key item exists at position: " + (index + 1));
        }
    }
}
```
## Ouput:
![Output for 3b](https://github.com/MEENUGA-VISHNUPRIYA/java-lab-cseg-5en/blob/0cfb039a53f0ee9d63fbab05e5912eeaca9407d8/3b.png)
## Title:3c(Implement Bubble sort)
```
class BubbleSort {
    BubbleSort(int arr[]) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }

            }
        }
    }
}
import java.util.Scanner;
class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter size of array:");
        int n = sc.nextInt();
        int arr[] = new int[n];
        System.out.println("Enter elements:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        new BubbleSort(arr);
        System.out.println("Sorted array:");
        for (int i = 0; i < n; i++) {
            System.out.print(arr[i] + " ");
        }
    }
}
```
## Output:
![Output for 3c](
