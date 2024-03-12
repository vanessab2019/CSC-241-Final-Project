// CSC-241-Final-Project 
import java.util.*;

/*
* Author: Eli Ledford and Vanessa Bartolo
* Date: 03/11/2024
* Purpose: 
*/
public class EmployeeInfo{
	public static void main(String[] args) {
		//declare scanner object
		Scanner scnr = new Scanner(System.in);
		
		//declare object
		//project241 employeeInfo[];  
		EmployeeInfo[] Employee = new EmployeeInfo[3]; 
		//declare variables

		String employeeEmail;
		String employeeID;
		String employeeName;
		int employeeRating;
		
		//for loop to loop to input input
		for(int i = 0;i < 3;i++) {
		    int attempts = 0;
		    boolean validInput = false;
		    
		    while (!validInput && attempts < 3) {
		    try {
			System.out.println("What is the name of the first Employee?");
			employeeName = scnr.nextLine();
			
			System.out.println("What is " + employeeName + "'s ID?");
			employeeID = scnr.nextLine();
			
			System.out.println("What is " + employeeName + "'s email address?");
			employeeEmail = scnr.nextLine();
			
			System.out.println("What is " + employeeName + "'s job rating?");
			employeeRating = scnr.nextInt();
			
			if (employeeRating >= 0 && employeeRating <= 10){
            System.out.println("Thanks for all the info! It seems that the employee " + employeeName 
            + " with the ID of "+ employeeID + " and the email of " + employeeEmail + " rates their job at a " 
            + employeeRating + " out of 10 ");
			    
			} else {
            System.out.println("Sorry the input given for rating was invalid please make sure an Integer from 0-10 is entered");}
            
			
			//put values in the array of objects
	    Employee[i] = new EmployeeInfo();
	    
	    } catch (InputMismatchException e) {
	        System.out.println("Invalid input/s. Please ensure that valid integer/s between 0-10 are entered for the job rating portion");
	        scnr.nextLine(); //eats the invalid input
	        attempts++; }
	    }
	    if (!validInput){
	        System.out.println("You have reached your maximum limit of attempts with incorrect inputs please refresh and restart process to try again.");
	    }
	}}}
			
