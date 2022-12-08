# Comp-7.2
import java.text.DecimalFormat;

public class Student {

	   private String firstName, lastName;
	   private Address homeAddress, schoolAddress;
	   private double testOne=0,testTwo=0,testThree=0;
	   private double avg=0;
	    DecimalFormat fmt = new DecimalFormat ("0.###");

	   //-----------------------------------------------------------------
	   //  Constructor: Sets up this student with the specified values.
	   //-----------------------------------------------------------------
	   public Student(String first, String last, Address home,
	                  Address school, double test1, double test2, double test3)
	   {
	      firstName = first;
	      lastName = last;
	      homeAddress = home;
	      schoolAddress = school;
	      testOne=test1;
	      testTwo=test2;
	      testThree=test3;
	   }

	   //-----------------------------------------------------------------
	   //  Returns a string description of this Student object.
	   //-----------------------------------------------------------------
	   
	   public void setTestScore(int select,double score){
	       switch(select){
	           case 1:
	               testOne=score;
	               break;
	           case 2 :
	               testTwo=score;
	               break;
	           case 3 :
	               testThree=score;
	               break;
	       }
	   }
	   public double getTestScore(int select){
	       switch(select){
	           case 1:
	               return testOne;
	               
	           case 2 :
	               return testTwo;
	           case 3 :
	               return testThree;
	               
	           default:
	               return 0;
	   }
	   }
	   public int average(){
	       avg=(testOne+testTwo+testThree)/3;
	       
	       return (int)avg;
	   }
	   public String getName(){
	       return firstName;
	   }
	    @Override
	   public String toString()
	   {
	      String result;

	      result = firstName + " " + lastName + "\n";
	      result += "Home Address:\n" + homeAddress + "\n";
	      result += "School Address:\n" + schoolAddress;
	      result += "Test Score:\n" + "Test 1 = " +testOne;
	      result += " ,Test 2 = " +testTwo;
	      result += " \n,Test 3 = " +testThree;
	      
	      return result;
	   }

	}
