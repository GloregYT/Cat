# Cat


    class Pet:

    def __init__(self, name, species="cat", age=0):
        self.name = name
        self.species = species
        self.age = age
        self.energy = 100
        self.hunger = 0
        self.happiness = 100
    def __str__(self):
        return f"{self.species.capitalize()} named {self.name}"
        
    def grow_older(self):
        """Збільшує вік тварини на 1 рік після кожної дії."""
        self.age += 1
        print(f"{self.name} стає старшим! Тепер йому {self.age} років.")

    def play(self):
        if self.energy > 20:
            self.happiness += 10
            self.energy -= 20
            self.hunger += 10
            self.grow_older()
            print(f"{self.name} грає і виглядає щасливим!")
        else:
            print(f"{self.name} занадто втомлений, щоб грати.")

    def feed(self):
        if self.hunger > 0:
            self.hunger -= 30
            self.energy += 10
            self.grow_older()
            print(f"{self.name} поїв і виглядає задоволеним!")
        else:
            print(f"{self.name} не голодний зараз.")

    def sleep(self):
        print(f"{self.name} зараз спить...")
        self.energy += 50
        self.hunger += 10
        self.grow_older()

    def status(self):
        print(f"Ім'я: {self.name}, Вид: {self.species}")
        print(f"Вік: {self.age} років")
        print(f"Рівень енергії: {self.energy}")
        print(f"Голод: {self.hunger}")
        print(f"Щастя: {self.happiness}")

    # Приклад використання класу
    my_pet = Pet("Барсик", species="cat", age=2)

    my_pet.status()  # Перевірка стану тварини
    my_pet.play()    # Граємо з тваринкою
    my_pet.feed()    # Годуємо
    my_pet.sleep()   # Спить
    my_pet.status()  # Перевіряємо стан знову


Ім'я: Барсик, Вид: cat
Вік: 2 років
Рівень енергії: 100
Голод: 0
Щастя: 100
Барсик стає старшим! Тепер йому 3 років.
Барсик грає і виглядає щасливим!
Барсик стає старшим! Тепер йому 4 років.
Барсик поїв і виглядає задоволеним!
Барсик зараз спить...
Барсик стає старшим! Тепер йому 5 років.
Ім'я: Барсик, Вид: cat
Вік: 5 років
Рівень енергії: 140
Голод: -10
Щастя: 110
