from abc import ABC, abstractmethod 

class Sensor(ABC):
    @abstractmethod
    def get_reading(self):
        pass


class PHSensor(Sensor):
    def get_reading(self):
        print("[pH Sensor] Reading: 7.2 pH (Neutral)")
my_sensor = PHSensor()



class TempSensor(Sensor):
    def get_reading(self):
        print("[Temperature Sensor] Reading: 24.5°C")
my_sensor = TempSensor()


print("--- Lab Inventory System ---")
ph = PHSensor()
print(ph.get_reading())

temp = TempSensor()
print(temp.get_reading())

print("----------------------------")


    

