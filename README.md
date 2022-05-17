import random
 
 
num = random.randint(0, 100)
 
while True:
    user_input = int(input("Guess the number: "))
    
    if num == user_input:
        print("Congratulations! You guessed")
        break
    else:
        diff = num - user_input
        if diff > 80:
            print("Not true. The number is much larger", user_input)
        elif diff > 50:
            print("Not true. The number is more larger", user_input)
        elif diff > 30:
            print("Not true. The number is little much larger", user_input) 
        else:
            print("Not true. Almost guessed", user_input)
        
