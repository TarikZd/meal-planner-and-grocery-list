# 📖 Start Here: Meal Planner & Grocery List

Welcome to the **Meal Planner & Grocery List** by **Moorish Dev**. Plan your first week of meals in under 60 seconds.

---

## ⚡ Quick Start (60 Seconds)

1. **Duplicate this template** → Click `Duplicate` in the top-right corner.
2. **Plan a meal** → Click "🍽️ Add Meal", name it, choose a Day and Meal Type, and set the date.
3. **Build the grocery list** → Click "🛒 Add Grocery Item", name the ingredient, and link it to the meal it belongs to.
4. **Shop smarter** → In the Grocery List view (grouped by Category), work through each aisle and check items off.

---

## 🏗️ Architecture Overview

| Location | What's Here |
| --- | --- |
| **Main Dashboard** | Weekly calendar + Grocery List + Linked Views |
| **`[DB] Backend`** | Raw `Meals` and `Grocery List` databases |

---

## ✍️ Manual Setup Steps (Required)

### Step 1: Set Up the Weekly Calendar View
1. On the dashboard's Meals Linked View → `+ Add a view` → `Calendar`.
2. Set date to `Date`. Name it `📅 This Week`.
3. *(Optional)* Filter by the current week's date range.

### Step 2: Group the Grocery List by Category
1. On the Grocery List Linked View → click `Group by` → select `Category`.
2. This organizes your shopping by aisle (Produce, Protein, etc.).

### Step 3: Create Button Blocks
1. Type `/button` → Create `🍽️ Add Meal` and `🛒 Add Grocery Item`.

---

## 🎨 Customization Tips
- **Meal Prep Mode**: Filter the Grocery List to `Bought = false` for a clean shopping checklist.
- **Recipe Library**: Use the `Recipe URL` field to link to online recipes — creates a searchable recipe vault.
- **Weekly Calorie Target**: Add a formula that sums all meal calories and compares to your daily target × 7.

---

*Built by Moorish Dev | Last Updated: June 2026*
