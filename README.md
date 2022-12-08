# Comp-7.2

public static void main(String[] args) {
      
      
        Address school = new Address("800 Lancaster Ave.", "Villanova", "PA", 19085);
        Address jHome = new Address("21 Jump Street", "Blacksburg", "VA", 24551);
        Student jake = new Student("Jake", "January", jHome, school, 95,55,100);
        Address mHome = new Address("123 Main Street", "Euclid", "OH", 44132);
        Student michael = new Student("Michael", "McGriddy", mHome, school,84.3,55,96);

		System.out.println(jake);
		System.out.println();
		System.out.println(michael);
		System.out.println(michael.average());
		Course math = new Course("math");
		math.addStudent(michael);
		math.addStudent(jake);
		System.out.println(math.roll());
		System.out.println(math.average());
	}



}
