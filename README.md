# Finance-calculator-
# This project, named "finance_calculators," is a Python program that serves as a financial calculator tool. It offers two main functionalities: an investment calculator and a home loan repayment calculator. 
import math
def show_calculation_menu():
    print("Welcome, which calculation would you like to choose:")
    print("1. Investment - To calculate the amount of interest you'll earn on your investment")
    print("2. Bond - To calculate the amount you'll have to pay on a home loan")
    

def calculation_main ():
    show_calculation_menu()
    calculation_menu = input("Enter either 'Investment' or 'Bond' from the menu above to proceed:").lower()
    
    if calculation_menu == "investment":
        print("You have chosen investment.")
        P = float(input("Enter the money you are depositing:"))
        R = float(input("Enter your interest rate:")) 
        T = int(input("Enter the number of years the investment is for:"))
        interest =  input("Would you like a simple or compound interest:").lower()
        
        if interest == "compound":
            compound_amount = P * math.pow((1+R),T)
            print(f"The total amount after {T} years will be: {compound_amount:.2f}.")
        elif interest == "simple":
             simple_amount = 𝑃 * (1 + R * T)
             
              
             print(f"The total amount after {T} years will be: {simple_amount:.2f}.")
    
    elif calculation_menu == "bond":
       print("You have chosen Bond.")
       P = float(input("Enter the present value of the house:"))
       I = float(input("Enter the interest rate:")) / 12 / 100
       N = int(input("number of months are you taking to repay the bond:"))
       bond_repayment = (i * P)/(1 - (1 + I)**(-N))
       print(f"Your monthly bond repayment will be: {bond_repayment:.2f}")

       
     
    else:
       print("invalid character. Please enter 'Investment' or 'Bond' calculation to proceed")

calculation_main()
