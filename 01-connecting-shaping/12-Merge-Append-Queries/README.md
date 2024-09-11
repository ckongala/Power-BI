### Merging Queries

**What It Is:**
Merging queries in Power BI is like joining two tables in Excel using a common column. This allows you to combine information from two tables based on a shared key.

**Real-Life Example:**
Imagine you have two tables:
1. **Sales Data**: Contains sales records including order numbers, quantities, and product IDs.
2. **Product Lookup**: Contains details about products like product ID, name, and color.

You want to add product names and colors to your sales records. To do this:
1. **Merge the Sales Data with Product Lookup**: Match the product IDs in both tables.
2. **Outcome**: Your Sales Data table will now include new columns with product names and colors.

**Steps in Power BI:**
1. **Go to the Query Editor**: Click on the "Merge Queries" button.
2. **Select Tables**: Choose your Sales Data table and Product Lookup table.
3. **Choose the Key Column**: Both tables should have a common column, e.g., "Product Key".
4. **Merge**: Power BI combines rows where the Product Key matches and adds columns from Product Lookup to Sales Data.
5. **Expand Columns**: Click the double arrow icon to choose which columns to add (e.g., Product Name, Product Color).

**Visual Example:**
- **Before Merge**: Sales Data table with columns: Order ID, Product Key, Quantity.
- **After Merge**: Sales Data table now has additional columns: Product Name, Product Color.

**Important Note:** Merging adds columns, not rows. Be cautious as merging might lead to redundant data, and in some cases, using relationships between tables might be more efficient.

### Appending Queries

**What It Is:**
Appending queries is like stacking similar tables on top of each other. It combines rows from multiple tables into one table, assuming they have the same structure.

**Real-Life Example:**
You have sales data from three years:
1. **Sales Data 2020**
2. **Sales Data 2021**
3. **Sales Data 2022**

You want to combine these into a single table.

**Steps in Power BI:**
1. **Go to the Query Editor**: Click on the "Append Queries" button.
2. **Select Tables**: Choose the tables you want to append (e.g., Sales Data 2020, Sales Data 2021, Sales Data 2022).
3. **Append**: Power BI combines rows from all selected tables into one.

**Visual Example:**
- **Before Append**: Separate tables for each year.
- **After Append**: One large table with all sales data combined.

**Key Points:**
- **Same Structure Required**: All tables must have the same columns and data types.
- **Handling New Files**: If you place files in a folder and append from that folder, Power BI will automatically update the combined table when new files are added or removed.

**Common Issue:** If you delete original tables after appending, Power BI might prevent deletion because the appended table relies on them.
