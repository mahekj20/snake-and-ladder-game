# snake-and-ladder-game
A simple Python snake and ladder game with random dice roll 

#Snake and Ladder 
logo="""
 ____              _                          _   _              _     _             ____        
/ ___| _ __   __ _| | _____    __ _ _ __   __| | | |    __ _  __| | __| | ___ _ __  | __ ) _   _ 
\___ \| '_ \ / _` | |/ / _ \  / _` | '_ \ / _` | | |   / _` |/ _` |/ _` |/ _ \ '__| |  _ \| | | |
 ___) | | | | (_| |   <  __/ | (_| | | | | (_| | | |__| (_| | (_| | (_| |  __/ |    | |_) | |_| |
|____/|_| |_|\__,_|_|\_\___|_ \__,_|_| |_|\__,_| |_____\__,_|\__,_|\__,_|\___|_|    |____/ \__, |
/ ___|  __ _ _ __ ___   ___| | __                                                          |___/ 
\___ \ / _` | '_ ` _ \ / _ \ |/ /                                                                
 ___) | (_| | | | | | |  __/   <                                                                 
|____/ \__,_|_| |_| |_|\___|_|\_\                                                                
"""
print(logo)
r=random.randint(1,9)
print(r)
list_friends=["mahek","harry","potter"]
print(random.choice(list_friends))
snakes={26:6,30:11,42:16,75:8,82:58,89:70,97:44}
ladders={2:55,13:27,31:67,38:65,60:62,69:87,76:95}
position=0
while True:
  roll=input("Enter 'r'  to roll the dice: ").lower()
  if roll=='r':
    dice=random.randint(1,6)
    print(f"You rolled a dice {dice} 🎲")
    if position+dice<=100:
      position+=dice
    print(f"You are in position: {position}")
    print("-- -- -- -- -- --")
    if position in ladders.keys():
      position=ladders[position]
      print(f"Hurry! U have Just climed a Ladder!!!! Now you stand at:🎢")
    if position in snakes.keys():
      position= snakes[position]
      print(f"Alas!! You are Bitten by a Snake!!! Now you stand at: {position} 🐍")
    if position== 100:
      print("WOHOO.YOU WON!!!🥰")
      break
  else:
    print("Kindly stick to the rules.Please enter 'r'")
    break
