# 📘 Dictionary API with Flask

This is a simple RESTful Translator API built using **Flask** and **Pandas**. The API reads a dictionary from a `.csv` file and allows users to retrieve word definitions by making GET requests to the endpoint.

## 🛠 Features

- Built with Python and Flask
- Reads data from a CSV file (`dictionary.csv`)
- Simple and fast API response

---

## 📂 Project Structure

```text
dictionary_api/
│
├── dictionary.csv        # CSV file containing words and their definitions
├── main.py               # Flask application
├── templates/
│   └── home.html         # Home page template
└── README.md             # Project documentation
```
---

## 📄 Sample dictionary.csv format

The CSV file should contain the following columns:

```csv
word,definition
...........
...........
acid,1. A compound capable of transferring a hydrogen ion......
sun,1. Any star, especially when seen as the centre of any single solar........
...........
...........
```
---

## 🚀 Running the Project
- Run the Flask App
```bash
python main.py
```
- Then open your browser and visit:
http://127.0.0.1:5001

---
## 🔌 API Usage
Use the endpoint below to get a word's definition in JSON format:

- **Endpoint:** You can access the word definition via:
    <br>
    `GET /api/v1/<word>/`  
    <br>
    *Example:*  
    http://127.0.0.1:5000/api/v1/acid/
    <br><br>
- **Response:**  
    If the word is present in the `dictionary.csv`:
    ```json
    {
      "word": "acid",
      "definition": "1. A compound capable of transferring a hydrogen ion......"
    }
    ```
    If the word is not found:  
  
    ```json
    {
      "word": "acid",
      "definition": "1. A compound capable of transferring a hydrogen ion......"
    }
    ```
