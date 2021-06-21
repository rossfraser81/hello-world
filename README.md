class Vehicle:
    # class attribute
    wheels = 4
    
    def __init__(self, make, model, fuel, cargo_capacity):
        self.make = make
        self.model = model
        self.fuel = fuel
        self.cargo_capacity = cargo_capacity
        
    def order_capacity(self):
        return self.cargo_capacity / 10
    
    def delivery_price(self):
        return self.order_capacity / 5

class Car(Vehicle):
    def cargo_capacity(self, capacity=500):
        return super().cargo_capacity(capacity=500)
    

class Van(Vehicle):
    def cargo_capacity(self, capacity=3000):
        return super().cargo_capacity(capacity=3000)
        
class Motorcycle(Vehicle):
    
    def cargo_capacity(self, capacity=10):
        return super().cargo_capacity(capacity=10)

#Overwrites class attribute for this instance
Motorcycle.wheels=2

Bike = Motorcycle("Yamaha","Katana","Petrol",10)
print(Bike.delivery_price())

CarA = Car("Ford", "Focus", "Diesel",350)
print(int(CarA.order_capacity()))        
    
