## EXPERIMENT-2
## Exp 2a) Title:Implement class mechanism in Java.Create a class,methods and invoke them inside the main method.
## Souce code:
``` java
 public class Rectangle{
   double length;
   double breadth;
 double area(){
   return length*breadth;
 }
  double perimeter(){
    return 2*(length+breadth);
 }
}

 class Main {
    public static void main (String args[]){
    Rectangle rect = new Rectangle();
     rect.length = 10;
     rect.breadth = 5;
   double area = rect.area();
   double perimeter = rect.perimeter();
   System.out.println("area of given rectangle: "+area);
   System.out.println("perimeter of given rectangle: "+perimeter);
   }
 }
```
## Output:
![experiment 2 output](2a.png)



