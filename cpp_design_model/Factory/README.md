## 工厂模式

最常用的一种设计模式之一。 工厂模式属于创建型模式，大致可以分为三类，简单工厂模式、工厂方法模式、抽象工厂模式。听上去差不多，都是工厂模式。

* **简单工厂模式**

将不同的类的实例创建集成到工厂中，在创建实例时，需要在工厂类中做判断，从而创造相应的产品。

* 当增加新的产品时，就需要修改工厂类。违反了开放封闭原则

* **工厂方法模式**

定义一个用于创建对象的接口，让子类决定实例化哪一个类。每个类拥有自己工厂，而客户根据自己的需要来决定使用哪种工厂来创建自己的实例。

工厂方法将工厂功能的添加从修改变为了扩展，虽然符合开放封闭原则，却也导致需要定义很多工厂带来的麻烦。

* **抽象工厂**

提供一个创建一系列相关或相互依赖对象的接口，而无需指定它们具体的类。

为每种工厂指定多种功能。

## 区别

* 工厂方法模式：

    一个抽象产品类，可以派生出多个具体产品类。   
    一个抽象工厂类，可以派生出多个具体工厂类。   
    **每个具体工厂类只能创建一个具体产品类的实例。**

* 抽象工厂模式：

    多个抽象产品类，每个抽象产品类可以派生出多个具体产品类。   
    一个抽象工厂类，可以派生出多个具体工厂类。   
    **每个具体工厂类可以创建多个具体产品类的实例（而实际最终的产品是通过多个具体产品组成的，也就达到了灵活组装的目的）。**

* 工厂方法模式只有一个抽象产品类，而抽象工厂模式有多个。   

* 工厂方法模式的具体工厂类只能创建一个具体产品类的实例，而抽象工厂模式可以创建多个。

简单工厂是工厂方法一种简单特例，只有一个具体工厂，有多个具体的产品类。抽象工厂则是在工厂方法的基础上，将产品组成的各部分进行灵活组装。