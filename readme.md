# W7D1 Breakout - The Robot Fight (Let's Get READY TO RUMBLE!)

## Requirements

- Allow any number of robots to fight
- End the game when only one robot is alive
- Robots have health and attack power
- Robots can attack other robots
- Robots under 10% health go berserk (a.k.a. do double damage)
- Each round should allow a robot to attack another robot
- Robots who are dead (i.e. <= 0 health) cannot attack

### Stretch

- Allow a robot to be controlled by the Human player (i.e. pick the target of the robot)

## Important Files

### [`main.rb`](./main.rb)

This is our entry point to the game, it instantiates a new `Game` instance and kicks off the game.

### [`game.rb`](./game.rb)

This file manages all of the game logic, including the game loop. It also coordinates with the `TurnManager` to get the right turn.

### [`turn.rb`](./turn.rb)

This file contains a single class which is just a bag of data, it holds onto the attacking robot (`attacker`), the defending robot (`defender`) and the current round number (`round`)

### [`turn_manager.rb`](./turn_manager.rb)

This class instantiates new instances of the `Turn` class for use inside of the `Game` class. It keeps track of who the next attacker should be as well as the current round number.

### [`robot.rb`](./robot.rb)

This file contains the `Robot` class and it manages everything to do with robots. It holds on to things like the robots `health`, `name` and `attack_power` statistic, and also provides an interface for the robots to fight each other.
