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
- **GitHub**: [YourGitHubProfile](https://github.com/your-github-profile)
