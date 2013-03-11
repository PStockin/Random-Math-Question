Random-Math-Question
====================
Randomaly Generates 10 Math Q's Either + or - And Scores Your Results At The End
======================================================================================
import java.util.*;

public class Maths
{
  public static void main (String[] args)
  {
// Declaration And Initialisation of variables
  	Scanner user = new Scanner(System.in);
  	Random myRandom = new Random();
  	String username;
  	int counter = 1;
  	counter = 1;
  	int answer = 0;
  	int Left = 0;
  	int Right = 0;
  	int counters = 0;
  	counters = 0;
  	int Sum ;
  	
  
//Welcome Message + Name
  	System.out.println ("Welcome To My Short Questionaire!");
  	System.out.println ("Please Answer All Questions That Are Listed");
  	System.out.println ("Please Enter Your Name: ");
  	username = user.next();
  	System.out.println ("Thank You " + username + " Lets Begin...");
  	
// Questions
  	
  	while (counter <11)
  	{
  	Left = myRandom.nextInt(11) + 8;
  	Right = myRandom.nextInt(1) + 8;
  	
//Operator
  	String operatorSwitch;
        int operator = myRandom.nextInt(2);
        
        switch (operator)
        {
        case 0: operatorSwitch= "-";
            answer = Left - Right;
            break;
        case 1: operatorSwitch= "+";
            answer = Left + Right;
            break;
        default: operatorSwitch= "";
        }  	
  	
  	  System.out.print("Q:" + counter + " " + Left + operatorSwitch + Right + " = ");
  	  Sum = user.nextInt ();
  	  operator = answer;
  			  
// Checks Answers Are Correct Or Incorrect
  	  if (operator == Sum)
  	  {
  		  System.out.print("Well Done!");
  		  counters = counters + 1;
  	  }
  	  if (operator != Sum)
  	  {
  		  System.out.print("Sorry, The Correct Answer Is " + answer);
  	  }
  	  
  	  System.out.println();
  	  counter = counter + 1;
  	}
  	
//End Of Exam
  	System.out.println("Well Done " + username + " You Have Got " + counters + "/10");
  	
  }
}
