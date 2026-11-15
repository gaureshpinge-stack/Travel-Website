# ✈️ WanderIndia — Travel & Trip Booking Web Application

A lightweight, responsive, and secure multi-page travel showcase and trip booking web application tailored for students and budget-conscious travellers. Built using pure **HTML5, CSS3, and Vanilla JavaScript (ES6)** with zero external dependencies.

---

## 🌟 Key Features

### 1. Home & Destination Showcase (`index.html`)
- **Curated Destinations:** 6 popular Indian travel destinations (Goa, Manali, Jaipur, Kerala, Ladakh, Rishikesh) with base prices, best travel seasons, and photography.
- **Student Travel Tips:** Practical advice on budgeting, packing light, local transport, and student ID discounts.
- **Photo Gallery:** Responsive 6-item photo gallery showcasing moments from the road.
- **Resilient Offline Architecture:** Serves local photography from `images/` with an instant inline SVG vector fallback on `onerror` to prevent broken image icons.

### 2. Dedicated Booking & Estimation System (`booking.html`)
- **Seamless Inter-Page Navigation:** Selecting any destination on the home page passes `?dest=<id>` via URL query parameters, automatically pre-selecting the destination and displaying its thumbnail in the booking form.
- **Smart Date Math:** Users select a **Start Date** and **Return Date**; the system automatically calculates the trip duration in days without requiring manual numeric entry:
  $$\text{Days} = \max\left(1, \text{round}\left(\frac{\text{Return Date} - \text{Departure Date}}{1000 \times 60 \times 60 \times 24}\right)\right)$$
- **Real-Time Cost Estimator:** Live recalculation accounting for base destination rates, duration, adult/child counts (children under 12 receive a 50% discount), hotel upgrades (Budget, 3-Star, 5-Star), and transport options.
- **Instant Printable Voucher (PDF):** Submitting the booking generates a confirmed **WanderIndia Travel Voucher** with a unique Booking ID (`WI-XXXX`). Powered by `@media print` CSS, clicking **"Download / Print Receipt (PDF)"** formats strictly the voucher cleanly for A4 printing or saving as PDF.
- **Browser Persistence:** Uses `localStorage` to save and display booking history across sessions, with one-click cancellation.
- **Defensive Security:** Implements `escapeHTML()` to sanitize all user-supplied data (Name, Notes, etc.), preventing DOM-based Cross-Site Scripting (XSS).

---

## 📁 Repository Structure

```text
Travel-Website/
├── index.html                       # Home page, hero banner, destination cards, tips, & gallery
├── booking.html                     # Dedicated booking form, live estimator, voucher & history
├── README.md                        # Project documentation
├── .gitignore                       # Ignored system and editor files
├── WanderIndia_Project_Report.pdf   # Complete 3-page academic report for submission
├── WanderIndia_Source_Code.pdf      # Complete 13-page syntax-formatted source code document
└── images/                          # Travel photography assets
    ├── goa.jpg
    ├── manali.jpg
    ├── jaipur.jpg
    ├── kerala.jpg
    ├── ladakh.jpg
    ├── rishikesh.jpg
    └── gallery1.jpg ... gallery6.jpg
```

---

## 🚀 Getting Started

No build step or server setup is required!

1. **Clone the repository:**
   ```bash
   git clone https://github.com/gaureshpinge-stack/Travel-Website.git
   ```
2. **Open in browser:**
   - Double-click `index.html` to open the home page in Google Chrome, Microsoft Edge, Firefox, or Safari.
   - Click **"Book This Trip"** on any destination card to test the booking flow.

---

## 🛠️ Technology Stack

- **Markup:** HTML5 (Semantic tags, WCAG accessibility with `<label for>` and `aria-live`)
- **Styles:** CSS3 (CSS Grid, Flexbox, `@media print`, custom responsive typography)
- **Scripting:** Vanilla JavaScript ES6 (DOM manipulation, `URLSearchParams`, `Date` arithmetic, `localStorage`)
- **Dependencies:** 0 (Completely offline-capable)

---

## 📄 Academic Project Details

- **Project:** First-Year Web Development College Project
- **Topic:** Travel & Trip Booking Web Application
- **Author:** Gouresh Pinge
- **Repository:** [github.com/gaureshpinge-stack/Travel-Website](https://github.com/gaureshpinge-stack/Travel-Website)
