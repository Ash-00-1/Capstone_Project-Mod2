# Capstone_Project-Mod2
# 🚗 Smart Parking Price Estimation System

This project implements a **smart pricing engine** for parking systems using real-time and historical data. It analyzes parking demand, location, traffic conditions, and vehicle type to dynamically calculate optimal parking prices. It features **two pricing models**:

- **Model 1**: Basic supply-demand pricing.
- **Model 2**: Demand-based pricing with traffic, queue, and vehicle intelligence.

---

## 🧰 Tech Stack

| Component       | Technology      |
|----------------|-----------------|
| Programming     | Python          |
| Data Processing | [Pathway](https://pathway.com) |
| Visualization   | Bokeh           |
| File Handling   | Pandas          |
| Data Format     | CSV, JSONL      |
| Notebook        | Google Colab / Jupyter |

---

## 📊 Architecture Diagram

![image](https://github.com/user-attachments/assets/692f17b8-11bf-4a6f-9c6c-d9e53d32d99f)

---

## 🔁 Workflow

### 🔹 Input

* `dataset.csv`: A CSV file with real-world parking logs.
* Columns include `ID`, `SystemCodeNumber`, `Capacity`, `Occupancy`, `TrafficConditionNearby`, etc.

### 🔹 Processing

* **Pathway** reads and processes the data in a **static pipeline mode**.
* **UDFs (User Defined Functions)** are used to:

  * Combine date and time into a `Datetime` field.
  * Compute prices using the chosen model.
  * Write results into a `.jsonl` file.

### 🔹 Output

* A processed `output.jsonl` or `output_model2.jsonl` file containing:

  * `ID`, `Occupancy`, `QueueLength`, `TrafficConditionNearby`, `VehicleType`, and computed `price`.
* Bokeh is used to generate interactive graphs such as:

  * Price vs Occupancy
  * Price vs Vehicle Type

---


## 🤝 Contributing

Pull requests and suggestions are welcome! For major changes, please open an issue first to discuss.

---

