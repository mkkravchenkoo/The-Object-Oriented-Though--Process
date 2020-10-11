#### Абстрактный класс 
— это класс, содержащий один или несколько методов, которые не имеют какой-либо обеспеченной реализации
Единственными методами, которые подкласс должен реализовать, являются те, что объявлены в суперклассе абстрактными. Эти абстрактные методы представляют собой контракт.
В некоторых языках для реализации контрактов используются только абстрактные классы, в некоторых - интерфейсы

Интерфейс для класса — это, в сущности, подписи его методов.

Абстрактные классы включают абстрактные и конкретные методы, а интерфейсы содержат только абстрактные методы.
Интерфейс никогда не обеспечивает реализации какого-либо рода — только поведение


```
public interface Nameable {
    String getName();
    void setName (String aName);
}

public abstract class Mammal {
    public void generateHeat() {
        System.out.println("Выработка тепла");
    }
    public abstract void makeNoise();
}

public class Dog extends Mammal implements Nameable {
    String name;
    public void makeNoise(){
        System.out.println("Лай");
    }
    public void setName (String aName) {
        name = aName;
    }
    public String getName () {
        return (name);
    }
}

```