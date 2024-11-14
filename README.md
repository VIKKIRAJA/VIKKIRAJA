
class AgriculturalRawMaterial:
    def __init__(self, material_code, category, name, quantity, unit_price):
        self.material_code = material_code  # unique material code
        self.category = category            # category of the material (seed, fertilizer, etc.)
        self.name = name                    # name of the raw material
        self.quantity = quantity            # quantity in stock
        self.unit_price = unit_price        # price per unit
        
    def __str__(self):
        return f"Material Code: {self.material_code}, Name: {self.name}, Category: {self.category}, Quantity: {self.quantity}, Unit Price: {self.unit_price}"

    def update_quantity(self, amount):
        self.quantity += amount
        return self.quantity
    
    def total_value(self):
        return self.quantity * self.unit_price


# Example usage:
material1 = AgriculturalRawMaterial('S001', 'Seed', 'Tomato Seed', 1000, 0.5)
material2 = AgriculturalRawMaterial('F001', 'Fertilizer', 'Nitrogen Fertilizer', 500, 1.2)

print(material1)
print(material2)

# Update q
