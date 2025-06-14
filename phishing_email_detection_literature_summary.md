# Literature Review – Phishing Email Detection Using Machine Learning: Patterns, Features, and Implementation


## Authors & Responsibilities

This literature review was completed by **Gabriel Naranjo** ✅ and **Hao Ding** as part of the responsibilities for the role of *Literature & Threat Analyst* in the ECE591/ECE597 Capstone Project 2025.

**Role Description:**
- Research phishing detection strategies  
- Summarize key features (e.g., suspicious links, wording patterns)  
- Propose ML directions for email classification  

---

## 1. Phishing Email Patterns and Features

Phishing emails tend to follow consistent patterns, which can be categorized into three broad types: linguistic, structural, and behavioral.

### 🔹 Linguistic Patterns
Linguistically, phishing messages often employ urgency and emotional triggers to pressure recipients into immediate action. Phrases like “Act now or your account will be suspended” are typical examples (1; 2). These emails also frequently feature generic greetings, such as “Dear Customer,” and are prone to grammatical or typographical errors. These issues usually stem from automated generation or non-native writing (1).
In addition, phishing emails often rely on psychological manipulation through threat-based or reward-based framing, such as “update now to avoid suspension” or “claim your prize now” (8; 9). Subject lines may contain excessive capitalization or symbolic characters, and frequently reference financial institutions, packages, or service disruptions (11).

### 🔹 Structural Patterns
Structurally, suspicious URLs are common. Attackers often use domain misspellings, like “paypa1.com,” or incorporate excessive subdomains, such as “secure.login.bank.com” (3; 4). Other techniques include obfuscating links through URL shortening services like bit.ly or embedding HTML forms and scripts that imitate legitimate websites (4; 5).   Visual inconsistencies, such as pixelated logos, misaligned layout, or off-brand fonts, are also strong indicators (10). Additionally, phishing emails often include malicious attachments or embedded JavaScript (e.g., onclick events) intended to harvest credentials or redirect users to controlled websites (12). Structural red flags also extend to header information: phishing emails frequently contain discrepancies between the “From” and “Reply-To” fields or originate from domains unrelated to the sender’s display name (3; 6; 9).

### 🔹 Behavioral Patterns
Behaviorally, phishing emails frequently include requests for sensitive data, such as login credentials or financial information (7). They may also contain unsolicited attachments, particularly files with extensions like `.exe` or `.zip`, which are commonly associated with malware (1). Additionally, phishing emails are often sent at unusual hours, such as in the middle of the night, in an attempt to catch recipients off guard (7).


Several studies also highlight spoofing behaviors where the sender mimics legitimate entities through domain lookalikes and display name manipulation (12). Messages may exploit social engineering techniques, like appealing to authority (e.g., “IT Department”) or mimicking trusted institutions to lower user suspicion (11).


These recurring linguistic, structural, and behavioral patterns form the basis for designing machine learning-based phishing detection systems. A clear understanding of these categories, supported by literature across multiple domains, is essential for building reliable, interpretable, and effective detection frameworks (8; 9; 10; 11; 12).

## 2. Features for Machine Learning Detection

To detect phishing emails using machine learning, these identifiable patterns must first be translated into measurable and quantifiable features. These features are typically categorized into content-based, URL-based, structural, and behavioral groups.

### 📝 Content-Based Features
Content-based features include the frequency of specific keywords like “urgent” or “verify” (1), sentiment scores that capture emotional tone—especially urgency or fear (2), and the number of grammatical or spelling errors, which can be identified using natural language processing tools such as NLTK (1).

### 🌐 URL-Based Features
URL-based features focus on elements like the length of the URL—longer URLs are often associated with phishing attempts (3). The presence of special characters such as “@” or “-”, the total number of subdomains, and the use of URL shortening services also provide useful indicators (4).

### 🧱 Structural Features
Structural features involve the presence of suspicious HTML elements, embedded scripts, or images within the body of the email (7). Additional structural data includes email header metadata (e.g., sender domain) and overall message length (3).

### ⚠️ Behavioral Features
Behavioral features include the presence of requests for personal information (1), the types of attachments included in the message (e.g., `.exe`, `.zip`), and the email’s sending time—particularly if it falls outside of normal business hours ( 7).

These features are used as input for training machine learning models to classify emails as either phishing or legitimate.


---

## 📚 References

1. Alhuzali, A., et al. (2025). *In-Depth Analysis of Phishing Email Detection*. Applied Sciences, 15, 3396. https://doi.org/10.3390/app15063396  
2. Bountakas, P., et al. (2024). *Cyber Threat Hunting Using Deep Learning*. Information, 15, 512. https://doi.org/10.3390/info15090512  
3. Fares, H., et al. (2024). *ML Approach for Email Phishing Detection*. Procedia Comp. Sci., 246, 179–186. https://doi.org/10.1016/j.procs.2024.11.179  
4. Al-Subaiey, A., et al. (2024). *Web-Based AI Platform for Threat Detection*. Comp. & Elec. Eng., 120, 109625. https://doi.org/10.1016/j.compeleceng.2024.109625  
5. Netskope. (2024). *Phishing Threat Analysis Report*.  
6. Proofpoint. (2024). *Email Threat Report*.  
7. Altwaijry, N., et al. (2024). *Advancing Phishing Email Detection*. Sensors, 24, 2077. https://doi.org/10.3390/s24072077  
8. Anwar, M.Z., et al. (2019). *A Survey of Phishing Email Filtering Techniques*. Comp. Communications, 145, 75–97.  
9. Khonji, T., et al. (2015). *Phishing Detection: A Literature Survey*. Telecommunication Systems, 60(3), 507–526.  
10. Burita, L., et al. (2021). *Analysis of Phishing Emails*. AIMS Electronics, 5(1), 1–14.  
11. Wash, M., et al. (2020). *Detection of Phishing Emails by Experts*. Proc. CHI Conf. Human Factors.  
12. Sabir, M.A., et al. (2016). *Phishing Detection Using Classification Techniques*. Neural Comput. & Apps, 28(10), 3151–3162.  
