# UP Climate Dashboard — Color Bar Range & Classification Documentation

## 1. Overview & Data Source
The color bar ranges and category breaks in the **UP Climate Dashboard** are established directly from the **Tmax** (Maximum Temperature) and **HTmax** (Heat Days) statistics reports/PDFs.

The visualization uses:
* **Sequential Warm Color Scale (Yellow to Dark Red):** For standard scenario maps ($\text{T}_{\text{max}}$ and Heat Days) to highlight increasing intensity.
* **Diverging Color Scale (Teal to Red):** For Comparison (% Delta) Mode to visually distinguish reduction versus increase.

---

## 2. Maximum Temperature ($\text{T}_{\text{max}}$ in °C)

| Range Category | Value Threshold | Hex Color Code | Color Name | Visual Representation |
| :--- | :--- | :--- | :--- | :--- |
| **Category 1 (Low)** | $< 32.0\text{ }^\circ\text{C}$ | `#fef3c7` | Light Yellow | 🟡 |
| **Category 2 (Moderate)** | $32.0\text{ }^\circ\text{C} - 34.0\text{ }^\circ\text{C}$ | `#fed7aa` | Soft Peach / Light Orange | 🟧 |
| **Category 3 (High)** | $34.0\text{ }^\circ\text{C} - 36.0\text{ }^\circ\text{C}$ | `#fdba74` | Medium Orange | 🟠 |
| **Category 4 (Very High)** | $36.0\text{ }^\circ\text{C} - 38.0\text{ }^\circ\text{C}$ | `#f97316` | Deep Orange | 🔴 |
| **Category 5 (Severe)** | $> 38.0\text{ }^\circ\text{C}$ | `#c2410c` | Dark Red / Red-Brown | 🔻 |

---

## 3. Average Heat Days ($\text{HT}_{\text{max}}$ in Days)

| Range Category | Value Threshold | Hex Color Code | Color Name | Visual Representation |
| :--- | :--- | :--- | :--- | :--- |
| **Category 1 (Low)** | $< 10\text{ Days}$ | `#fef3c7` | Light Yellow | 🟡 |
| **Category 2 (Moderate)** | $10 - 20\text{ Days}$ | `#fed7aa` | Soft Peach / Light Orange | 🟧 |
| **Category 3 (High)** | $20 - 30\text{ Days}$ | `#fdba74` | Medium Orange | 🟠 |
| **Category 4 (Very High)** | $30 - 40\text{ Days}$ | `#f97316` | Deep Orange | 🔴 |
| **Category 5 (Severe)** | $> 40\text{ Days}$ | `#c2410c` | Dark Red / Red-Brown | 🔻 |

---

## 4. Comparison Mode (% Delta Change)

### Average Temperature Range (-50% to +50%)
| Range Category | Percentage Threshold | Hex Color Code | Meaning / Classification | Visual Representation |
| :--- | :--- | :--- | :--- | :--- |
| **Reduction - Major** | $\le -30\%$ | `#1f6f6b` | Dark Teal Green | 🟢 |
| **Reduction - Moderate** | $-30\% \text{ to } -10\%$ | `#5fa39e` | Medium Teal | 🩵 |
| **Reduction - Slight** | $-10\% \text{ to } 0\%$ | `#bcdedb` | Light Teal | 🤍 |
| **Increase - Slight** | $0\% \text{ to } 10\%$ | `#f3c9b8` | Light Salmon / Pink | 🌸 |
| **Increase - Moderate** | $10\% \text{ to } 30\%$ | `#e07a52` | Dark Coral | 📙 |
| **Increase - High** | $> 30\%$ | `#c23b22` | Crimson Red | 🔴 |

### No. of Hot Days Range (-100% to +100%)
| Range Category | Percentage Threshold | Hex Color Code | Meaning / Classification | Visual Representation |
| :--- | :--- | :--- | :--- | :--- |
| **Reduction - Major** | $\le -50\%$ | `#1f6f6b` | Dark Teal Green | 🟢 |
| **Reduction - Moderate** | $-50\% \text{ to } -20\%$ | `#5fa39e` | Medium Teal | 🩵 |
| **Reduction - Slight** | $-20\% \text{ to } 0\%$ | `#bcdedb` | Light Teal | 🤍 |
| **Increase - Slight** | $0\% \text{ to } 20\%$ | `#f3c9b8` | Light Salmon / Pink | 🌸 |
| **Increase - Moderate** | $20\% \text{ to } 50\%$ | `#e07a52` | Dark Coral | 📙 |
| **Increase - High** | $> 50\%$ | `#c23b22` | Crimson Red | 🔴 |

