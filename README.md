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

# 4. combined 

class Pet {

    String type = "Pet";    

    Pet() {             
        System.out.println("Pet parent class constructor");    }

    void sound() {          
        System.out.println("Animal makes sound");    }
}

class Cat extends Pet {

    String type = "Cat";    

    Cat() {                
        super();            
        System.out.println("Cat child class constructor");    }

    void printInfo() {
        System.out.println("Parent type: " + super.type);   
        System.out.println("Child type: " + this.type);    }

      void sound() {
        super.sound();      
        System.out.println("Meow");     }
}

public class Main {

    public static void main(String[] args) {
        Cat c = new Cat();
        System.out.println();
        c.printInfo();
        System.out.println();
        c.sound();
    }
}

Output:

Pet parent class constructor

Cat child class constructor

Parent type: Pet

Child type: Cat

Animal makes sound

Meow
