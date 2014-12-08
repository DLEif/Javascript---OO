#Javascript-OO

##类 , 对象 和 实例
###类（Class）
类是对对象的抽象概念。
For example:

###对象（Object）
对象是类的一个实例，是一个特定的类。
For example:

###实例（Instance）
实例化表示一个动作，去实例一个对象。或者说强调是实例。
For example:人是一个类，女人就是一个对象，实例就是具体到某一个人“小丽”。

###三者关系：
类实例化得出对象，即对象是类的实例化。
##JS中如何定义Class？
    function Person(name, age, sex){
      this.name = name;
      this.age = age;
      this.sex = sex;
    }
    function Female(name,age){
      Person.call(this,name,age,'Female');
    }
    Female.prototype = Object.create(person.prototype);
    Female.prototype.constructor = Female;
##JS中如何定义属性
###方法：
###1.类方法
    fuction Person(name, age, sex){
      this.name = name;
      this.age = age;
      this.sex = sex;
    }
    Person.helloWorld = fuction(){
      return 'HelloWorld';
    }
    var helloWorld = Person.helloWorld();
    console.log(helloWorld);
###2.实例方法
    fuction Person(name, age, sex){
      this.name = name;
      this.age = age;
      this.sex = sex;
    }
     Person.prototype.gethName = fuction(){
     return this.name;
    }
    var person = new Person('Joy',18,'Female');
    var name = person.getName();
    console.log(name);
站在调用者角度去思考，只在乎调用函数所输出的结果，不在乎运行的过程。
##三要素
###1.封装

###2.继承

###3.多态
