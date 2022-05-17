import random
 
 
print("Welcome to the game")
num = random.randint(0, 100)
max_tries = 15
user_tries = 0
score = 100
 
while True:
    print("\nRemaining attempts: %s" % (max_tries - user_tries))
    user_input = input("Guess the number (enter 'stop' for stop): ")
    
    if user_input == 'stop':
        print("The number was %s" % num)
        break
    
    try:
        user_input = int(user_input)
    except ValueError as ex:
        print("The hidden number must be an integer and contain only numbers," +
              "'%s' not suitable for use. Try again." % user_input)
        continue
    
    user_tries += 1
    
    if user_tries >= max_tries:
        print("The maximum number of attempts has been reached. The hidden number was %s" % num)
        break
    
    if num == user_input:
        print("Congratulations! You guessed the number.")
        print("Your score: %s" % (score * (max_tries - user_tries + 1) / (max_tries) ))
        break
    else:
        diff = num - user_input
        if diff > 70:
            print("Not true. The hidden number is much greater than %s" % user_input)
        elif diff > 50:
            print("Not true. The hidden number is greater than %s" % user_input)
        elif diff > 10:
             print("Not true. The hidden number is slightly more than %s" % user_input)
        else:
            print("Not true. Almost guessed %s" % user_input)
