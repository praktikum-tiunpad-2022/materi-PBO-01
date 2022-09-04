# Input & Output

```java {all|1-2|6-7|9-11|13-15|17-18|all}
// import class Scanner dari pakcage java.util
import java.util.Scanner;

public class Test {
  public static void main(String args[]){
    // Instansiasi objek scanner
    Scanner sc = new Scanner(System.in);

    //Input dengan objek scanner
    String name = sc.nextLine();
    int age = Integer.parseInt(sc.nextLine());

    // Output dengan System.out
    System.out.println("Thy shall know i as " + name);
    System.out.println("for i ame " + age + " years old.");

    // Menutup objek scanner supaya tidak terjadi memory leak
    sc.close();
  }
}
```