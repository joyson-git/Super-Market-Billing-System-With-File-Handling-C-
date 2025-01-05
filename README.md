Explanation of the Code
This C++ program simulates a Supermarket Billing System that allows the user to:

Add Items to the Inventory (addItem function).
Generate Bills for customers by deducting the items from the inventory (printBill function).
Exit the application.
It uses file I/O to store the inventory and modify it based on the user's operations. Here's how the program works:

Input/Output Details
1. Adding Items (addItem function):
Input:
The user enters:
Item name
Rate of the item
Quantity of the item
Output:
Writes this information into a file (D:/Bill.txt).
Displays a message: "Item Added Successfully".
2. Printing the Bill (printBill function):
Input:
The user enters:
Item name to be purchased
Quantity of the item
Output:
If the item is available in the inventory:
Displays a formatted bill line:
mathematica
Copy code
Item | Rate | Quantity | Amount
Deducts the purchased quantity from the inventory file (D:/Bill.txt).
Updates the inventory and calculates the total amount.
If the item is not available or quantity exceeds stock:
Displays "Item Not Available!" or "Sorry, [item] Ended!".
At the end:
Displays the total bill amount.
3. Exit Option (main):
Output:
Displays "Good Luck!" before exiting.
Example Run
Step 1: Adding Items
User Input:
makefile
Copy code
1 (Add Item)
Item: Apple
Rate: 10
Quantity: 50
Output:
mathematica
Copy code
Item Added Successfully
File (D:/Bill.txt) after addition:
yaml
Copy code
Apple : 10 : 50
Step 2: Generating a Bill
User Input:
mathematica
Copy code
2 (Print Bill)
Item: Apple
Quantity: 5
Output:
mathematica
Copy code
Item | Rate | Quantity | Amount
Apple      10       5       50
Total Bill ----------------- : 50
Thanks For Shopping!
File (D:/Bill.txt) after deduction:
yaml
Copy code
Apple : 10 : 45
If an item is not available:
User Input:
mathematica
Copy code
2 (Print Bill)
Item: Banana
Quantity: 10
Output:
mathematica
Copy code
Item Not Available!
Key Features of the Code
Inventory Management:

Keeps the inventory file (D:/Bill.txt) updated with the available stock.
Modifies the file dynamically when items are purchased.
File Handling:

Uses ifstream and ofstream to read from and write to files.
Handles temporary files for safe data modification.
User Interaction:

User-friendly menu-driven interface.
Allows adding items, billing, and exiting the program.
Session Persistence:

Data is saved to a file, so it remains persistent across program runs.
Issues/Improvements:
Hardcoded File Path:

The path (D:/Bill.txt) should be dynamic or relative for better portability.
Error Handling:

Proper handling for invalid inputs (e.g., non-numeric rates/quantities).
Optimization:

Instead of creating a temporary file every time, consider an in-memory inventory system with periodic file updates.
UI Enhancements:

Add better input validation and formatting for output.
Final Notes
The program demonstrates a simple inventory and billing system using file handling and OOP concepts. It is suitable for small-scale applications and can be further extended with features like:

Multiple item purchases at once.
Persistent databases (e.g., SQLite, MySQL).
Enhanced UI with frameworks like Qt or a web-based interface.
