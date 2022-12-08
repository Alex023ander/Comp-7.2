# Comp-7.2

import java.util.ArrayList;

public class Course {
    
    private String course;
	    static ArrayList<String> studentNames=new ArrayList<String>();
	    static ArrayList<Student> student=new ArrayList<Student>();
	    
	    public Course(String course){
	    	this.course=course;
	    }
	    public void addStudent(Student enroll){
	        studentNames.add(enroll.getName());
	        student.add(enroll);
	    }
	    public ArrayList roll(){
	        return studentNames;
	    }
	    public int average(){
	        int avg=0;
	        for(Student tester:student){
	            avg+=tester.average();
	        }
	        return avg/student.size();
	    }
}
