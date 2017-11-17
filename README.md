import java.util.*;

 public class pigLab
 {
 public static void main(String[] args)
 {
 int rolledScore = 0;
 int totalScore = 0;
 int rolledScore2 = 0;
 int totalScore2 = 0;
 final int win = 20; //
 int dice = 0;
 // int dice2 = 0;
 String input = "roll";
 String input2 = "roll";
 char repeat;

 Scanner keyboard = new Scanner(System.in);
 Scanner s = new Scanner (System.in);

 Random diceNumbers = new Random(); // allows the  dice to roll randomly
 
 while(totalScore < win && totalScore2 < win) //tells who win based off the totalScore
 {
 //Player 1's turn

 do
  {
      dice = diceNumbers.nextInt(6) + 1;
      System.out.println();
      System.out.println("You rolled: " + dice);

           if(dice == 1)
           {
               rolledScore = 0;
               System.out.println("Player 1's total is " + totalScore);
               break;
           }
           else
           {         
              rolledScore += dice;
              System.out.println("Player 1, you got a " + rolledScore + " ");
              System.out.println("Wanna roll again? enter y for yes or n for no"); //roll or stop
              input = keyboard.nextLine();
              repeat = input.charAt(0);


         if(repeat == 'n')
         {
         System.out.println("Current score: Player 1 has " + totalScore);
         System.out.println(" Player 2 has " + totalScore2);
         break;

         }
      }
  }
 while(input.equalsIgnoreCase("y") || dice != 1); 
 {             

     totalScore +=rolledScore;
 }

  if(totalScore >= win)
  {
      System.out.println("Your total Score is " + totalScore);
      System.out.println("Player 1 wins!");
      System.out.println("GAME OVER");

  }


  //player2's turn
  System.out.println();
  System.out.println("It is Player 2's turn."); 

 { do
  {
     dice = diceNumbers.nextInt(6) + 1;
      System.out.println("Player 2 rolled: " + dice); // score for player 2

      if(dice == 1)
        {
          rolledScore2 = 0;
         System.out.println("Player 2 total is " + totalScore2); // total score for Player 2
          break;             
        }
      else
      {
      rolledScore2 += dice;
      System.out.println("Player 2, you rolled a " +rolledScore2 + " ");
      System.out.println("Wanna roll again? enter y for yes or n for no"); // option to roll again
      input = keyboard.nextLine();
      repeat = input.charAt(0);


    if(repeat == 'n')
        {
    System.out.println("Current score:");
    System.out.println("Player 1 has " + totalScore);
    System.out.println(", Player 2 has " + totalScore2);
    break;
        }
    }
}  
while(input2.equalsIgnoreCase("y") && dice != 1); {

    totalScore2 += rolledScore2; // It is adding the rolled score to the total score for player 2
    

      }
 }
if(totalScore2 >= win);
  {
      System.out.println("Player 2 score is " + totalScore2);
      System.out.println("Player 2 wins!");
      System.out.println("GAME OVER"); // announcing if the the player 2's the winner
      break;
  }
 }

}
}
