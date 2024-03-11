// CSC-241-Final-Project 
import java.util.*;

/*
* Author: Eli Ledford, Murtazza and Venessa
* Date: 03/11/2024
* Purpose: 
*/
public class project241 {
	public static void Main(String[] args) {
		//declare scanner object
		Scanner scnr = new Scanner(System.in);
		
		//declare object
		EmployeeInfo[] Employee = new EmployeeInfo[3]; 
		
		//declare variables
		String employeeEmail;
		String employeeID;
		String employeeName;
		int employeeRating;
		
		//for loop to loop to input input
		for(int i = 0;i < 3;i++) {
			System.out.println("What is the name of the first Employee?");
			employeeName = scnr.nextLine();
			System.out.println("What is " + employeeName + "'s ID?");
			employeeID = scnr.nextLine();
			System.out.println("What is " + employeeName + "'s email address?");
			employeeEmail = scnr.nextLine();
			System.out.println("What is " + employeeName + "'s job rating?");
			employeeRating = scnr.nextInt();
			//put values in the array of objects
			Employee[i] = new EmployeeInfo(employeeName, employeeEmail, employeeID, employeeRating);
		}
		
		
		
		
		
	}
}
