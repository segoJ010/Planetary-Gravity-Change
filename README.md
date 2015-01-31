/*
	Author: Juan Segoviano
	Class: ITCS 1213-002
	Program: Planets.java
	Purpose: The purpose of this program is to determine 
				the amount of weight the user will have when
				he/she is on a different planet. The user will
				enter the normal weight, and the program will 
				execute calculations for the different weight, 
				which will be shown on screen. After, the user will
				be asked if he/she wishes to repeat the process.
*/

import java.util.Scanner;

public class Planets
{  public static void main(String[] args)
	{
	   // Variables to be used for the program
		double normalWeight; //The user's weight on Earth
		double mercuryWeightFix; // user's weight times 0.4
		double venusWeightFix; // user's weight times 0.9
		double jupiterWeightFix; // user's weight times 2.5
		double saturnWeightFix; //user's weight times 1.1
		double mercuryWeight; //The user's weight in Mercury
		double venusWeight; //The user's weight in Venus
		double jupiterWeight; //The user's weight in Jupiter
		double saturnWeight; //The user's weight in Saturn
		char repeat; // necessary for user to repeat the process 
		String input; // Needed for the confirmation of the request
		
		//The program will ask for the user to input his/her weight
		Scanner keyboard = new Scanner(System.in);
		
		//This loop is needed since the end of the program will 
		//be determined by the user's wish to repeat or end it
		do
		{
		   System.out.print("Please type in your weight on Earth: ");
		   normalWeight = keyboard.nextDouble();
		
		    //The program will now calculate the user's weight with fixed number of each of the four planets	
		    mercuryWeightFix = normalWeight * 0.4;
		    venusWeightFix = normalWeight * 0.9;
		    jupiterWeightFix = normalWeight * 2.5;
		    saturnWeightFix = normalWeight * 1.1;
		    mercuryWeight = normalWeight + mercuryWeightFix; 
		    venusWeight = normalWeight + venusWeightFix;
		    jupiterWeight = normalWeight + jupiterWeightFix;
		    saturnWeight = normalWeight + saturnWeightFix;
			 System.out.println(); //Necessary to separate the section for easy reading
		
		    //The program will now display the calculations to the screen
		    System.out.println("Your weight in Mercury is:  " + mercuryWeight);
          System.out.println("Your weight in Venus is:  " + venusWeight);
		    System.out.println("Your weight in Jupiter is:  " + jupiterWeight);
		    System.out.println("Your weight in Saturn is:  " + saturnWeight);
			 System.out.println();
			
			 //The user will now be asked if he/she wants to do it again
			 System.out.println ("Would you like to repeat "
			                    + "the process with a different weight?");
			 System.out.println( "Please enter Y for Yes or N for No: ");
			 input = keyboard.next();
			 repeat = input.charAt(0);					  
		
		 }while ( repeat == 'Y' || repeat == 'y');
		
	}
}
		
				
