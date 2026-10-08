# hack-the-login-writeup
A professional writeup for the HackerDNA lab “Hack the Login.” Includes methodology, tools used, insights, and key learnings. No flag content disclosed.

# Hack the Login – Writeup

🔗 Lab Reference: [Hack the Login](https://hackerdna.com/labs/hack-the-login)

## 🎯 Objective
Understand how insecure login mechanisms can be exploited and learn the importance of secure authentication practices.

## 🛠 Tools & Techniques Used
- Web Browser Developer Tools (Inspect Element, Cookies tab)
- Basic credential testing (`guest/guest`, `admin/admin`)
- Cookie manipulation
- Optional CLI tools (`curl`, `httpie`) for request replay

## 🔎 Methodology
1. **Explored the Login Page**  
   - Opened the lab URL and tested default credentials.  

2. **Analyzed Authentication Flow**  
   - Observed cookies or tokens set after login.  
   - Identified values like `role=guest` or `user=guest`.  

3. **Manipulated Cookies**  
   - Edited cookie values to escalate privileges (e.g., changing `guest` to `admin`).  
   - Refreshed the page to test if the application validated cookies properly.  

4. **Accessed Restricted Content**  
   - Gained access to hidden admin functionality.  
   - Located the flag string (not disclosed here).  

5. **Submitted the Flag**  
   - Entered the flag into the lab’s submission box to complete the challenge.  

---

## 📚 Key Learnings
- **Weak Authentication**: Relying on client-side cookies without validation is insecure.  
- **Cookie Poisoning**: Attackers can manipulate cookies to impersonate higher-privileged users.  
- **Best Practices**: Authentication tokens should be signed and validated server-side.  

---

## ⚡ Challenges Faced
- Initially overlooked cookie values.  
- Learned to carefully inspect browser storage and headers.  

---

## 🚀 Insights for Future Labs
- Always inspect cookies, local storage, and session tokens.  
- Test for privilege escalation by modifying values.  
- Reinforce the principle: **authentication must never trust client-side data.**

