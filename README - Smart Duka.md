# Smart Duka Retail Sales & Customer Intelligence 


---



**Duka Smart Electronics** is a growing Kenyan retailer selling phones, laptops, accessories, TVs and
home appliances in ten towns — from Nairobi and Mombasa to Meru and Machakos. It has been trading
since January 2025 and keeps every order in a database.

Management has questions. *Who are our best customers? Which products actually make money? Are sales
growing? Which customers have stopped buying?* Nobody has looked at the data properly yet.

You have just joined as a **Junior Data Analyst**. Your job this week: set up the company's database,
load its data, answer 46 business questions in SQL, and tell management what you found.

All the people and companies in this data are fictional.




### `customers` — one row per customer (150 rows)

| Column | Type | Meaning |
|---|---|---|
| `customer_id` | INTEGER, **primary key** | Unique customer number |
| `customer_name` | VARCHAR(100), not null | Full name |
| `gender` | VARCHAR(10) | `Male` / `Female` |
| `city` | VARCHAR(50) | One of ten Kenyan towns |
| `registration_date` | DATE | When they joined |
| `customer_segment` | VARCHAR(20) | `Retail`, `Corporate` or `VIP` |

### `orders` — one row per order (800 rows)

| Column | Type | Meaning |
|---|---|---|
| `order_id` | INTEGER, **primary key** | Unique order number |
| `customer_id` | INTEGER, **foreign key → customers** | Who placed it |
| `order_date` | DATE, not null | When it was placed |
| `product_name` | VARCHAR(100) | What was bought |
| `product_category` | VARCHAR(50) | `Electronics`, `Accessories`, `Home Appliances`, `Computing`, `Mobile Phones` |
| `quantity` | INTEGER (> 0) | Units in the order |
| `unit_price` | NUMERIC(12,2) | Selling price per unit, KSh, **before** discount |
| `cost_price` | NUMERIC(12,2) | What one unit cost the company, KSh |
| `discount` | NUMERIC(5,2) (0–100) | Discount **percentage** — `10` means 10% off |
| `payment_method` | VARCHAR(30) | `M-Pesa`, `Cash`, `Card`, `Bank Transfer` |
| `order_status` | VARCHAR(20) | `Completed`, `Pending`, `Cancelled` |


## Insights 
Revenue vs profit by category, both mertics seem to be on the positive sides with some months doing poorly comparing to the rest.
City concentration. Nairobi seems to have the most ordrs and revenue as well.
