# Template Audit & Friction Points — Meal Planner & Grocery List

## 1. Logo Hosting Issue (Notion API)
- **Problem:** The Notion API does not support local file uploads for page icons.
- **Resolution:** Distribute `moorish_dev_logo.png` to `assets/`. User sets it as page icon manually.

## 2. Meal → Grocery Ingredient Linking
- **Problem:** A true meal-to-grocery relation would ideally let users add ingredients to a meal and auto-populate the grocery list. This is a complex many-to-many relation that the Notion API can partially create, but ingredient deduplication across meals cannot be automated.
- **Resolution:** Simplify to a direct `Meals` → `Grocery Items` relation where each grocery item is tagged to the meal it's needed for. Deduplication must be managed manually by the user.

## 3. Calorie Rollup Complexity
- **Problem:** A `Weekly Calories` Rollup requires filtering Meals by the current week's date range — this dynamic filter cannot be set automatically via the API.
- **Resolution:** Create a static Rollup that sums all meal calories (no date filter). Instruct users in `setup_guide/Setup_Guide.md` to manually apply a "This Week" filter to the Meals view.

## 4. Button Block API Limitation
- **Problem:** Notion's native Button blocks cannot be created via the public Notion API.
- **Resolution:** User must manually create `🍽️ Add Meal` and `🛒 Add Grocery Item` button blocks.

## 5. Weekly Meal Planning View
- **Problem:** A Calendar view showing meals by day requires each meal to have a `Date` property. The API can create this property, but configuring the Calendar view layout needs manual setup in the Notion UI.
- **Resolution:** Stage as a manual step in `setup_guide/Setup_Guide.md`.
