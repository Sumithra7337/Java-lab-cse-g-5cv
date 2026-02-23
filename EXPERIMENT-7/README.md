# EXPERIMENT-7
# 7A) TITLE:Write  a JAVA program for creation of User Defined Exception.
# SorceCode:
``` java
class InvalidCountryException extends Exception {
  InvalidCountryException() {
    super();
  }
  InvalidCountryException(String message) {
    super(message);
  }
}
class userRegistration {
  void registerUser(String userName, String userCountry) throws InvalidCountryException {
      if(!userCountry.equals("India")) {
        throw new InvalidCountryException("User outside India cannot be registered");
      }
      else {
        System.out.println("User Registration Done Successfully");
      }
    }

    public static void main(String[] args) {
      userRegistration ur = new userRegistration();
      try {
        ur.registerUser("srilatha ", "russia");

      }
      catch(InvalidCountryException e) {
        System.out.println(e.getMessage());
    }
  }
}
```
# OUTPUT:
![Experiment 7 output](7a.png)

# 7b) Title: Write a JAVA program that creates threads by extending Thread class.
# SourceCode:
``` java
class GoodMorningThread extends Thread {
  public void run() {
    for(int i=0; i<10; i++) {
      System.out.println("Thread1: Good Morning ");
    }
    try {
      Thread.sleep(1000);
    }
    catch(Exception e) {
      System.out.println("Exception : " + e);
    }

  }
}
class HelloThread extends Thread {
  public void run() {
    for(int i=0; i<10; i++) {
      System.out.println("Thread2: Hello ");
    }
    try {
      Thread.sleep(2000);
    }
    catch(Exception e) {
      System.out.println("Exception : " + e);
    }
  }
}
class WelcomeThread extends Thread {
  public void run() {
    for(int i=0; i<10; i++) {
      System.out.println("Thread3: Welcome");
    }
    try {
      Thread.sleep(3000);
    }
    catch(Exception e) {
      System.out.println("Exception : " + e);
    }
  }
}
class TestThread {
  public static void main(String[] agrs) {
    GoodMorningThread t1 = new GoodMorningThread();
    HelloThread t2 = new HelloThread();
    WelcomeThread t3 = new WelcomeThread();
    t1.start();
    t2.start();
    t3.start();
  }
}
```
# OUTPUT:
![experiment 7 output](7b.png)

 # 7c) Write a program for creation of JAVA Built-in EXceptions.
 # SourceCode:
 ``` java
class LongRunningTask extends Thread {

    public void run() {
        System.out.println("Long running task Started");

        for(int i = 0; i < 5; i++) {
            System.out.println("Working... " + i + " iteration");
            try {
                Thread.sleep(1000);
            }
            catch(Exception e) {
                System.out.println(e);
            }
        }

        System.out.println("Long running task Completed");
    }
}

class ThreadDemo {

    public static void main(String[] args) throws Exception {

        LongRunningTask task1 = new LongRunningTask();

        System.out.println("Before starting task1: " + task1.isAlive());

        task1.start();

        System.out.println("After starting task1: " + task1.isAlive());

        System.out.println("Main thread waiting for task1 to complete using join operation");

        task1.join();

        System.out.println("After join: " + task1.isAlive());

        System.out.println("Main thread continues after task1 is completed");
    }
}
```
# OUTPUT:
![experiment 7 output](7c.png)
