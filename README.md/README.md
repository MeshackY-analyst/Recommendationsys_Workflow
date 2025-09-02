# 🛒 Product Recommender Workflow (n8n)

## 📌 Overview
This project is a **Product Recommender System** built using **n8n** and **Google Sheets**.  
It allows users to select their **preferred category** and **budget**, then recommends suitable products from a product catalog.  
The recommendations are displayed in a **carousel format** (JSON output).

---

## ⚙️ Workflow Components

1. **Form Trigger (PickBuddy)**
   - Collects user details (Name, Email, Category, Budget).

2. **Append Row in Google Sheets**
   - Saves user input into a **Customer Record Sheet**.

3. **Get Rows from Google Sheets**
   - Reads the product catalog (`Train_data.xlsx`) containing product details.

4. **If Node (Filter Logic)**
   - Filters products by **Category** and **Budget**.

5. **Code Node (Carousel Formatter)**
   - Formats matching products into a **carousel JSON output** with:
     - Title → Product Name
     - Subtitle → Category & Price
     - Image → Product Image URL
     - Button → "View Product"

6. **Delete Rows or Columns (Optional)**
   - Cleans data if no matches are found.

---

## 📂 Project Files

- `My workflow 3.json` → Exported **n8n Workflow**
- `Train_data.xlsx` → Product catalog with categories, prices, and image URLs
- `README.md` → Documentation for the project

---

## 🚀 How to Use

1. Import `My workflow 3.json` into **n8n**.
2. Update Google Sheets credentials in the workflow.
3. Upload your own product data into `Train_data.xlsx`.
4. Run the workflow → Submit form → Get recommendations.

---

## 📊 Example Carousel Output

```json
{
  "type": "carousel",
  "items": [
    {
      "title": "Mechanical Keyboard az1",
      "subtitle": "Accessories | Price: $5102",
      "image_url": "https://i.postimg.cc/pl3QtJtS/Mechanical-Keyboard.jpg",
      "buttons": [
        {
          "type": "web_url",
          "url": "https://i.postimg.cc/pl3QtJtS/Mechanical-Keyboard.jpg",
          "title": "View Product"
        }
      ]
    }
  ]
}
```

---

## ✅ Deliverables

- Workflow Export (`My workflow 3.json`)
- Product Data (`Train_data.xlsx`)
- README.md (this file)

---

## 👨‍💻 Author
Developed as part of an **n8n workflow project** to demonstrate **automation + product recommendation**.
