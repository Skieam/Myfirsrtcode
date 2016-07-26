// Myfirstcode

// 关于'接口'的小测试

//接口
interface Interesting{
	public abstract void interesting();
}

//定义一个父类: Person
abstract class Person{
	//成员变量
	private String name;
	private int age;
	
	//无参构造
	public Person(){}
	
	//有参构造
	public Person(String name, int age){
		this.name = name;
		this.age = age;
	}
	
	//成员方法:get/set xxx 
	public String getName(){
		return name;
	}
	
	public void setName(String name){
		this.name = name;
	}
	
	public int getAge(){
		return age;
	}
	public void setAge(int age){
		this.age = age;
	}
	
	//成员方法
	public void running(){
		System.out.println("I just wanna run,running away~");
	}
	
	//抽象方法
	public abstract void rest();
}

//子类：运动员
class Athlete extends Person{
	public Athlete(){}
	
	public Athlete(String name, int age){
		super(name,age);
	}
	
	public void running(){
		System.out.println("Athletes run 15 laps");
	}
	
	public void rest(){
		System.out.println("Athletes rest 15 minutes");
	}
}

//interesting运动员
class InterestingAthlete extends Person implements Interesting{
	public InterestingAthlete(){}
	
	public InterestingAthlete(String name, int age){
		super(name,age);
	}
	
	public void running(){
		System.out.println("interestings run 20 laps");
	}
	
	public void rest(){
		System.out.println("interestings rest 10 minutes");
	}
	
	public void interesting(){
		System.out.println("excited!");
	}
}

//子类：教练类
class Coach extends Person{
	public Coach(){}
	
	public Coach(String name, int age){
		super(name,age);
	}
	
	public void running(){
		System.out.println("Coaches walk 1 laps..");
	}
	
	public void rest(){
		System.out.println("Coaches rest -__- whenever they want ");
	}
}

class InterestingCoach extends Person implements Interesting{
	public InterestingCoach(){}
	
	public InterestingCoach(String name, int age){
		super(name,age);
	}
	
	public void running(){
		System.out.println("Interestings walk 1 laps ~_~");
	}
	
	public void rest(){
		System.out.println("Interestings rest |-_-|");
	}
	
	public void interesting(){
		System.out.println("Excited!");
	}
}

//测试类
class Interfacedemo {
	public static void main(String[] args){
		//创建Athlete对象
		/** Person p = new Athlete();
		
		//赋值
		p.setName("Alan");
		p.setAge(15);
		
		System.out.println(p.getName()+"--"+p.getAge());
		
		//调用方法
		p.running();
		p.rest();
		
		Athlete a = (Athlete)p;
		a.running();
		a.rest();
		*/
		InterestingAthlete ia = new InterestingAthlete("Bob",16);
		System.out.println(ia.getName()+"--"+ia.getAge());
		
		ia.running();
		ia.rest();
		ia.interesting();
	}
}




