package com.company;
class Person{
    String Name;
    int age;

    Person(String Name,int age){
        this.Name = Name;
        this.age = age;
    }
    void display(){
        System.out.println("Имя: " + this.Name + " возраст: " + this.age);
    }
}
class Emp extends Person{
    String company;
    String profession;
    double salary;

    Emp (String Name,int age,String company,String profession,double salary){
        super(Name,age);
        this.company = company;
        this.profession = profession;
        this.salary = salary;
    }
    @Override
    public void display(){
        System.out.println("Имя: " + this.Name +
                " возраст:" + this.age +
                " компания:" + this.company +
                " должность:" + this.profession +
                " зарплата:" + this.salary);
    }
}
public class Main {

    public static void main(String[] args) {
	Person Hastua = new Person("Настя",20);
	Hastua.display();

	Person Vika = new Person("Вика",16);
	Vika.display();

	Emp People = new Emp("Настя", 20, "Сладевиль", "Бухгалтерский учет", 50000.50);
	People.display();

	Emp People1 = new Emp("Вика", 16, "Новадрайв", "Продавец", 20000.00);
	People1.display();
    }
}
