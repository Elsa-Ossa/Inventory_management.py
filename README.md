# Inventory Management System

## Description
This is a simple Inventory Management System implemented in Python. It allows users to add, update, delete, and display products. The system is built using object-oriented programming principles, with a focus on ease of use and extensibility.

---

## Features
- Add new products to the inventory.
- Update product details (name, quantity, and price).
- Delete products from the inventory.
- Display a list of all products in the inventory.

---

## Requirements
- Python 3.x
- (Optional) Visual Studio Code (VS Code) with Python extension for development and debugging.

---

## Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-repo/inventory-management-system.git
   ```
2. **Navigate to the Project Directory**
   ```bash
   cd inventory-management-system
   ```
3. **Install Dependencies** (Optional, if additional libraries are added later):
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

1. **Run the Script**
   - Open a terminal and navigate to the project folder.
   - Execute the following command:
     ```bash
     python inventory_management.py
     ```

2. **Interact with the System**
   - The program will display messages as you add, update, delete, or display products.

3. **Example Commands**
   - Add a product:
     ```python
     inventory.add_product(1, "Laptop", 10, 1500)
     ```
   - Update a product:
     ```python
     inventory.update_product(1, quantity=12, price=1400)
     ```
   - Delete a product:
     ```python
     inventory.delete_product(2)
     ```
   - Display all products:
     ```python
     inventory.display_products()
     ```

---

## File Structure
- `inventory_management.py` - Main Python script containing the system logic.
- `README.md` - Documentation for the project.

---

## Contributing
Feel free to fork this repository and make changes. Submit a pull request if you'd like your changes to be merged.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## Contact
If you have any questions or suggestions, feel free to reach out:
- **Email**: business@oyrone.com
- **GitHub**: [Elsa-Ossa](https://github.com/Elsa-Ossa)

class Product:
    def __init__(self, product_id, name, quantity, price):
        self.product_id = product_id
        self.name = name
        self.quantity = quantity
        self.price = price

    def __str__(self):
        return f"ID: {self.product_id}, Name: {self.name}, Quantity: {self.quantity}, Price: {self.price}"


class Inventory:
    def __init__(self):
        self.products = []

    def add_product(self, product_id, name, quantity, price):
        # Check if product already exists
        for product in self.products:
            if product.product_id == product_id:
                print("Product with this ID already exists.")
                return
        new_product = Product(product_id, name, quantity, price)
        self.products.append(new_product)
        print("Product added successfully.")

    def update_product(self, product_id, name=None, quantity=None, price=None):
        for product in self.products:
            if product.product_id == product_id:
                if name is not None:
                    product.name = name
                if quantity is not None:
                    product.quantity = quantity
                if price is not None:
                    product.price = price
                print("Product updated successfully.")
                return
        print("Product not found.")

    def delete_product(self, product_id):
        for product in self.products:
            if product.product_id == product_id:
                self.products.remove(product)
                print("Product deleted successfully.")
                return
        print("Product not found.")

    def display_products(self):
        if not self.products:
            print("No products in inventory.")
        else:
            for product in self.products:
                print(product)


# Example usage
if __name__ == "__main__":
    inventory = Inventory()

    # Adding products
    inventory.add_product(1, "Laptop", 10, 1500)
    inventory.add_product(2, "Smartphone", 50, 800)

    # Displaying products
    print("\nInventory:")
    inventory.display_products()

    # Updating a product
    inventory.update_product(1, quantity=12, price=1400)

    # Displaying products after update
    print("\nUpdated Inventory:")
    inventory.display_products()

    # Deleting a product
    inventory.delete_product(2)

    # Displaying products after deletion
    print("\nFinal Inventory:")
    inventory.display_products()

