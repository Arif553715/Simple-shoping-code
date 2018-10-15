# Simple-shoping-code


import re

class Sign:

    def lol(self,x):
        if x == 1:
            self.a = input("1st name:")
            self.b = input("2nd name:")
            return self.gmail()
        else:
            return
    def gmail(self):
        self.s = input("input your mail:")
        pattern = r".@gmail.com$"
        self.c = re.search(pattern,self.s)
        if self.c:
            return self.password()
        else:
            return self.gmail()

    def password(self):
        self.d = input("input your pass:")
        self.e = input("conf your pass:")
        if self.d == self.e:
            return self.sign_up()
        else:
            return self.password()

    def sign_up(self):
        if self.d == self.e:
            print("create your account")

        else:
            return self.password()

w = Sign()
w.lol(1)

t = w.s
q = w.e

#**************************************Login page*************************************************

def login():
    mail = input("Input Mail:")
    pas = input("Input password:")

    if mail == t and pas == q:
        print("login")
    else:
        return login()

login()

#**************************************Shoping page *************************************************
print("Now you are ready to shoping\n")
shoping = ["Car", "Baike", "Table", "Sokes\n"]

class Buy:
    def menu(self,d):
        p = int(input("Akon jodi tmi abar product list a jete cau tahole 0 press koro:"))
        if p == d:
            return self.pay()

    def pay(self):
        print("press, \n1 for Car 200 tk.\n2 for Baike 300 tk. \n3 for Table 400 tk. \n4 for sokes 500 tk.")
        pres = int(input("coes koro: "))
        if pres == 1:
            return self.pay1()
        elif pres == 2:
            return self.pay2()
        elif pres == 3:
            return self.pay3()
        elif pres == 4:
            return self.pay4()
        else:
            print("vul")
            return self.pay()

    def pay1(self):
        print("atar dam 200 tk\n")
        taka = int(input("takar poriman patau:\n"))
        if taka == 200:
            print("tmi ata kine felaiso")
            return self.menu(0)

        elif taka != 200:
            print("tmi 200 tk deu ny")
            return self.pay1()

    def pay2(self):
        print("atar dam 300 tk\n")
        taka = int(input("takar poriman patau:\n"))
        if taka == 300:
            print("tmi ata kine felaiso")
            return self.menu(0)

        elif taka != 300:
            print("tmi 300 tk deu ny")
            return self.pay2()

    def pay3(self):
        print("atar dam 300 tk\n")
        taka = int(input("takar poriman patau:\n"))
        if taka == 300:
            print("tmi ata kine felaiso")
            return self.menu(0)

        elif taka != 300:
            print("tmi 300 tk deu ny")
            return self.pay3()

    def pay4(self):
        print("atar dam 400 tk\n")
        taka = int(input("takar poriman patau:\n"))
        if taka == 400:
            print("tmi ata kine felaiso")
            return self.menu(0)

        elif taka != 400:
            print("tmi 400 tk deu ny")
            return self.pay4()

f = Buy()
f.pay()
