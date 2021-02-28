# Demo
class Atm:
    balance=5000



    def deposite(self,amount):
        self.amount=amount
        self.balance=self.balance+self.amount
        print(f"Your account balance is {self.balance}")

    def Login(self,pin):
        if pin==1111:
            return True
        else:
            return False

    def Withdraw(self,amount):
        if self.amount>self.balance:
            print("Your balance is low")
        else:
            self.balance=self.balance-self.amount
            print(f"your account balance is {self.balance}")

    def Balance_check(self):

        print(f"your current balance is{self.balance}")

if __name__ == '__main__':
    obj=Atm()
    flag=False
    for i in  range(1,4):
        if obj.Login(int(input("enter pin code"))):
            flag=True
            break
    if flag:
        while True:
            print("Enter your choice\n"
                  "1.credit\n"
                  "2.Withdraw\n"
                  "3.Balance check\n"
                  "4.Exit")
            user_choice=int(input())
            if user_choice==1:
                obj.deposite(int(input("after credit total amount")))
                obj.Balance_check()

            elif user_choice==2:
                amount=int(input("enter amount for withdraw"))
                obj.Withdraw(amount)

            elif user_choice==3:

                obj.Balance_check()


            elif user_choice==4:
                exit()



    else:
        print("your pin code attempt has been completed")





