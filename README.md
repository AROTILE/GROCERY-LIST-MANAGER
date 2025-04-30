Grocery List Manager

A Python program to manage a grocery list with budget tracking.

Overview
This program allows users to create and manage a grocery list while tracking their budget. It provides options to add items to the list, display the list, and exit the program. The program ensures that the budget is not exceeded and handles exceptions for invalid inputs.

Features
- Get and track budget
- Add items to the list with price and quantity
- Display the grocery list with remaining budget
- Exit the program with final list and budget
- Exception handling for invalid inputs (e.g., negative numbers, non-numeric inputs)
- Budget exhaustion detection and notification

Requirements
- Python 3.x

Usage
1. Run the program and enter your budget when prompted.
2. Choose an option from the menu:
    - Add item to list: Enter item name, price, and quantity.
    - Display list: View the current grocery list and remaining budget.
    - Exit: Display the final list and budget, then exit the program.
3. The program will handle exceptions and budget exhaustion automatically.

Code Structure
The program consists of four main functions:

- get_budget(): Gets and validates the user's budget.
- add_item(): Adds an item to the list with price and quantity, and updates the budget.
- display_list(): Displays the current grocery list and remaining budget.
- main(): Controls the program flow and handles user input.


    "# PROJECT FOR PYTHON ESSENTIAL CLASS"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "406769e8-510c-4221-a1d9-45b90f304589",
   "metadata": {},
   "outputs": [],
   "source": [
    "# Python | Maintaining Grocery list\n",
    "### Problem Statement:\n",
    "### Make a Grocery List for supermarket shopping with name, \n",
    "### price and quantity; if the list already contains an item, then \n",
    "### only update the quantity it should not append the item name \n",
    "### again. Ask the user his/her budget initially and minus the \n",
    "### budget after adding a new item to the list. If budgets, go \n",
    "### zero/0 then no more item could be bought and if some \n",
    "### money left and user add item greater than budget left then \n",
    "### inform “over price” or any other message.\n",
    "### VALIDATION is a must."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "8408e043-1c33-48dd-9633-9badf9c8676e",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your budget:  80000\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  2\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "Grocery List:\n",
      "\n",
      "Remaining budget: 80000.0\n",
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  1\n",
      "Enter item name:  milk\n",
      "Enter item price:  1400\n",
      "Enter item quantity:  5\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Added milk to the list. Remaining budget: 73000.0\n",
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  2\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "Grocery List:\n",
      "Item: milk, Price: 1400.0, Quantity: 5\n",
      "\n",
      "Remaining budget: 73000.0\n",
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  1\n",
      "Enter item name:  apple\n",
      "Enter item price:  400\n",
      "Enter item quantity:  10\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Added apple to the list. Remaining budget: 69000.0\n",
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  2\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "Grocery List:\n",
      "Item: milk, Price: 1400.0, Quantity: 5\n",
      "Item: apple, Price: 400.0, Quantity: 10\n",
      "\n",
      "Remaining budget: 69000.0\n",
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  1\n",
      "Enter item name:  bread\n",
      "Enter item price:  1600\n",
      "Enter item quantity:  20\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Added bread to the list. Remaining budget: 37000.0\n",
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  2\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "Grocery List:\n",
      "Item: milk, Price: 1400.0, Quantity: 5\n",
      "Item: apple, Price: 400.0, Quantity: 10\n",
      "Item: bread, Price: 1600.0, Quantity: 20\n",
      "\n",
      "Remaining budget: 37000.0\n",
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  1\n",
      "Enter item name:  bag\n",
      "Enter item price:  700\n",
      "Enter item quantity:  2\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Added bag to the list. Remaining budget: 35600.0\n",
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  3\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "Grocery List:\n",
      "Item: milk, Price: 1400.0, Quantity: 5\n",
      "Item: apple, Price: 400.0, Quantity: 10\n",
      "Item: bread, Price: 1600.0, Quantity: 20\n",
      "Item: bag, Price: 700.0, Quantity: 2\n",
      "\n",
      "Remaining budget: 35600.0\n"
     ]
    }
   ],
   "source": [
    "def get_budget():\n",
    "    while True:\n",
    "        try:\n",
    "            budget = float(input(\"Enter your budget: \"))\n",
    "            if budget < 0:\n",
    "                print(\"Budget cannot be negative. Please try again.\")\n",
    "            else:\n",
    "                return budget\n",
    "        except ValueError:\n",
    "            print(\"Invalid input. Please enter a valid number.\")\n",
    "\n",
    "def add_item(grocery_list, budget):\n",
    "    name = input(\"Enter item name: \")\n",
    "    while True:\n",
    "        try:\n",
    "            price = float(input(\"Enter item price: \"))\n",
    "            if price < 0:\n",
    "                print(\"Price cannot be negative. Please try again.\")\n",
    "            else:\n",
    "                break\n",
    "        except ValueError:\n",
    "            print(\"Invalid input. Please enter a valid number.\")\n",
    "    while True:\n",
    "        try:\n",
    "            quantity = int(input(\"Enter item quantity: \"))\n",
    "            if quantity < 0:\n",
    "                print(\"Quantity cannot be negative. Please try again.\")\n",
    "            else:\n",
    "                break\n",
    "        except ValueError:\n",
    "            print(\"Invalid input. Please enter a valid integer.\")\n",
    "\n",
    "    total_price = price * quantity\n",
    "    if name in grocery_list:\n",
    "        if total_price <= budget:\n",
    "            grocery_list[name]['quantity'] += quantity\n",
    "            budget -= total_price\n",
    "            print(f\"Updated quantity of {name} to {grocery_list[name]['quantity']}. Remaining budget: {budget}\")\n",
    "            return budget\n",
    "        else:\n",
    "            print(\"Over price! Not enough budget to add this item.\")\n",
    "            return budget\n",
    "    else:\n",
    "        if total_price <= budget:\n",
    "            grocery_list[name] = {'price': price, 'quantity': quantity}\n",
    "            budget -= total_price\n",
    "            print(f\"Added {name} to the list. Remaining budget: {budget}\")\n",
    "            return budget\n",
    "        else:\n",
    "            print(\"Over price! Not enough budget to add this item.\")\n",
    "            return budget\n",
    "\n",
    "def display_list(grocery_list, budget):\n",
    "    print(\"\\nGrocery List:\")\n",
    "    for item, values in grocery_list.items():\n",
    "        print(f\"Item: {item}, Price: {values['price']}, Quantity: {values['quantity']}\")\n",
    "    print(f\"\\nRemaining budget: {budget}\")\n",
    "\n",
    "def main():\n",
    "    budget = get_budget()\n",
    "    grocery_list = {}\n",
    "    while True:\n",
    "        if budget <= 0:\n",
    "            print(\"Budget exhausted! Cannot add more items.\")\n",
    "            display_list(grocery_list, budget)\n",
    "            break\n",
    "        print(\"\\n1. Add item to list\")\n",
    "        print(\"2. Display list\")\n",
    "        print(\"3. Exit\")\n",
    "        choice = input(\"Enter your choice: \")\n",
    "        if choice == '1':\n",
    "            budget = add_item(grocery_list, budget)\n",
    "        elif choice == '2':\n",
    "            display_list(grocery_list, budget)\n",
    "        elif choice == '3':\n",
    "            display_list(grocery_list, budget)\n",
    "            break\n",
    "        else:\n",
    "            print(\"Invalid choice! Please try again.\")\n",
    "\n",
    "if __name__ == \"__main__\":\n",
    "    main()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 4,
   "id": "06d5d8c7-d9c5-4d74-9cd3-24db7e86d609",
   "metadata": {},
   "outputs": [
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your budget:  7000\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  2\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "Grocery List:\n",
      "\n",
      "Remaining budget: 7000.0\n",
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  1\n",
      "Enter item name:  fan\n",
      "Enter item price:  8000\n",
      "Enter item quantity:  5\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Over price! Not enough budget to add this item.\n",
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  2\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "Grocery List:\n",
      "\n",
      "Remaining budget: 7000.0\n",
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  1\n",
      "Enter item name:  stone\n",
      "Enter item price:  6098\n",
      "Enter item quantity:  7\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Over price! Not enough budget to add this item.\n",
      "\n",
      "1. Add item to list\n",
      "2. Display list\n",
      "3. Exit\n"
     ]
    },
    {
     "name": "stdin",
     "output_type": "stream",
     "text": [
      "Enter your choice:  3\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "\n",
      "Grocery List:\n",
      "\n",
      "Remaining budget: 7000.0\n"
     ]
    }
   ],
   "source": [
    "def get_budget():\n",
    "    while True:\n",
    "        try:\n",
    "            budget = float(input(\"Enter your budget: \"))\n",
    "            if budget < 0:\n",
    "                print(\"Budget cannot be negative. Please try again.\")\n",
    "            else:\n",
    "                return budget\n",
    "        except ValueError:\n",
    "            print(\"Invalid input. Please enter a valid number.\")\n",
    "\n",
    "def add_item(grocery_list, budget):\n",
    "    name = input(\"Enter item name: \")\n",
    "    while True:\n",
    "        try:\n",
    "            price = float(input(\"Enter item price: \"))\n",
    "            if price < 0:\n",
    "                print(\"Price cannot be negative. Please try again.\")\n",
    "            else:\n",
    "                break\n",
    "        except ValueError:\n",
    "            print(\"Invalid input. Please enter a valid number.\")\n",
    "    while True:\n",
    "        try:\n",
    "            quantity = int(input(\"Enter item quantity: \"))\n",
    "            if quantity < 0:\n",
    "                print(\"Quantity cannot be negative. Please try again.\")\n",
    "            else:\n",
    "                break\n",
    "        except ValueError:\n",
    "            print(\"Invalid input. Please enter a valid integer.\")\n",
    "\n",
    "    total_price = price * quantity\n",
    "    if name in grocery_list:\n",
    "        if total_price <= budget:\n",
    "            grocery_list[name]['quantity'] += quantity\n",
    "            budget -= total_price\n",
    "            print(f\"Updated quantity of {name} to {grocery_list[name]['quantity']}. Remaining budget: {budget}\")\n",
    "            return budget\n",
    "        else:\n",
    "            print(\"Over price! Not enough budget to add this item.\")\n",
    "            return budget\n",
    "    else:\n",
    "        if total_price <= budget:\n",
    "            grocery_list[name] = {'price': price, 'quantity': quantity}\n",
    "            budget -= total_price\n",
    "            print(f\"Added {name} to the list. Remaining budget: {budget}\")\n",
    "            return budget\n",
    "        else:\n",
    "            print(\"Over price! Not enough budget to add this item.\")\n",
    "            return budget\n",
    "\n",
    "def display_list(grocery_list, budget):\n",
    "    print(\"\\nGrocery List:\")\n",
    "    for item, values in grocery_list.items():\n",
    "        print(f\"Item: {item}, Price: {values['price']}, Quantity: {values['quantity']}\")\n",
    "    print(f\"\\nRemaining budget: {budget}\")\n",
    "\n",
    "def main():\n",
    "    budget = get_budget()\n",
    "    grocery_list = {}\n",
    "    while True:\n",
    "        if budget <= 0:\n",
    "            print(\"Budget exhausted! Cannot add more items.\")\n",
    "            display_list(grocery_list, budget)\n",
    "            break\n",
    "        print(\"\\n1. Add item to list\")\n",
    "        print(\"2. Display list\")\n",
    "        print(\"3. Exit\")\n",
    "        choice = input(\"Enter your choice: \")\n",
    "        if choice == '1':\n",
    "            budget = add_item(grocery_list, budget)\n",
    "        elif choice == '2':\n",
    "            display_list(grocery_list, budget)\n",
    "        elif choice == '3':\n",
    "            display_list(grocery_list, budget)\n",
    "            break\n",
    "        else:\n",
    "            print(\"Invalid choice! Please try again.\")\n",
    "\n",
    "if __name__ == \"__main__\":\n",
    "    main()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "4b5995a1-fd7a-486a-948d-bd0c672acebf",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.12.7"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}

Contributing
Feel free to modify and improve the program. Contributions and suggestions are welcome!

Author
Arotile Oluwaseun Bamitale
