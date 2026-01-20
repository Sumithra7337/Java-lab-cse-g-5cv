## EXPERIMENT-3
## EXP-3a)Title:Implement constructor overlapping in JAVA.
## Source code:
``` java
class Student{
  String name;
  int age;
  double marks;
  Student(){
  }
  Student(String name,int age,double marks){
    this.name = name;
    this.age = age;
    this.marks = marks;
  }
  void display(){
    System.out.println("Name: " + name);
    System.out.println("Age: " + age);
    System.out.println("Mark: " + marks);
  }
}
class Main{
  public static void main(String args[]){
    Student std = new Student();
    std.display();
    Student std1 = new Student("Sumithra",19,98.2);
    std1.display();
  }
} 
```
## OUTPUT:
![Experiment 3 output](constructor ovverlapping.png)

