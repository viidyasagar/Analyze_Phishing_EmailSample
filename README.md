# Analyze_Phishing_EmailSample
Analyze a phishing email by examining the sender's address, email headers, and body content. Identify suspicious links, urgent language, mismatched URLs, and spelling errors. Use tools like header analyzers and link checkers to detect spoofing and malicious intent.


### 🛠️ **Phishing Email Analysis – Commands with Explanation**

---

#### 1. **Open the email sample**

```bash
nano phishing-sample.eml
```

📝 *Opens the phishing email file in the terminal using the `nano` text editor for manual inspection.*

---

#### 2. **Extract the "From" email address**

```bash
grep -i from phishing-sample.eml
```

🔍 *Searches for lines containing "From" (case-insensitive) to check the sender's address. Helps detect spoofed domains like `paypai.com` instead of `paypal.com`.*

---

#### 3. **Check the "Reply-To" field**

```bash
grep -i reply-to phishing-sample.eml
```

🎯 *Finds the `Reply-To` header to see where the attacker wants replies sent. Often a different, suspicious address like `attacker@fake-site.com`.*

---

#### 4. **Extract all URLs in the email**

```bash
grep -oP 'http[s]?:\/\/[^"]+' phishing-sample.eml
```

🌐 *Extracts any HTTP/HTTPS URLs using Perl-compatible regex. This helps identify suspicious or malicious links in the email body.*

---

#### 5. **Find urgent or phishing keywords**

```bash
grep -iE 'urgent|suspend|verify|account' phishing-sample.eml
```

⚠️ *Searches for common phishing-related keywords like "Urgent", "Suspended", "Verify", and "Account" to detect social engineering language.*

---

#### 6. **View entire email content**

```bash
less phishing-sample.eml
```

📖 *Allows you to scroll through the full email content for detailed analysis, formatting, and hidden signs of phishing.*






