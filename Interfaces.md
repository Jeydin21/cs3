Name: Jeydin Pham
Period: 5
Date: 9/5/2023

# Unit 2: Interfaces

- An interface is a list of methods that must be implemented
- An interface may not contain any implemented methods. Intefaces do not have constructors
- Interfaces are used when you know what you want an object to do, but do not know what will be used to get it done
- If only the behavior is known > use interface

```java
public interface myHope {
    boolean geta100inCalcBC();
}

public class Student implements MyHope {
    // instance variables and constructors
    boolean geta100inCalcBC() {
        // ...
    }
}
```

## Comparable Interface

```java
public interface Comparable {
    int comparableTo(Object o); // Abstract - an idea of what to do
}

public class Creature implements Comparable {
    private int size;
    public Creature(int g) {
        size = g;
    }
    public int comparableTo(Object o) {
        Creature other = (Creature) o;
        if(size > other.size) {
            return 1;
        } else if(size < other.size) {
            return -1;
        }
        return 0;
    }
}
```

##### Note: If an entire hierarchy of classes implements the same interface, you can write very generic code to manipulate all the classes at once

```java
Comparable[] list = {3, 8, 7, 6, 5, 4, 9};
Arrays.sort(list);
for(Comparable num : list) { // This uses the compareTo() method to check each object while sorting
    System.out.println(num);
}

Comparable x = 54;
Comparable y = 67;
System.out.println(x.compareTo(y)); // -1
```

```java
Comparable x = "23";
Comparable y = "45";
System.out.println(x.compareTo(y)); // -2
```

```java
Comparable x = "dog";
Comparabe y = "hog";
System.out.println(x.compareTo(y)); // -4
```

```java
public interface Locatable {
    public int getX();
    public int getY();
}

public interface Moveable {
    public void setPos(int x, int y);
    public void setX(int x);
    public void setY(int y);
}

class Ship implements Locatable, Moveable {
    private int xPos, yPos;
    // How many methods need to be implemented (5)
}
```
