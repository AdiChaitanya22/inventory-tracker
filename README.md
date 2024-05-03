# inventory-tracker
This code provides a basic framework for managing an inventory of products, allowing for addition, removal, updating quantity, and displaying the inventory.
* class Product:
*     def __init__(self, name, category, price, quantity):
*         self.name = name
*         self.category = category
*         self.price = price
*         self.quantity = quantity
* 
*     def __str__(self):
*         return f"{self.name} ({self.category}): ${self.price} - Quantity: {self.quantity}"
* 
* 
* class Inventory:
*     def __init__(self):
*         self.products = []
* 
*     def add_product(self, product):
*         self.products.append(product)
* 
*     def remove_product(self, product_name):
*         for p in self.products:
*             if p.name == product_name:
*                 self.products.remove(p)
*                 return True
*         return False
* 
*     def update_quantity(self, product_name, new_quantity):
*         for p in self.products:
*             if p.name == product_name:
*                 p.quantity = new_quantity
*                 return True
*         return False
* 
*     def display_inventory(self):
*         print("Inventory:")
*         for product in self.products:
*             print(product)
* 
* 
* # Example usage:
* inventory = Inventory()
* 
* # Adding products to inventory
* inventory.add_product(Product("Laptop", "Electronics", 999.99, 10))
* inventory.add_product(Product("Smartphone", "Electronics", 699.99, 20))
* inventory.add_product(Product("Headphones", "Electronics", 49.99, 30))
* 
* # Displaying inventory
* inventory.display_inventory()
* 
* # Removing a product
* inventory.remove_product("Laptop")
* 
* # Updating quantity of a product
* inventory.update_quantity("Smartphone", 15)
* 
