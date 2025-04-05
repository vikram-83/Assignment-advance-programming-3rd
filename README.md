# Assignment-advance-programming-3rd
Bank account 
// BankAccount class implementing Cloneable interface
class BankAccount implements Cloneable {
    private int accountNumber;
    private double balance;
    private String accountHolder;
    public BankAccount(int accountNumber, double balance, String accountHolder) {
        this.accountNumber = accountNumber;
        this.balance = balance;
        this.accountHolder = accountHolder;
    }
    public int getAccountNumber() {
        return accountNumber;
    }
    public void setAccountNumber(int accountNumber) {
        this.accountNumber = accountNumber;
    }

    public double getBalance() {
        return balance;
    }
    public void setBalance(double balance) {
        this.balance = balance;
    }

    public String getAccountHolder() {
        return accountHolder;
    }

    public void setAccountHolder(String accountHolder) {
        this.accountHolder = accountHolder;
    }

    
    @Override
    protected Object clone() throws CloneNotSupportedException {
        return super.clone(); 
    }

  
    public void displayAccount() {
        System.out.println("Account Number: " + accountNumber);
        System.out.println("Account Holder: " + accountHolder);
        System.out.println("Balance: " + balance);
        System.out.println("----------------------------");
    }
}


public class BankAccountCloneDemo {
    public static void main(String[] args) {
        try {
            BankAccount object
            BankAccount original = new BankAccount(1001, 50000.0, "Rahul Bhargav");

            
            BankAccount duplicate = (BankAccount) original.clone();

          
            System.out.println("Original Account:");
            original.displayAccount();

            System.out.println("Cloned Account:");
            duplicate.displayAccount();

            cloned object
            duplicate.setAccountHolder("Sikunj User");
            duplicate.setBalance(75000.0);

            System.out.println("After modifying cloned account:");
            System.out.println("Original Account:");
            original.displayAccount();
            System.out.println("Cloned Account:");
            duplicate.displayAccount();

        } catch (CloneNotSupportedException e) {
            System.out.println("Cloning not supported: " + e.getMessage());
        }
    }
}
