# adventure-game-in-forest-river-and-village
This is a text-based game that offers players an interactive storytelling experience through a series of choices. Players navigate through different scenarios, make decisions, and explore various outcomes.
forest_art = '''
      ,@@@@@@@,
  ,,,.   ,@@@@@@/@@,  .oo8888o.
&%%&%&&%,@@@@@/@@@@@@,8888\88/8o
%%%%%&&%@@@@@@/@@\@@@,@@\88/88888
%%%%%&&%@@@@@@/@@\@@@,    |88|
+%%&&%&@@@@@@/@@@@@@\,   /88/
 %&&%&&@@@@@/@@@@@@@o\  / o8/
  %&&&%&@@/@@@ ooo\8888/    88/
    %&&/ \8888/    \8/    88/
     &/   \8/    \8/    88/
         -8/    -8/    88/
          -/    -/    88/
           /    /    88/
          /    /    88/
         /    /    88/
      __/   /    8/
      (,__ /    
'''

cave_art = '''
      ___
     /   \\
    /_____\\
   (  (_)  )
   | /(_)\ |
   |/_____\\|
   (  (_)  )
   | /(_)\ |
   |/_____\\|
  /_________\\
'''

river_art = '''
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
'''

def game():
    print("Welcome to the Adventure Game!")
    print("You find yourself in a dark forest. What do you do?")

    while True:
        print("1. Walk deeper into the forest")
        print("2. Search for food")
        print("3. Climb a tree")
        print("4. Quit")

        choice = input("Enter your choice: ")

        if choice == "1":
            print(forest_art)
            print("As you walk deeper, you encounter a mysterious cave.")
            explore_cave()
        elif choice == "2":
            print("You find some berries to eat, but they taste strange.")
            game_over("You feel dizzy and fall asleep.")
        elif choice == "3":
            print("From the tree, you spot a hidden path leading to a river.")
            cross_river()
        elif choice == "4":
            print("Thanks for playing!")
            break
        else:
            print("Invalid choice. Please select a valid option.")


def explore_cave():
    print("Inside the cave, you find a chest filled with gold coins!")
    print("What do you want to do?")

    while True:
        print("1. Take the coins")
        print("2. Leave the cave")

        choice = input("Enter your choice: ")

        if choice == "1":
            print(cave_art)
            print("As you reach for the coins, the cave entrance collapses!")
            game_over("You are trapped inside the cave.")
        elif choice == "2":
            print("You leave the cave and continue your journey.")
            break
        else:
            print("Invalid choice. Please select a valid option.")


def cross_river():
    print(river_art)
    print("You successfully cross the river and arrive at a peaceful village.")
    print("What do you want to do?")

    while True:
        print("1. Explore the village")
        print("2. Rest at the inn")
        print("3. Return to the forest")

        choice = input("Enter your choice: ")

        if choice == "1":
            print("The villagers are friendly and offer you a place to stay.")
            game_over("You decide to settle in the village and live happily ever after.")
        elif choice == "2":
            print("After a good rest, you continue your adventure.")
            break
        elif choice == "3":
            print("You return to the forest, ready for more challenges.")
            game()
        else:
            print("Invalid choice. Please select a valid option.")


def game_over(message):
    print(message)
    print("Game over.")


# ASCII art for forest, cave, and river


def display_art(art):
    print(art)


def start_game():
    display_art(forest_art)
    print("You find yourself in a dark forest. What do you do?")
    game()


# Start the game
start_game()
