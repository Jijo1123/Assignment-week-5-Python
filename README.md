Assignment 1

# Superhero class
class Superhero:
    def __init__(self, name, alias, superpower, strength_level):
        self.name = name
        self.alias = alias
        self.superpower = superpower
        self.strength_level = strength_level

    def introduce(self):
        print(f"I am {self.alias}, also known as {self.name}!")
        print(f"My superpower is {self.superpower}.")

    def use_power(self):
        print(f"{self.alias} is using their {self.superpower}!")

    def check_strength(self):
        if self.strength_level > 80:
            print(f"{self.alias} is at peak strength!")
        else:
            print(f"{self.alias} needs to train more.")

# Subclass for Villains inheriting from Superhero
class Villain(Superhero):
    def __init__(self, name, alias, superpower, strength_level, evil_plan):
        super().__init__(name, alias, superpower, strength_level)
        self.evil_plan = evil_plan

    # Overriding the introduce method
    def introduce(self):
        print(f"I am {self.alias}, the villain! My plan is {self.evil_plan}.")

    def execute_plan(self):
        print(f"{self.alias} is executing their evil plan: {self.evil_plan}!")

# Creating objects and demonstrating encapsulation
hero = Superhero("Clark Kent", "Superman", "Super Strength", 95)
villain = Villain("Lex Luthor", "Lex", "Genius Intellect", 70, "World Domination")

# Hero actions
hero.introduce()
hero.use_power()
hero.check_strength()

# Villain actions
villain.introduce()
villain.execute_plan()
villain.check_strength()


Assignment 2

# Base class
class Vehicle:
    def move(self):
        raise NotImplementedError("This method should be overridden by subclasses")

# Subclasses implementing polymorphism
class Car(Vehicle):
    def move(self):
        print("The car is driving on the road. 🚗")

class Plane(Vehicle):
    def move(self):
        print("The plane is flying in the sky. ✈️")

class Boat(Vehicle):
    def move(self):
        print("The boat is sailing on the water. 🚤")

# Testing polymorphism
vehicles = [Car(), Plane(), Boat()]

for vehicle in vehicles:
    vehicle.move()
    
