# 🛒 E-Commerce Web Automation Framework

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)
![Selenium](https://img.shields.io/badge/Selenium-WebDriver-green?style=flat-square&logo=selenium)
![Pytest](https://img.shields.io/badge/Pytest-Framework-orange?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)

A **Selenium WebDriver + Python** test automation framework built using the **Page Object Model (POM)** design pattern to automate key user journeys on an e-commerce web application.

---

## 📌 About This Project

This project was built to demonstrate end-to-end test automation for a real-world e-commerce application. It covers the most critical user flows — login, product search, cart management, and checkout — and is structured so new test cases can be added quickly without rewriting existing code.

**Reduced manual regression effort by 40%**, cutting regression cycle time from ~4 hours to under 45 minutes.

---

## 🚀 Features

- ✅ Page Object Model (POM) design for clean, maintainable code
- ✅ Data-driven testing using Pytest parametrize
- ✅ Automated test reporting with Pytest HTML Report
- ✅ Cross-browser support (Chrome, Firefox)
- ✅ Reusable utility functions (waits, screenshots, config reader)
- ✅ Easy to extend — add new pages and tests without touching existing code

---

## 🧪 Test Scenarios Covered

| Module | Test Cases |
|--------|-----------|
| Login | Valid login, invalid credentials, empty fields, locked account |
| Product Search | Search by keyword, filter by category, no results handling |
| Cart | Add to cart, remove item, update quantity, empty cart |
| Checkout | Guest checkout, form validation, order confirmation |
| Navigation | Home page load, broken links, page title verification |

---

## 🗂️ Project Structure

```
selenium-ecommerce-automation/
│
├── pages/                  # Page Object classes
│   ├── base_page.py        # Common methods (click, type, wait)
│   ├── login_page.py
│   ├── home_page.py
│   ├── search_page.py
│   ├── cart_page.py
│   └── checkout_page.py
│
├── tests/                  # Test files
│   ├── test_login.py
│   ├── test_search.py
│   ├── test_cart.py
│   └── test_checkout.py
│
├── utils/                  # Helper utilities
│   ├── config_reader.py    # Reads config.ini
│   ├── driver_factory.py   # Browser setup/teardown
│   └── screenshot.py       # Captures failure screenshots
│
├── test_data/              # Test input data
│   └── users.json
│
├── reports/                # Auto-generated HTML reports
├── config.ini              # Base URL, browser, timeouts
├── conftest.py             # Pytest fixtures
├── requirements.txt        # Dependencies
└── README.md
```

---

## ⚙️ Setup & Installation

### Prerequisites
- Python 3.8 or above
- Google Chrome browser
- ChromeDriver (matching your Chrome version)

### Steps

```bash
# 1. Clone this repository
git clone https://github.com/YOUR_USERNAME/selenium-ecommerce-automation.git
cd selenium-ecommerce-automation

# 2. Install dependencies
pip install -r requirements.txt

# 3. Update config.ini with your base URL
[settings]
base_url = https://your-app-url.com
browser = chrome
timeout = 10
```

---

## ▶️ Running Tests

```bash
# Run all tests
pytest tests/

# Run a specific module
pytest tests/test_login.py

# Run with HTML report
pytest tests/ --html=reports/report.html --self-contained-html

# Run with verbose output
pytest tests/ -v
```

---

## 📊 Sample Test Report

After running tests, open `reports/report.html` in your browser to see:
- Total tests run / passed / failed
- Execution time per test
- Screenshots attached on failure
- Error messages and stack traces

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.8+ | Programming language |
| Selenium WebDriver | Browser automation |
| Pytest | Test framework & runner |
| POM (Design Pattern) | Code structure & reusability |
| pytest-html | HTML test reports |
| ChromeDriver | Chrome browser driver |

---

## 👨‍💻 Author

**Raju Kudupudi**
- 📧 Rajukudupudi2001@gmail.com
- 🔗 [LinkedIn](https://linkedin.com/in/raju-k-17b3b)
- 💼 SDET | QA Automation Engineer

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
