# experiment-1
## 1a) Title: Displaying Default Primitive Datatype
## Source Code
``` java
 class DisplayDefaultPrimitiveType{
   int PrimInt;
   double PrimDouble;
   float PrimFloat;
   char PrimChar;
   long PrimLong;
   short PrimShort;
   boolean PrimBoolean;
   public static void main(String[] args){
     DisplayDefaultPrimitiveType dDPT=new DisplayDefaultPrimitiveType();
     System.out.println("default int values:" +dDPT.PrimInt);
     System.out.println("default double values:" +dDPT.PrimDouble);
     System.out.println("default float values:" +dDPT.PrimFloat);
     System.out.println("default char values:" +dDPT.PrimChar);
     System.out.println("default long values:" +dDPT.PrimLong);
     System.out.println("default short values:" +dDPT.PrimShort);
     System.out.println("default Boolean values:" +dDPT.PrimBoolean);
   }
 }
```
## Output:
![experiment-1a output](primitive.png)

## Exp1b)Title:Calculate the roots of a Quadrative Equation
## Source code:
``` java
import java.util.Scanner;
class QuadraticEquationSolution{
  public static void main(String[] args){
    Scanner sc=new Scanner(System.in);
    System.out.print("Enter value a:");
    double a = sc.nextDouble();
    System.out.print("Enter value b:");
    double b = sc.nextDouble();
    System.out.print("Enter value c:");
    double c = sc.nextDouble();
    double D = b*b-4*a*c;
    if(D>0){
    double x1 = (-b+Math.sqrt(D))/(2*a);
    double x2 = (-b-Math.sqrt(D))/(2*a);
    System.out.println("roots are real");
    System.out.println("x1= " + x1);
    System.out.println("x2= " + x2);
    }
    else if(D==0){
    double y = -b/(2*a);
    System.out.println("roots are equal");
    System.out.println("y= " + y);
    }
    else if(D<0){
    double z1 = -b/(2*a);
    double img1 = Math.sqrt(-D)/(2*a);
    System.out.println("roots are complex");
    System.out.println("complex roots of root1: " + z1 + "+" + img1 + "j");
    System.out.println("complex roots of root2: " + z1 + "-" + img1 + "j");
    }
    else{
    System.out.println("invalid choice");
    }
  }
}
```
## Output:
## Case-1(D>0):
![Experiment 1b output](quad1.png)
## Case-2(D=0):
![Experiment 1b output](quad2.png)
## Case-3(D<0):
![Experiment 1b output](quad3.png)




