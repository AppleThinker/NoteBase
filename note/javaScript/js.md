1.说说对 prototype和 ___proto ___ 的理解
    prototype是函数的属性，他本身也是个函数对象，  ___proto ___是所有对象都有的属性。 ___proto ___指向构造它的对象的prototype。

原型链：当js查找对象的属性时，先查找对象自身是否具有该属性，如果没有，就会去___proto ___指向的prototype对象上查找，直到找到或者__proto __为null

    Javascript里面都是对象，必须有一种机制，将所有对象联系起来。
    js通过new命令生成实例，new后面跟的是构造函数。
    prototype是构造函数的属性，通过改动它能改动所有的对象实例。
    由于所有的实例对象共享同一个prototype对象，那么从外界看起来，prototype对象就好像是实例对象的原型，而实例对象则好像"继承"了prototype对象一样。

2.使用构造函数实现一个类Foo，需要有属性 count, 方法bar(), 并且写出创建该类对象的方法
    function Foo(){
        this.count=0;
    }
    Foo.prototype.bar(){

    }
    var foo =new Foo();
    foo.bar();