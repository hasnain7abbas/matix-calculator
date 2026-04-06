<p align="center">
  <img src="https://img.shields.io/badge/vanilla-HTML%20%2F%20CSS%20%2F%20JS-0b0f1a?style=for-the-badge&labelColor=0b0f1a&color=2dd4bf" alt="Tech Stack" />
  <img src="https://img.shields.io/badge/dependencies-zero-0b0f1a?style=for-the-badge&labelColor=0b0f1a&color=818cf8" alt="Zero Dependencies" />
  <img src="https://img.shields.io/badge/matrix%20size-up%20to%207×7-0b0f1a?style=for-the-badge&labelColor=0b0f1a&color=f472b6" alt="Matrix Size" />
</p>

<h1 align="center">
  Matix — Matrix Determinant Calculator
</h1>

<p align="center">
  <strong>A premium, dark-themed matrix determinant calculator with recursive cofactor expansion and step-by-step breakdowns.</strong>
</p>

<p align="center">
  <a href="#-live-demo">Live Demo</a> •
  <a href="#-features">Features</a> •
  <a href="#-how-it-works">How It Works</a> •
  <a href="#-usage">Usage</a> •
  <a href="#-tech-stack">Tech Stack</a>
</p>

---

## 🔗 Live Demo

**[→ Launch Matix Calculator](https://hasnain7abbas.github.io/matix-calculator/)**

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| **Adjustable Size** | Supports matrices from 1×1 up to 7×7 via an interactive slider |
| **Step-by-Step Breakdown** | Expandable section shows the full cofactor expansion tree with highlighted signs and intermediate results |
| **Instant Computation** | Pure client-side JavaScript — no server, no dependencies, no latency |
| **Random Fill** | One-click random matrix generation for quick testing |
| **Keyboard Navigation** | Tab/Enter moves between cells for fast data entry |
| **Dark Lab Theme** | Deep void backgrounds with phosphor-cyan glows — designed to feel like a precision instrument |
| **Responsive** | Fully functional on mobile, tablet, and desktop |

---

## 🧮 How It Works

The calculator uses **cofactor expansion** (Laplace expansion) along the first row:

```
det(A) = Σ (-1)^j · a₀ⱼ · det(M₀ⱼ)
```

Where `M₀ⱼ` is the **minor matrix** obtained by removing row 0 and column j.

### Base Cases

| Size | Method | Example |
|------|--------|---------|
| **1×1** | Direct value | `det([5]) = 5` |
| **2×2** | `ad − bc` | `det([[a,b],[c,d]]) = ad − bc` |
| **N×N** | Recursive cofactor expansion along row 0 | Breaks down into (N−1)×(N−1) sub-problems |

### Example: 3×3 Matrix

```
A = | 1  2  3 |
    | 4  5  6 |
    | 7  8  9 |

det(A) = +1·det|5 6| − 2·det|4 6| + 3·det|4 5|
              |8 9|       |7 9|       |7 8|

       = 1·(45−48) − 2·(36−42) + 3·(32−35)
       = 1·(−3) − 2·(−6) + 3·(−3)
       = −3 + 12 − 9
       = 0
```

---

## 📖 Usage

1. **Set the matrix size** using the slider (1–7)
2. Click **Generate** to create the input grid
3. Enter values into each cell (or click **Random** for test data)
4. Click **Compute Determinant** to see the result
5. Expand **Step-by-step breakdown** to see the full computation tree

---

## 🛠 Tech Stack

- **Vanilla HTML / CSS / JS** — zero external dependencies
- **CSS Custom Properties** — consistent theming via design tokens
- **Google Fonts** — [Outfit](https://fonts.google.com/specimen/Outfit) (display), [DM Sans](https://fonts.google.com/specimen/DM+Sans) (UI), [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) (code/numbers)
- **CSS Animations** — smooth transitions, flicker effects, gradient pulses
- **Single HTML file** — just open `index.html` in any browser

---

## 📂 Project Structure

```
matix-calculator/
├── index.html    ← The entire application (self-contained)
└── README.md     ← You are here
```

---

## 🚀 Run Locally

No build step. No install. Just open the file:

```bash
# Clone and open
git clone https://github.com/hasnain7abbas/matix-calculator.git
cd matix-calculator
open index.html    # macOS
start index.html   # Windows
xdg-open index.html  # Linux
```

Or simply drag `index.html` into your browser.

---

<p align="center">
  <sub>Built by <strong>Hasnain</strong></sub>
</p>