---

## 5. Active Combination (Combination 3 — High Contrast Thermal Palette)

### Standard View breaks (Tmax):
- $< 34.0\text{ }^\circ\text{C}$ (`#fef9c3` Bright Pale Sun)
- $34.0\text{ }^\circ\text{C} - 35.5\text{ }^\circ\text{C}$ (`#fde047` Golden Yellow)
- $35.5\text{ }^\circ\text{C} - 36.5\text{ }^\circ\text{C}$ (`#fb923c` Bright Amber)
- $36.5\text{ }^\circ\text{C} - 37.2\text{ }^\circ\text{C}$ (`#ea580c` Red-Orange)
- $37.2\text{ }^\circ\text{C} - 38.0\text{ }^\circ\text{C}$ (`#dc2626` Crimson Red)
- $> 38.0\text{ }^\circ\text{C}$ (`#7f1d1d` Deep Maroon)

### Standard View breaks (Heat Days):
- $< 2\text{ Days}$ (`#fef9c3`)
- $2 - 8\text{ Days}$ (`#fde047`)
- $8 - 18\text{ Days}$ (`#fb923c`)
- $18 - 28\text{ Days}$ (`#ea580c`)
- $28 - 38\text{ Days}$ (`#dc2626`)
- $> 38\text{ Days}$ (`#7f1d1d`)

---

## 6. History of Tested Scale Combinations

### **Combination 1: Original Wide Coarse Scale (Baseline)**
- **Tmax Breaks:** $< 32.0^\circ\text{C}$, $32.0 - 34.0^\circ\text{C}$, $34.0 - 36.0^\circ\text{C}$, $36.0 - 38.0^\circ\text{C}$, $> 38.0^\circ\text{C}$
- **Outcome:** Very wide 2.0°C intervals. Almost all UP blocks fell into $34-36^\circ\text{C}$ or $36-38^\circ\text{C}$, making Raw Model and Bias-Corrected Model look flat and uniform.

### **Combination 2: Boss's Specified % Range + 1.5°C Standard Scale**
- **Tmax Breaks:** $< 33.5^\circ\text{C}$, $33.5 - 35.0^\circ\text{C}$, $35.0 - 36.0^\circ\text{C}$, $36.0 - 37.0^\circ\text{C}$, $37.0 - 38.0^\circ\text{C}$, $> 38.0^\circ\text{C}$
- **Comparison % Range:** $-50\%$ to $+50\%$ for Avg Temp, $-100\%$ to $+100\%$ for Hot Days.
- **Outcome:** Added boss's specified comparison percentage scales. Improved contrast between Raw Model (cooler) and Bias-Corrected Model (warmer).

### **Combination 3: Ultra High-Contrast 6-Color Thermal Palette (Current Active)**
- **Tmax Breaks:** $< 34.0^\circ\text{C}$, $34.0 - 35.5^\circ\text{C}$, $35.5 - 36.5^\circ\text{C}$, $36.5 - 37.2^\circ\text{C}$, $37.2 - 38.0^\circ\text{C}$, $> 38.0^\circ\text{C}$
- **Heat Days Breaks:** $< 2\text{ d}$, $2 - 8\text{ d}$, $8 - 18\text{ d}$, $18 - 28\text{ d}$, $28 - 38\text{ d}$, $> 38\text{ d}$
- **Comparison Palette:** Deep Emerald Teal (`#004d40`, `#26a69a`, `#80cbc4`) & Coral Crimson (`#ffcc80`, `#ff7043`, `#d32f2f`).
- **Outcome:** Maximum visual resolution. High saturation and 88% fill opacity make block-level variations immediately striking at a glance.

---

## 7. Technical Implementation Reference
* **File Location:** [index.html](file:///c:/UP_Climate_Dashboard-1/index.html#L245-L271)
* **Functions:** `colorScaleTmax()`, `colorScaleHeat()`, `renderLegends()`
* **Map Engine:** Leaflet GeoJSON Polygon Styling (`styleFeatureForMap`)

