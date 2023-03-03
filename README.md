# scanner
scanner task
task 1
class Main{
	public static void main(String[] args){


Team t1 =new Team("superman");
Team t2 =new Team("wonderwoman");
Team t3 =new Team("spiderman");
Team t4 =new Team("avengers");
Team t5 =new Team("thor");
t1.setRank(10);
t2.setRank(5);
t3.setRank(3);
t4.setRank(8);
t5.setRank(9);

System.out.println(t1.toString());
System.out.println(t2.toString());
System.out.println(t3.toString());
System.out.println(t4.toString());
System.out.println(t5.toString());


}
}
-----------------------------------------------------------------------------------------------------------------------------------------------
class Team{

private String nameTeam;
private int rank;
private String nameOfPlayers;

public Team (String nameTeam){
	this.nameTeam= nameTeam;
}

public void setRank(int rank
){
this.rank = rank;


}



public String toString (){


String s = "Hold :" + this.nameTeam + "rank : " + this.rank ;

return s;
}


}
--------------------------------
task 2
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.println("Please type your name");
        String name = scan.nextLine();
        System.out.println("Please type your age");
        int age = scan.nextInt();
        System.out.println("Your name is " + name + " and you are " + age + " years old.");
        int retire = 67- age ;
        System.out.println("you will retire after:"+ retire );
     



    }
}
-------------------------------------------------------------------------------------------------------------------------------------------------------
task 4 and task 5 
import java.util.ArrayList;

public class Main {

    public static void main(String[] args) {

        ArrayList<String> actions = new ArrayList<String>();
        actions.add("start game");
        actions.add("resume game");
        actions.add("pause game");
        actions.add("end game");
        System.out.print(actions.get(2));

        GameMenu menu = new GameMenu(actions);
        menu.displayMenu();

        String response = menu.getAction();
        System.out.println("user choice" + response);
        int userChoice = Integer.parseInt(response);
        doAction(userChoice);
        }


    public static void doAction(int action) {
        switch (action) {
            case 1:
                System.out.println("Starting the game now");
                break;
            case 2:
                System.out.println("Fetching previously saved game data");
                break;
            case 3:
                System.out.println("Game paused");
                break;
            case 4:
                System.out.println("Ending game");
                break;
            default:
                System.out.println("Invalid action selected");
                break;
        }
    }
}

------------------
import java.util.ArrayList;
import java.util.Scanner;

public class GameMenu{
	
private  ArrayList<String> actions= new ArrayList<String>();


public GameMenu( ArrayList<String> actions){

this.actions= actions ;
}






public  void displayMenu(){
for (String s: actions){
System.out.println(s);


}

}

public String getAction(){

	//System.out.println("Type a number to choose an action");
    Scanner scan = new Scanner(System.in);
    String choice = scan.nextLine();
    return choice;
   
   }


}


