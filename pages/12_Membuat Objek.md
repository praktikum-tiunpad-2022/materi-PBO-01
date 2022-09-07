# Membuat Object dari Class

<br>
<br>

```java {all|3|all}
public class Test {
  public static void main(String args[]){
    Ship ferry = new Ship();

    if (ferry.getCrew() < 30){
      ferry.setCrew(30);
    }

    System.out.println("The following ship has " + ferry.getCrew() + " crew.");
  }
}
```

Instansiasi class menjadi object dilakukan dengan keyword `new` diikuti dengan class yang akan dijadikan object