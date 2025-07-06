# [Task 2] - Product Search Based on User Preferences
## EDU AI Challenge

---

### Overview

In this task, you’ll learn how to build a product filtering system using OpenAI’s function calling capabilities. Instead of manually writing filtering logic, you’ll define a function schema, describe user preferences, and let the model invoke the function with the appropriate structured arguments.

---

### 🧠 Theory

Traditional product filtering relies on conditional logic written in code. But with OpenAI’s function calling [documentation], you can hand off this logic to the model.

Function calling lets the model decide **when and how** to invoke a predefined function, using structured reasoning over both user preferences and JSON-formatted data. You define the function signature and the model fills in the arguments based on natural language input and dataset context.

This approach allows for flexible, natural filtering behavior—while keeping full control over structure, safety, and post-processing.

#### AI Techniques Used

- **OpenAI Function Calling** — Let the model select matching products and call your function with structured arguments.
- **Natural Language-to-Structure Conversion** — Translate user-friendly input like *“under $200 and in stock”* into clean, typed JSON arguments.
- **Reasoning over Datasets** — Guide the model to extract relevant products from a JSON dataset based on user intent.

---

### ✅ Task

#### Introduction

Build a **console-based product search tool** that:

- Accepts user preferences (e.g. category, max price, min rating, in-stock status) in natural language  
  _e.g., "I need a smartphone under $800 with a great camera and long battery life"_
- Calls the **OpenAI API** using **function calling**
- Searches a given dataset [products.json](src/main/resources/products.json) for matching items
- Returns the final filtered product list in **structured format**

#### Definitions

- **User Preferences**: Inputs provided by the user that define the filtering criteria for a search query. Examples include:
 - Maximum price
 - Minimum rating
 - Product category (e.g., Electronics, Fitness, Kitchen, Books, Clothing)
 - Stock availability

- **Filtering Logic**: The mechanism or algorithm used to narrow down a dataset based on user-defined conditions.  
  In this task, filtering logic must be performed via:
 - A hardcoded JSON dataset [products.json](src/main/resources/products.json)
 - User input in natural language
 - OpenAI API (no manual logic allowed)

- **Dataset**: A JSON file with structured product data. Each product contains:
 - `name`
 - `category`
 - `price`
 - `rating`
 - `in_stock`

---
 
### Example Response:
Filtered Products:

1. Wireless Headphones - $99.99, Rating: 4.5, In Stock
2. Smart Watch - $199.99, Rating: 4.6, In Stock

 You must use OpenAI’s function calling to extract and return matching products. Manual filtering logic is not allowed.

### 🔍 Verification

You must provide **all** of the following:

1. ✅ **Source code** of a working console application
2. 📘 `README.md` with detailed instructions on how to run your application
3. 📄 `sample_outputs.md` with **at least two** sample runs for different user requests
4. 📁 Solution files must be placed in the appropriate folder of your **GitHub Challenge repository**

---

### 📋 Requirements

- The app **must include calls to the OpenAI API**
- The app **must use the function calling mechanism**
- The app **must accept natural language input** from the console
- `README.md` should contain **clear and detailed** setup/run instructions
- `sample_outputs.md` must contain **at least two sample runs**
- Output must be **structured, clear, and aligned** with task requirements
- Your **OpenAI API key must NOT** be stored in the GitHub repository
 
