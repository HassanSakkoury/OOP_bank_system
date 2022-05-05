# OOP_bank_system
class BankAccount():
    def __init__(self):
        self.name = None
        self._ID = None
        self.pn = None
        self._balance = None
        self.email = None
        self._password = None
        print('welcome to our bank sir, please enter your information.')
        self.takeinput()
        print('account succesfully created')
    def takeinput(self):
        self.user = input('enter your name: ')
        self.email = input('enter your email: ')
        self.job = input('enter your job: ')
        self._ID = int(input('enter your ID number: '))
        self._balance = int(input('enter your balance: '))
        self._password = int(input('enter your password: '))
    def add_deposit(self, amount):
        password = int(input('enter your password: '))
        if self._password == password:
            self._balance += amount
        else:
            print('wrong password')
    def withdraw(self, amount):
        password1 = int(input('enter your password: '))
        if self._password == password1:
            if self._balance >= amount:
                self._balance -= amount
            else:
                print('not enough balance available')
        else:
            print('wrong password')
    def show_balance(self):
        password2 = int(input('enter your password: '))
        if self._password == password2:
            print('your balance is ',self._balance, ' EGP')
        else:
            print('wrong password')
