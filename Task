# Доработаем задачи 5-6. Создайте класс-фабрику.
# Класс принимает тип животного (название одного из созданных классов)
# и параметры для этого типа.
# Внутри класса создайте экземпляр на основе переданного типа и
# верните его из класса-фабрики

class Animal():
    def __init__(self, name, age):
        self.__name, self.__age = name, age

    def get_name(self):
        return self.__name

    def get_age(self):
        return self.__age


class Fish(Animal):
    def __init__(self, name, age, color):
        super().__init__(name, age)
        self.__color = color

    def get_sprecific(self):
        return self.__color


class Mammal(Animal):
    def __init__(self, name, age, wool):
        super().__init__(name, age)
        self.__wool = wool

    def get_sprecific(self):
        return self.__wool


class Bird(Animal):
    def __init__(self, name, age, feather):
        super().__init__(name, age)
        self.__feather = feather

    def get_sprecific(self):
        return self.__feather


class AnimalFactory:
    def create_animal(self, animal_type, name, age, **kwargs):
        if animal_type == "mammal":
            return Mammal(name, age, **kwargs)
        elif animal_type == "bird":
            return Bird(name, age, **kwargs)
        elif animal_type == "fish":
            return Fish(name, age, **kwargs)
        else:
            raise ValueError("Invalid animal type")


factory = AnimalFactory()

mammal = factory.create_animal("mammal", "Zuza", 5, wool="Camel")
print(f"{mammal.get_name()}, {mammal.get_age()}, {mammal.get_sprecific()}")
bird = factory.create_animal("bird", "Black Еуеs", 7, feather="Black")
print(f"{bird.get_name()}, {bird.get_age()}, {bird.get_sprecific()}")
fish = factory.create_animal("fish", "Nemo", 1, color="Orange")
print(f"{fish.get_name()}, {fish.get_age()}, {fish.get_sprecific()}")
