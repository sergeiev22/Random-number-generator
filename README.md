import random
 
 
num = random.randint(0, 100)
 
while True:
    user_input = int(input("Guess the number: "))
    
    if num == user_input:
        print("Congratulations! You guessed")
        break
    else:
        diff = num - user_input
        if diff > 60:
            print("Not true. The number is much larger", user_input)
        elif diff > 30:
            print("Not true. The number is larger", user_input)
        elif diff > 10:
            print("Not true. The number is little much larger", user_input)
        
