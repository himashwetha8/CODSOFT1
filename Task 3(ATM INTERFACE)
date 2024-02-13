import java.util.Scanner;

class BankAccount{
    private int balance;

    public BankAccount(int initialAmount){
        this.balance=initialAmount;
    }

    public int balance(){
        return balance;
    }
    public void deposit(int amount){
        if (amount>0){
            balance+=amount;
            System.out.println("Deposit of "+amount+" Rs was successful");
        }else{
            System.out.println("Invalid entery!. Please choose a number above 0");
        }
    }

    public void withdraw(int amount){
        if (amount>0 && amount<=balance){
            System.out.println("withdraw successful of "+amount+"Rs ");
            balance-=amount;
        }else{
            System.out.println("Invalid Entery!!. Insuffecient balance or neagative value entered");
        }
    }
}

class ATM{

    private BankAccount account;
    public ATM(BankAccount account){
        this.account=account;
    }

        public void display(){
            System.out.println("Select option");
            System.out.println("1.Check Balance");
            System.out.println("2.Deposit");
            System.out.println("3.withdraw");
            System.out.println("4.Exit");
        }
        public void run(){
            Scanner sc=new Scanner(System.in);
            int option;
            do{
                display();
                System.out.println("Pick an option");
                option=sc.nextInt();

                switch(option){
                    case 1:
                        System.out.println("Current balance"+account.balance());
                        break;
                    case 2:
                        System.out.println("Enter amount to deposit");
                        int depositAmount=sc.nextInt();
                        account.deposit(depositAmount);
                        break;
                    case 3:
                        System.out.println("Enter amount to withdraw");
                        int withdrawAmount=sc.nextInt();
                        account.withdraw(withdrawAmount);
                        break;
                    case 4:
                        System.out.println("Thanks for working with XYZ Bank");
                        break;
                    default:
                        System.out.println("Invalid entry");
                }

            }while(option!=4);
            sc.close();;
        }
    }

    public class Main {

        public static void main(String[] args){
            Scanner sc=new Scanner (System.in);
            BankAccount userAccount=new BankAccount(50000);
            ATM atm= new ATM(userAccount);
            System.out.println("Enter your PIN");
            int pin=sc.nextInt();
            if (pin==1234){
                atm.run();
            }else{
                System.out.println("Wrong pin");
            }
            
        }
    
}
