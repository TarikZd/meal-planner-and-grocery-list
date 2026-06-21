# 📋 Free Templates: Active Tasks — Meal Planner & Grocery List

This document tracks all development tasks for this template, strictly adhering to the `AGENTS.md` protocol.

- `[ ]` uncompleted | `[/]` in progress | `[x]` completed

---

## 🏃 Current Sprint

### Local Filesystem Initialization
- [x] **T0: [DESIGN] Create Local Directory Structure and Apply Logo** — *(completed 2026-06-18 by Antigravity)*
  - **Changed:** Created subdirectories and copied `moorish_dev_logo.png` into `assets/`.
  - **Gotchas/Next Steps:** Proceed to T0.01.

### 🛠️ Refactoring & Build
- [ ] **[REFACTOR] | T0.01 | ⚡CRITICAL — Build Meal Planner Notion Template**
  - **Impact:** `/Meal Planner and Grocery List/notion_screenshots/`, `/docs/`
  - **Details:**
    1. **[ARCHITECTURE]** Create `[DB] Backend`. Move `Meals` and `Grocery List` databases inside. Create a Relation between Meals → Grocery Items. Create Linked Views on dashboard.
    2. **[FORMULA]** Add `Grocery Progress` on Grocery List: `slice("▓▓▓▓▓▓▓▓▓▓", 0, round((prop("Bought Count") / prop("Total Items")) * 10))`. Add `Weekly Calories` Rollup on Meals to sum calorie counts.
    3. **[NAVIGATION]** Synced Block at top for Navigation Menu.
    4. **[FOOTER]** Synced Block at bottom (Traffic Footer) with Moorish Dev brand mention.
    5. **[SEO]** Toggle titled `[Admin] SEO Metadata` with SEO Title, Meta Description, 10 Keywords.
    6. **[BUTTON]** Add Buttons: "🍽️ Add Meal" and "🛒 Add Grocery Item".
    7. **[CALLOUT]** Gray Callout "How to Use": (1. Duplicate, 2. Plan Your Meals for the Week, 3. Auto-Generate Grocery List).
  - **Affiliate Check:** N/A

### 📄 Documentation
- [ ] **[CONTENT] | D7.01 | 🔴 HIGH — Populate `docs/Database_Schema.md`**
- [ ] **[CONTENT] | D7.02 | ⚠️ MEDIUM — Populate `marketing/Launch_Copy.md`**
- [ ] **[CONTENT] | D7.03 | ⚠️ MEDIUM — Populate `setup_guide/Setup_Guide.md`**

### 🚀 Launch
- [ ] **[MARKETING] | L7.01 | 🟢 LOW — Publish to Notion Template Gallery**

---

## Summary

| Phase | Tasks | Done | Remaining |
|-------|-------|------|-----------|
| Init & Structure | 1 | 1 | 0 |
| Build & Refactor | 1 | 0 | 1 |
| Documentation | 3 | 0 | 3 |
| Launch | 1 | 0 | 1 |
| **TOTAL** | **6** | **1** | **5** |

> **Priority Order**: T0.01 → D7.01 → D7.02 → D7.03 → L7.01
