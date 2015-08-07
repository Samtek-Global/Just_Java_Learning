// Игра угадай число... 
import java.util.Scanner;

public class Probnik {
	

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner scn = new
		Scanner(System.in);
		int rand;
		rand = (int) (Math.random()*100);
		System.out.println("Введите любое число");
		
		int cicle,game_end=0;
		
		for (cicle=0;cicle<999999;cicle++)
		{
			String user_str = scn.next();
			int user_chislo=Integer.parseInt(user_str);
			if (rand == user_chislo) 
			System.out.println("Тыц! Тыдыц! Вы победитель!");
			else 
			{
			if (rand > user_chislo) System.out.println("Число введённое вами, меньше загаданного числа...");
			if (rand < user_chislo) System.out.println("Число введённое вами, больше загаданного числа...");
			
			game_end++;
			    if (game_end==7)
			    {
			    	game_end=0;
			    	rand = (int) (Math.random()*100);
			    System.out.println("Игра окончена... Вы проиграли");
			    System.out.println("Хотите начать новую игру?");
			    System.out.println("Введите 'exit' для выхода, оставьте пустую строку, и дважды нажмите Enter для начала новой игры");
			    
			    String endgamestr = scn.next();
			         if (endgamestr.equals ("exit") ) break;
			    }
			}
		}
		}

}


=============================================



