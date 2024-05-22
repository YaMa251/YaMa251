class Player:
    def __init__(self, name):
        self.name = name
        self.health = 100
        self.weapon = None

    def equip_weapon(self, weapon):
        self.weapon = weapon

    def shoot(self, target):
        if self.weapon:
            print(f"{self.name} feuert mit {self.weapon} auf {target}!")
        else:
            print(f"{self.name} hat keine Waffe ausgerüstet.")

class Weapon:
    def __init__(self, name, damage):
        self.name = name
        self.damage = damage

# Beispiel: Spieler und Waffen erstellen
player1 = Player("Spieler 1")
player2 = Player("Spieler 2")

sniper_rifle = Weapon("Scharfschützengewehr", 50)
mp5 = Weapon("MP5", 30)

player1.equip_weapon(sniper_rifle)
player2.equip_weapon(mp5)

player1.shoot("Gegner")
player2.shoot("Spieler 1")
