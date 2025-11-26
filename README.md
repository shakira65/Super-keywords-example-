# Super-keywords-example-

# 1. Call parent class variables

class Animal {

    String a= "Pet" ;
}

class Cat extends Animal {

    String b= "Cat" ;

    void printType() {
        System.out.println(super.a);  
        System.out.println(this.b);   
    }
}

public class Main {

    public static void main(String[] args) {
        Cat d = new Cat();
        d.printType();
    }
}

Output:
Pet

Cat

# 2. Call parent class methods

class Animal {

   void sound() {
   
        System.out.println("Animal makes sound");
    } 
}

class Cat extends Animal {

   void sound() {
   
        super.sound(); 
        System.out.println("Meow");
 }

}
public class Main {

    public static void main(String[] args) {
        new Cat().sound();
    }
}

Output:
Animal makes sound

Meow


# 3. Call Parent Class Constructor

class Animal {


  Animal() {
  
        System.out.println("Animal constructor");
    }
}

class Cat extends Animal {

       Cat() {
        super();  
        System.out.println("Cat constructor");
    }

}

public class Main {

    public static void main(String[] args) {
        new Cat();
    }
}

Output:
Animal constructor

Cat constructor
