Pivoting and Unpivoting in Power BI with simple explanations and real-life examples.

### **What is Pivoting and Unpivoting?**

- **Pivoting:** This transforms row values into columns.
- **Unpivoting:** This transforms columns into rows.

#### **Real-Life Example:**

Imagine you have a sales report where each column represents sales for different regions (North, South, East, West) for different product categories.

**Goal:** You want to change this report to make it easier to analyze by turning region columns into rows, or vice versa.

### **How Pivoting Works:**

1. **Starting Table:**

   Suppose you have a table like this:

   | Date       | Product Category | North | South | East | West |
   |------------|------------------|--------|-------|------|------|
   | 2024-01-01 | Bikes            | 10     | 5     | 7    | 4    |
   | 2024-01-02 | Accessories      | 8      | 12    | 3    | 9    |

2. **Pivoting Example:**

   **Goal:** Convert regions from columns to rows.

   **Steps:**
   - Select the columns for regions (North, South, East, West).
   - Go to the **Transform** tab and choose **Unpivot Columns**.

   **Result:**

   | Date       | Product Category | Region | Quantity Sold |
   |------------|------------------|--------|---------------|
   | 2024-01-01 | Bikes            | North  | 10            |
   | 2024-01-01 | Bikes            | South  | 5             |
   | 2024-01-01 | Bikes            | East   | 7             |
   | 2024-01-01 | Bikes            | West   | 4             |
   | 2024-01-02 | Accessories      | North  | 8             |
   | 2024-01-02 | Accessories      | South  | 12            |
   | 2024-01-02 | Accessories      | East   | 3             |
   | 2024-01-02 | Accessories      | West   | 9             |

   Now, you have a more analyzable format where regions are in rows, making it easier to filter or create visualizations.

### **How Unpivoting Works:**

1. **Starting Table (Unpivoted):**

   Suppose you have a table like this (after unpivoting):

   | Date       | Product Category | Region | Quantity Sold |
   |------------|------------------|--------|---------------|
   | 2024-01-01 | Bikes            | North  | 10            |
   | 2024-01-01 | Bikes            | South  | 5             |
   | 2024-01-01 | Bikes            | East   | 7             |
   | 2024-01-01 | Bikes            | West   | 4             |
   | 2024-01-02 | Accessories      | North  | 8             |
   | 2024-01-02 | Accessories      | South  | 12            |
   | 2024-01-02 | Accessories      | East   | 3             |
   | 2024-01-02 | Accessories      | West   | 9             |

2. **Unpivoting Example:**

   **Goal:** Convert regions from rows back to columns.

   **Steps:**
   - Select the Region column.
   - Go to the **Transform** tab and choose **Pivot Columns**.
   - Use "Region" as the column to pivot and "Quantity Sold" as the value to aggregate.

   **Result:**

   | Date       | Product Category | North | South | East | West |
   |------------|------------------|--------|-------|------|------|
   | 2024-01-01 | Bikes            | 10     | 5     | 7    | 4    |
   | 2024-01-02 | Accessories      | 8      | 12    | 3    | 9    |

   Now, regions are columns again, which might be useful for certain types of analysis.

### **Transpose vs. Pivot/Unpivot:**

- **Transpose**: This flips the entire table, converting rows into columns and columns into rows, but it doesn’t handle duplicates or unique values well. It’s more of a straightforward flip without any aggregation.

#### **Example of Transpose:**

If you transpose the table:

| Date       | 2024-01-01 | 2024-01-02 |
|------------|------------|------------|
| Product    | Bikes      | Accessories|
| North      | 10         | 8          |
| South      | 5          | 12         |
| East       | 7          | 3          |
| West       | 4          | 9          |

Here, the dates have become columns and product categories are now rows. This may not be useful for detailed analysis where specific metrics or dimensions are needed.

### **In Summary:**

- **Pivoting:** Turns distinct row values into columns (e.g., regions become columns).
- **Unpivoting:** Turns columns into rows (e.g., regions become rows).
- **Transpose:** Flips the entire table but may not be useful for detailed analysis as it doesn’t handle unique values well.

These tools help you reshape your data to fit different analysis needs and improve data visualization in Power BI.
