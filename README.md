# Simple Inventory Management for Beginner

A beginner-friendly inventory management desktop app for a small sari-sari store, built with Java Swing in Apache NetBeans. It shows how to build a simple CRUD (Create, Read, Update, Delete) program with a graphical interface, using a `JTable` as the inventory list.

The window title is **Evelyn's Sari-Sari Store**.

## Features

- **Add** an item with its name, expiration date, category, price and quantity
- **Update** an existing item: click a row in the table, change the fields, then press Update
- **Delete** the selected item from the table
- **Clear** all the input fields
- **Search** the table by keyword (case-insensitive, matches any column)
- **Input checking**: a message appears if a field is empty or no category is chosen
- **Confirmation messages** after adding, updating and deleting

### Item fields

| Field | Input |
|-------|-------|
| Name | Text |
| Expiration Date | Text |
| Category | Dropdown: Canned Goods, Beverages, Cigarettes, Medicines, Biscuit, Detergent, Toiletries, Condiments |
| Price | Text |
| Quantity | Text |

## Concepts Used

- Java Swing GUI (`JFrame`, `JTextField`, `JComboBox`, `JButton`, `JTable`)
- `DefaultTableModel` for adding, editing and removing rows
- `TableRowSorter` with `RowFilter.regexFilter` for searching
- Event handling (`ActionListener`, `MouseListener`)
- `JOptionPane` dialogs for messages
- NetBeans GUI Builder (`.form` file)
- Scaling an image with `ImageIcon` for the store logo

## Project Structure

```
Simple-Inventory-Management-for-Beginner/
├── nbproject/                          NetBeans project settings
├── src/
│   └── Main/
│       ├── Simple_Inventory.java       Main program and all the logic
│       ├── Simple_Inventory.form       NetBeans GUI layout
│       └── shoppingcart-removebg-preview.png   Store logo
├── build.xml
└── manifest.mf
```

## How to Run

**NetBeans**

1. Clone the repo: `git clone https://github.com/Karumuii/Simple-Inventory-Management-for-Beginner.git`
2. In NetBeans, choose **File > Open Project** and select the cloned folder.
3. Open `src/Main/Simple_Inventory.java` and press **Shift + F6** (Run File).

**Command line**

```bash
cd Simple-Inventory-Management-for-Beginner/src
javac Main/Simple_Inventory.java
java Main.Simple_Inventory
```

## Requirements

- JDK 24 (the version set in the project settings)
- Apache NetBeans (optional, the command line also works)

## Limitations

- Items are kept only while the program is open. Closing the app clears the list, because nothing is saved to a file or database.
- Price, quantity and expiration date are plain text with no format check.

## Possible Improvements

- Save and load items from a file or a database
- Check that price and quantity are numbers and that dates follow a format
- Low-stock and near-expiry warnings
