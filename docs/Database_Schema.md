# 🗄️ Database Schema: Meal Planner & Grocery List

---

## Database 1: Meals

| Property Name | Type | Purpose |
| --- | --- | --- |
| **Meal Name** | `Title` | e.g., "Chicken Stir Fry", "Overnight Oats". |
| **Day** | `Select` | `Monday` through `Sunday`. |
| **Meal Type** | `Select` | `Breakfast`, `Lunch`, `Dinner`, `Snack`. |
| **Date** | `Date` | Specific date planned for this meal. |
| **Calories (kcal)** | `Number` | Estimated calorie count. |
| **Prep Time (min)** | `Number` | Estimated preparation time. |
| **Status** | `Select` | `Planned`, `Prepped`, `Cooked`, `Skipped`. |
| **Ingredients** | `Relation` | Links to the Grocery List database. |
| **Recipe URL** | `URL` | Link to the recipe source. |
| **Notes** | `Text` | Dietary notes, substitutions, etc. |

## Database 2: Grocery List

| Property Name | Type | Purpose |
| --- | --- | --- |
| **Item** | `Title` | e.g., "Chicken Breast", "Olive Oil". |
| **Meal** | `Relation` | Links to the Meals database (which meal needs this item). |
| **Category** | `Select` | `Produce`, `Protein`, `Dairy`, `Pantry`, `Frozen`, `Bakery`. |
| **Quantity** | `Text` | e.g., "500g", "2 cans", "1 dozen". |
| **Bought** | `Checkbox` | Mark when purchased. |
| **Estimated Cost (£)** | `Number` | Rough price estimate. |
| **Store** | `Select` | Where to buy (e.g., `Tesco`, `Amazon Fresh`, `Any`). |
| **Priority** | `Select` | `Essential`, `Optional`. |

## Architectural Notes
- **Vault Method:** Both databases reside in `[DB] Backend`. Dashboard uses Linked Views.
- **Recommended Views:** Weekly Meal Plan (Calendar, by Date), Shopping List (Table grouped by Category, filtered Bought = false), Meal Ideas (Gallery for recipe inspiration).
