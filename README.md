# 🛡️ Web Vulnerability Scanner (Reflected XSS Detector)

A lightweight Python-based web vulnerability scanner designed to detect **Reflected Cross-Site Scripting (XSS)** and basic input sanitization flaws.

> ⚠️ **Disclaimer:** This tool is strictly for educational purposes and authorized security testing only. Do NOT scan websites without explicit permission.

---

## 🚀 Features

* 🌐 Recursive web crawler (same-domain)
* 🔍 Detects URL parameter-based XSS
* 🧾 Scans HTML forms (GET & POST)
* 💉 Injects test payloads safely
* 📊 Generates a vulnerability report
* ⚡ Simple and beginner-friendly implementation

---

## 🧠 How It Works

1. Crawls the target website
2. Identifies:

   * Links with query parameters
   * Forms and input fields
3. Injects XSS payloads
4. Checks if payload is reflected in response
5. Logs potential vulnerabilities

---

## 📂 Project Structure

```
web-vuln-scanner/
│
├── scanner.py        # Main scanner script
├── report.txt        # Generated report (after scan)
├── requirements.txt  # Dependencies
└── README.md         # Project documentation
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/sandip-sec/web-vuln-scanner.git
cd web-vuln-scanner
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install requests beautifulsoup4
```

---

## ▶️ Usage

```bash
python scanner.py
```

Enter the target URL when prompted:

```
Enter target URL: http://testphp.vulnweb.com
```

---

## 📄 Sample Output

```
[!] Vulnerable: http://example.com/search?q=<script>alert(1)</script>
[!] XSS in form: http://example.com/login
```

---

## 📝 Report Output

A file named `report.txt` will be generated:

```
Vulnerable URL: http://example.com/search?q=<script>alert(1)</script>
Payload: <script>alert(1)</script>
```

---

## 🧪 Safe Testing Environments

Use only on intentionally vulnerable apps like:

* **DVWA (Damn Vulnerable Web Application)**
* **OWASP Juice Shop**
* Localhost test environments

---

## ⚠️ Limitations

* ❌ No DOM-based XSS detection
* ❌ No JavaScript execution engine
* ❌ No WAF bypass techniques
* ❌ No payload encoding/obfuscation
* ❌ Basic crawling only

---

## 🔥 Future Improvements

* ✅ Add Selenium/Playwright for DOM XSS
* ✅ Multi-threaded scanning
* ✅ Advanced payload generation
* ✅ GUI (Tkinter / PyQt)
* ✅ JSON/HTML report export
* ✅ Authentication handling
* ✅ Proxy support (Burp/ZAP integration)

---

## 🛠️ Tech Stack

* Python 3
* requests
* BeautifulSoup (bs4)

---

## 📌 Example Payloads Used

```html
<script>alert(1)</script>
"><script>alert(1)</script>
<img src=x onerror=alert(1)>
```

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create a new branch
3. Make your changes
4. Submit a pull request

---

## 📜 License

This project is licensed under the MIT License.

---

## ⚠️ Legal Disclaimer

This tool is intended for:

* Educational purposes
* Ethical hacking labs
* Authorized penetration testing

The developer is **not responsible for misuse**.

---

## 💡 Author

**Vaskar Chandra Mandal**

Cybersecurity Enthusiast | Python Developer

---

## ⭐ Support

If you found this project useful, give it a ⭐ on GitHub!
