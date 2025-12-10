# 🍃 EcoTrack: Industrial CO₂ Monitor

EcoTrack is a simple, web-based tool designed to help industrial plants calculate, visualize, and benchmark their daily carbon dioxide ($\text{CO}_2$) emissions based on fuel consumption. It provides an immediate emission analysis, an AI-driven suggestion, and a Green Score.

## ✨ Features

* **Emission Calculation:** Calculates total daily $\text{CO}_2$ emissions (in kg) based on consumption of Coal, Diesel, and Natural Gas.
* **Industry Benchmarks:** Compares calculated emissions against specific industry benchmarks (Fertilizer, Polymer, Refinery, and Generic plants).
* **Performance Analysis:** Shows the difference between the plant's emissions and the industry benchmark, indicating 'Excess' or 'Saved' $\text{CO}_2$.
* **Green Score:** Assigns an intuitive Eco-Gold, Eco-Silver, or Eco-Bronze score.
* **AI Recommendation:** Provides actionable suggestions based on the total emission level (e.g., "Excellent," "Moderate," or "Critical").
* **Data Visualization:** Includes interactive charts (using Chart.js) for:
    * **Fuel Source Breakdown:** Doughnut chart showing the percentage contribution of each fuel source to the total $\text{CO}_2$.
    * **Emission Trend:** Line chart simulating recent emission trends (up to the current day's calculated value).
* **PDF Report Generation:** Allows users to download the analysis results as a PDF document (using jsPDF).

## 🚀 Getting Started

This project is entirely front-end and requires no server-side configuration.

### Prerequisites

You only need a modern web browser to run the application.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YourUsername/EcoTrack-CO2-Monitor.git](https://github.com/YourUsername/EcoTrack-CO2-Monitor.git)
    cd EcoTrack-CO2-Monitor
    ```
2.  **Open the file:**
    Simply open the `index.html` file in your web browser.

    ```bash
    # Example command (may vary by OS)
    open index.html
    ```

## 🛠 Technology Stack

* **HTML5:** Structure and content.
* **CSS3:** Styling (using custom CSS variables for a clean, green theme).
* **JavaScript (ES6):** Core logic, calculations, and DOM manipulation.
* **Chart.js:** For creating the dynamic emission breakdown and trend charts.
* **jsPDF:** For generating the downloadable PDF reports.

## ⚙️ Core Logic: Emission Factors

The $\text{CO}_2$ calculation is based on the following hardcoded emission factors ($\text{EF}$s) from `script.js`:

| Fuel Source | Unit | Emission Factor ($\text{EF}$) | Formula |
| :--- | :--- | :--- | :--- |
| **Coal** | kg/day | $2.42$ | $\text{Coal Emissions} = \text{Consumption} \times 2.42$ |
| **Diesel** | L/day | $2.68$ | $\text{Diesel Emissions} = \text{Consumption} \times 2.68$ |
| **Natural Gas** | $\text{m}^3$/day | $2.00$ | $\text{Gas Emissions} = \text{Consumption} \times 2.00$ |
| **Total** | | | $\sum(\text{Fuel Emissions})$ |

All $\text{CO}_2$ emissions are in $\text{kg} \, \text{CO}_2$.

## 💡 How to Use

1.  **Select Plant Type:** Choose your industry type from the dropdown to set the correct $\text{CO}_2$ benchmark.
2.  **Input Data:** Enter your daily consumption values for Coal (kg), Diesel (L), and Natural Gas ($\text{m}^3$).
3.  **Calculate:** Click the "**Calculate Footprint**" button to see the detailed **Emission Analysis** and update the dashboard charts.
4.  **Report:** Use the "**Download PDF**" button to save a copy of the analysis.

## 🎨 Styling and Theme

The application uses a green-themed color palette defined via CSS variables in `style.css`:

| Variable | Hex Code | Purpose |
| :--- | :--- | :--- |
| `--primary` | `#1cba24` | Main action color, primary text. |
| `--bg-color` | `#d7f3d9` | Light background for the page. |
| `--card-bg` | `#ffffff` | Background for information cards. |
| `--text-color` | `#183424` | Primary body text color. |

## 🤝 Contribution

Contributions are welcome! If you have suggestions for new industry benchmarks, better emission factors, or feature improvements, please open an issue or submit a pull request.

## 📄 License

This project is licensed under the MIT License - see the `LICENSE` file (if you choose to add one) for details.

---

*Made with $\heartsuit$ for a greener planet.*
