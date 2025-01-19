---

# **Topsis-Harsh-102203964**

A Python package for implementing the Technique for Order of Preference by Similarity to Ideal Solution (TOPSIS) method. This method is used for multi-criteria decision-making.

---

## **Installation**

Install the package using `pip`:

```bash
pip install Topsis-Harsh-102203964
```

---

## **Usage**

### **Command-Line Interface**

After installation, you can use the `topsis` command to calculate rankings for your dataset.

#### **Command Syntax**
```bash
topsis <InputDataFile> <Weights> <Impacts> <ResultFileName>
```

- `<InputDataFile>`: Path to the input CSV file.
- `<Weights>`: Comma-separated list of weights for each criterion (e.g., `2,1,3,2,1`).
- `<Impacts>`: Comma-separated list of impacts for each criterion (`+` for positive, `-` for negative).
- `<ResultFileName>`: Path to save the output CSV file.

---

### **Input File Format**
- The input file must be a CSV with at least 3 columns.
- The **first column** should contain the names of the objects (e.g., M1, M2, ...).
- The remaining columns should contain **numeric criteria values**.

#### Example Input (`data.csv`):
```csv
Object,Criteria1,Criteria2,Criteria3,Criteria4
M1,250,16,12,5
M2,200,16,8,3
M3,300,32,16,4
M4,275,16,8,4
M5,225,32,16,2
```

---

### **Example Usage**
1. Prepare the input CSV file (e.g., `data.csv`).
2. Run the following command:

```bash
topsis data.csv 2,1,3,2,1 +,-,+,+,+ result.csv
```

3. The result will be saved in the specified output file (e.g., `result.csv`).

#### Example Output (`result.csv`):
```csv
Object,Criteria1,Criteria2,Criteria3,Criteria4,Topsis Score,Rank
Fund Name,P1,P2,P3,P4,P5,Topsis Score,Rank
M1,0.69,0.48,4.4,66.7,18.07,0.5406539104721046,4
M2,0.78,0.61,6.6,68.9,19.22,0.8121668525756994,1
M3,0.78,0.61,5.3,31.1,9.45,0.38802109858012196,7
M4,0.63,0.4,5.8,34.4,10.31,0.4644299512083332,5
M5,0.95,0.9,6.8,44.5,13.29,0.6174397741627528,3
M6,0.7,0.49,3.4,51.0,13.9,0.3370177549655649,8
M7,0.68,0.46,6.5,59.8,16.86,0.7279526954856499,2
M8,0.93,0.86,4.7,45.5,13.0,0.4185634486976432,6
```

---

## **Requirements**

This package requires the following Python libraries:
- `numpy`
- `pandas`

These dependencies are automatically installed with the package.

---

## **License**

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

