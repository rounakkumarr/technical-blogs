# technical-blogs
🔐 Security-related technical blog posts by Rounak

🔍 What is XSS?
Cross-Site Scripting (XSS) is a type of security vulnerability usually found in web applications. It allows attackers to inject malicious scripts into web pages viewed by other users. These scripts can be used to:  
• Steal session cookies  
• Redirect users to malicious websites  
• Deface web pages  
• Hijack accounts or user actions  
XSS is part of the OWASP Top 10, a well-known list of the most serious web application security risks. 

🧪 Types of XSS Attacks
There are three main types of XSS:  
1. Stored XSS (Persistent)  
• The malicious script is stored on the server, for example, in comments or user profiles.  
• It triggers when other users visit the infected page.  
2. Reflected XSS (Non-Persistent)  
• The script is injected via URL or form input.  
• It runs immediately when the user clicks a crafted link.  
3. DOM-Based XSS  
• The vulnerability exists in the frontend JavaScript.  
• The script manipulates the DOM without proper sanitization.

💡 A Simple Example of XSS
Imagine a blog comment box that doesn’t clean user input. An attacker submits:  
<script>alert('Hacked!');</script>  
If the app displays this as-is, any visitor will see a popup. In real-world attacks, this could be used to steal cookies, log keystrokes, or inject phishing links.  

🛡️ How to Prevent XSS
1. Input Validation & Sanitization 
• Never trust user input.  
• Use libraries like DOMPurify to clean HTML.  
2. Output Encoding  
• Escape dynamic data before rendering it in HTML, JS, or CSS.  
• Use built-in template engines that auto-escape output, such as Django or Flask.  
3. Use Security Headers  
• Implement Content-Security-Policy (CSP) to control which scripts can run.  
Example:  
Content-Security-Policy: default-src 'self'; script-src 'self'  
4. Framework-Level Protections  
• Use secure frameworks like React, Angular, or Vue.  
• These automatically escape output unless overridden.  
5. Regular Security Audits  
• Use tools like Astra Security’s Pentest Suite to scan and fix vulnerabilities.  
• Combine automated scans with manual testing for better coverage.  

✅ Conclusion
XSS is a serious but preventable threat. By following security best practices, such as input sanitization, output encoding, and regular security testing, you can greatly reduce the risk of XSS and protect your users.  
If you’re running a website or web app, don’t wait for an attack to take action. Make secure coding a habit, and use tools like Astra Security to stay one step ahead of attackers. 
