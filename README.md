# 📚 Book Library Management Agentic AI

An intelligent AI-powered chatbot system for managing a company's book library.

## Features

✨ **Agentic AI** - Natural language processing for intuitive queries
📖 **Book Management** - Complete catalog with search and availability tracking
👥 **Employee Management** - Track employee details and borrowing history
🔄 **Borrow/Return System** - Automated tracking of book circulation
📊 **Analytics** - Library statistics and overdue book tracking
🏢 **Provider Management** - Manage book suppliers and publishers
💬 **Interactive Chatbot** - Easy-to-use command interface

## Project Structure

```
book-library-agentic-ai/
├── data/
│   ├── books.csv           # Book catalog
│   ├── employees.csv       # Employee directory
│   ├── borrowers.csv       # Borrowing records
│   └── providers.csv       # Book providers/publishers
├── src/
│   ├── __init__.py
│   ├── database_manager.py # Database operations
│   ├── agentic_ai.py      # AI agent logic
│   ├── api_server.py	   # Flask REST API
│   └── utils.py           # Shared helpers
├── config/
│   └── settings.py        # Configuration
├── main.py/api_main.py    # Entry point
├── streamlit run app.py   # UI app
└── requirements.txt       # Dependencies
```

## Installation

### Prerequisites
- Python 3.8+
- pip (Python package manager)

### Step 1: Clone or Download
```bash
cd C:\Users\akumarmishra\Documents\Accelerate_With_AI\book-library-agentic-ai
```

### Step 2: Create Virtual Environment
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash

pip install -r requirements.txt
```

### Step 4: Run the Application
```bash
python main.py
```

## Usage

### Starting the Chatbot
```bash
For cmd 
python main.py

For Chatbot
python api_main.py
streamlit run app.py
```
### Available Commands

#### Information Commands
- `help` - Show all available commands
- `tools` - List all AI tools
- `books` - Show all books
- `available` - Show available books
- `employees` - Show all employees
- `providers` - Show all providers
- `stats` - Show library statistics
- `overdue` - Show overdue books

#### Query Commands
- `search <keyword>` - Search books by title or author
- `employee <EMP_ID>` - Show employee details and books
- `history <EMP_ID>` - Show employee borrowing history

#### Action Commands
- `borrow <EMP_ID> <BOOK_ID>` - Borrow a book
- `return <EMP_ID> <BOOK_ID>` - Return a book
- `query <natural language>` - Ask AI agent a question

#### Utility Commands
- `clear` - Clear screen
- `exit` - Exit the chatbot

### Example Queries

```
📚 Library> books
# Shows all books in the library

📚 Library> available
# Shows only available books

📚 Library> search python
# Searches for books with "python" in title or author

📚 Library> employee EMP001
# Shows details of employee EMP001

📚 Library> borrow EMP001 B001
# Borrows book B001 for employee EMP001

📚 Library> overdue
# Shows all overdue books

📚 Library> query show me all programming books
# Natural language query to AI agent
```

## Data Files

### books.csv
Contains book information:
- book_id: Unique identifier
- title: Book title
- author: Author name
- isbn: ISBN number
- genre: Book category
- total_copies: Total copies in library
- available_copies: Currently available copies
- provider_id: Provider reference
- added_date: Date added to library

### employees.csv
Contains employee information:
- employee_id: Unique identifier
- name: Employee name
- department: Department
- email: Email address
- phone: Phone number
- joining_date: Joining date

### borrowers.csv
Contains borrowing records:
- borrow_id: Unique identifier
- employee_id: Employee ID
- book_id: Book ID
- borrow_date: Date borrowed
- due_date: Return due date
- return_date: Actual return date
- status: borrowed/returned

### providers.csv
Contains provider information:
- provider_id: Unique identifier
- provider_name: Publisher/supplier name
- provider_type: Type of provider
- contact_email: Email address
- phone: Phone number
- address: Physical address
- city: City
- country: Country

## Architecture

### Database Manager
Handles all database operations:
- CRUD operations for books, employees, borrowers
- Data import from CSV files
- Query execution and result formatting

### Agentic AI
AI agent with multiple tools:
- Book management tools
- Employee management tools
- Borrowing tools
- Statistics tools
- Natural language processing

### Chatbot Interface
Interactive command-line interface:
- Command parsing
- Tool execution
- Result formatting and display
- Natural language query processing

## Visual Studio Setup

### Prerequisites
- Visual Studio 2022 or later
- Python workload installed

### Steps

1. **Open Visual Studio**
   - File → Open → Folder → Select project folder

2. **Create Virtual Environment**
   - View → Terminal
   - Run: `python -m venv venv`
   - Activate: `venv\Scripts\activate`

3. **Install Dependencies**
   - Run: `pip install -r requirements.txt`

4. **Configure Python Interpreter**
   - Tools → Options → Python → Environments
   - Select your venv environment

5. **Run the Project**
   - Right-click `main.py` → Run
   - Or press F5

## Features in Detail

### 🤖 Natural Language Processing
The AI agent understands natural language queries and routes them to appropriate tools.

### 📊 Real-time Statistics
Get instant insights into library usage and book availability.

### ⏰ Due Date Tracking
Automatic tracking of due dates and overdue notifications.

### 🔍 Advanced Search
Search books by title, author, ISBN, or genre.

### 📈 Analytics
View borrowing patterns and library utilization.

## Troubleshooting

### Issue: "Module not found" error
**Solution:** Ensure virtual environment is activated and dependencies are installed
```bash
pip install -r requirements.txt
```

### Issue: Database not found
**Solution:** Database is created automatically on first run. If issues persist, delete `library.db` and restart

### Issue: CSV files not loading
**Solution:** Verify CSV files exist in the `data/` folder with correct names

## Contributing

Feel free to contribute improvements:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License - see LICENSE file for details.

## Support

For issues or questions:
- Create an issue on GitHub
- Contact the maintainer

## Version History

### v1.0.0 (Current)
- Initial release
- Basic book management
- Employee tracking
- Borrowing system
- AI chatbot interface

---

**Created with ❤️ for efficient library management**
