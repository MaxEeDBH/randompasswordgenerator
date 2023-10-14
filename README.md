# randompasswordgenerator
# This is a Python code that lets you create a strong password with a combination of letters, numbers and special characters. 

numbers=['0','1','2','3','4','5','6','7','8','9']
letters = ['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t',
           'u','v','w','x','y','z','A','B','C','D','E','F','G','H','I','J','K','L','M','N',
           'O','P','Q','R','S','T','U','V','W','X','Y','Z']
special= ['!','@','#','$','%','^','&','&','*','(',')']

lenText = int(input("How many characters: "))
lenNum = int(input("How many numbers: "))
lenSpecial = int(input("How many special characters: "))

password_list=[]

for char in range (1,lenText+1):
    password_list.append(random.choice(letters))

for char in range (1,lenNum+1):
    password_list.append(random.choice(numbers))

for char in range (1,lenSpecial+1):
    password_list.append(random.choice(special))

random.shuffle(password_list)

password = ""
for char in password_list:
    password += char

print ("Your password is ",password)
