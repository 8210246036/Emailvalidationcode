email = input("enter your email:")  # w@g.in  , rajnishhit@gmail.com
k = 0
j = 0
d = 0

if len(email) >= 6:  # 1
    if email[0].isalpha():  # 2
        if ("@" in email) and (email.count("@") == 1):  # 3
            if (email[-4] == ".") ^ (email[-3] == "."):  # 4
                for i in email:
                    if i == i.isspace():  # 5
                        k = 1
                    elif i.isalpha():
                        if i == i.upper():  # 5
                            j = 1
                    elif i.isdigit():
                        continue
                    elif i == "_" or i == "@" or i == ".":
                        continue
                    else:
                        d = 1

                if k == 1 or j == 1 or d == 1:
                    print("wrong email 5", "k==", k, "j==", j, "d==", d)

                else:
                    print("right email")
            else:

                print("wrong email 4")
        else:
            print("wrong email 3")
    else:
        print("wrong email 2")
else:
    print("worng email 1")

