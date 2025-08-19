# redesigned-sniffle
Banking application in oops 
public class Account {
    private String number;
    private double balance;
    private String name;
    private String email;
    private String phoneNumber;
    public Account(String number, double balance, String name, String email, String phoneNumber) {
        this.number = number;
        this.balance = balance;
        this.name = name;
        this.email = email;
        this.phoneNumber = phoneNumber;
    }
    public void depositMoney(double depositAmount) {
        this.balance += depositAmount;
        System.out.println("Deposit successful. Balance is " + this.balance);
    }
    public void withdrawMoney(double withdrawAmount) {
        if (this.balance - withdrawAmount < 0) {
            System.out.println("Withdraw unsuccessful. Only " + this.balance + " is available.");
        } else {
            this.balance -= withdrawAmount;
            System.out.println("Withdraw successful. Current balance is " + this.balance);
        }
    }
    public static void main(String[] args) {
        Account abhayAccount= new Account("1000116569", 0.0, "abhay", "abhay@gmail.com", "9347528821");
        System.out.println("acoount number:1000116569XXXXXXXXX");
        System.out.println("acoount name:abhay");
        System.out.println("acoount emali:abhay@gmali.com");
        abhayAccount.depositMoney(20000);
        abhayAccount.withdrawMoney(1000);

    }
}
