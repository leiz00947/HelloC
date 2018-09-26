# HelloC++

## 代码类说明

- **AcctABC** :	练习抽象基类以及虚方法的使用
- **BaseDMA** :	使用动态内存分配和友元的继承范例
- **MIworker**:	多重继承实例

## 关键字

- **define**
- **typedef**
- **typename**
- **explicit**
- **operator**

## 知识点

- **静态联编和动态联编**

- **内联函数**

- **析构函数**

- **友元函数**

- **复制构造函数**

- **成员初始化列表**

- **派生类**

	- 创建派生类对象时，程序首先调用基类构造函数，然后再调用派生类构造函数
	- 基类构造函数负责初始化继承的数据成员
	- 派生类构造函数主要用于初始化新增的数据成员
	- 派生类构造函数总是调用一个基类构造函数
	- 可以使用初始化成员列表句法指明要使用的基类构造函数，否则将使用默认的基类构造函数
	- 派生类对象过期时，程序将首先调用派生类析构函数，然后再调用基类析构函数
	
	---
	
	> 在派生类方法中，标准的技术是使用作用域解析操作符来调用基类方法

- **虚方法**

	使用关键字**virtual**定义虚方法

	> 如果要在派生类中重新定义基类的方法，通常应将基类方法声明为虚拟的；这样，程序将根据对象类型而不是引用或指针的类型来选择方法版本；为基类声明一个虚拟析构函数也是一种惯例；关键字**virtual**只用于类声明的方法原型中

- **向上强制转换和向下强制转换**

- **抽象基类（abstract base clas, 简称 ABC）**

	在原型中使用 **=0** 指出类是一个抽象基类
	
	> 当类声明中包含纯虚函数时，则不能创建该类的对象，即包含纯虚函数的类只用作基类；而要成为真正的 ABC，必须至少包含一个纯虚函数，而在虚函数后缀加上 **=0** 就可以使其成为纯虚函数

- **函数模板**

- **类模板**

- **私有继承**

	使用私有继承，基类的公有成员和保护成员都将成为派生类的私有成员
	
	使用公有继承，基类的公有方法将成为派生类的公有方法，简言之，派生类将继承基类的接口；而使用私有继承，基类的公有方法将成为派生类的私有方法，简言之，派生类不能继承基类的接口，但可以在派生类的成员函数中使用它们

- **保护继承**

- **多重继承（multiple inheritance, MI）**

- **虚基类**