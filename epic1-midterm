import 'dart:io';
import 'dart:math';

var rock = '\u270A';
var paper = '\u270B';
var scissors = '\u270C';
int playerScore = 0;
int computerScore = 0;
int round = 1;

void main() 
{
    print("Round $round:");
    int move1 = playerMove();
    int move2 = computerMove();
    winner(move1, move2);
}

int playerMove()
{
  print("Papel$paper , Gunting$scissors , Bato$rock ! What's your Pick? ");
  String choice = stdin.readLineSync();
  print(" ");

  if ((choice == "Bato") || (choice == "bato") || (choice == "BATO"))
  {
      print("You chose Bato$rock");
      return 1;
  }
  else if ((choice == "Papel") || (choice == "papel") || (choice == "PAPEL"))
  { 
    print("You chose Papel$paper");
    return 2;
  }

  else if ((choice == "Gunting") || (choice == "gunting") || (choice == "GUNTING"))
  { 
    print("You chose Gunting$scissors");
    return 3;
  }

  else
  { 
    print("Invalid Input!");
    print("Try Again");
    print(" ");
    main();
  }

}

int computerMove() 
{
  Random rand = new Random();
  int move = rand.nextInt(3); 
  
  switch (move) {
    case 0:
      print("Bot chose Bato$rock");
      print(" ");
      return 1;
      break;
    case 1:
     print("Bot chose Papel$paper");
     print(" ");
     return 2;
     break;
    case 2:
     print("Bot chose Gunting$scissors");
     print(" ");
     return 3;
     break;
    default:
      break;
  }
}

void winner ( int playerMove, int computerMove)
{
    if (playerMove == computerMove)
    {
        print("It's a Tie!");
        print(" ");
        choice();
        
    }

    else if ((playerMove == 1 && computerMove == 3) || (playerMove == 2 && computerMove == 1) || (playerMove == 3 && computerMove == 2))
    {
        print("You Win!");
        print(" ");
        playerScore += 1;
        choice();
  
    }

    else
    {
        print ("Sorry, Bot won.");
        print(" ");
        computerScore += 1;
        choice();
      
    }

}

void score()
{
    int player = playerScore;
    int computer = computerScore;

    print("You - $player");
    print("Bot - $computer");
    print(" ");
}

void choice()
{ 
    print("Do you want to play another round? Yes or No?");
    String choose = stdin.readLineSync();
    print(" ");

    if ((choose == "Yes") || (choose == "yes") || (choose == "YES"))
    {
        round += 1;
        main();
    }

    else if ((choose == "No") || (choose == "no") || (choose == "NO"))
    {
        print("Final Score:");
        score();

        if (playerScore > computerScore)
        {
            print("Congratulations! You are the Winner!");
            print("Thank you for playing the game!");
        }

        else if (playerScore < computerScore)
        {
            print("Sorry. Better Luck Next time.");
            print("Thank you for playing the game!");
        }

        else
        {
            print("It's a draw game.");
            print("Thank you for playing the game!");
        }

    }

    else
    {
        print("Invalid Input!");
        print("Try Again.");
        print(" ");
        choice();
    }

}
