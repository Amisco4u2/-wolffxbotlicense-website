# 📧 COMPLETE EMAILJS SETUP GUIDE - STEP BY STEP

## 🎯 WHAT WE'RE SETTING UP

**2 Automated Emails:**
1. **Admin Notification** - When customer submits purchase
2. **Customer Activation** - When admin approves license

**Time Required:** 15 minutes

---

## 📝 STEP 1: CREATE EMAILJS ACCOUNT

### **1.1 Sign Up**

```
1. Go to: https://www.emailjs.com/

2. Click "Sign Up" button (top right)

3. Fill in:
   - Email: aminfx.gh@gmail.com
   - Password: (create a strong password)
   - Name: Amin FX
   
4. Click "Sign Up"

5. Check your email inbox

6. Open verification email from EmailJS

7. Click verification link

8. ✅ Account activated!
```

---

## 🔗 STEP 2: CONNECT GMAIL

### **2.1 Add Email Service**

```
1. After login, you're on Dashboard

2. Left sidebar → Click "Email Services"

3. Click "Add New Service" button

4. You'll see service options:
   - Gmail
   - Outlook
   - Yahoo
   - Custom SMTP
   - etc.

5. Click "Gmail"
```

### **2.2 Connect Your Gmail**

```
6. A popup appears

7. Click "Connect Account"

8. Google login page opens

9. Select your account: aminfx.gh@gmail.com

10. Google asks: "EmailJS wants to access your account"
    Permissions:
    - Send email on your behalf
    - Read email settings

11. Click "Allow"

12. You're redirected back to EmailJS

13. ✅ Success message: "Service added successfully"

14. You'll see your service listed:
    Name: Gmail
    Service ID: service_xxxxxxx (copy this!)
    Status: Connected

15. IMPORTANT: Copy the Service ID
    Example: service_abc123xyz
    
    Write it down:
    Service ID: _________________
```

---

## 📄 STEP 3: CREATE EMAIL TEMPLATE #1 (ADMIN NOTIFICATION)

### **3.1 Create New Template**

```
1. Left sidebar → Click "Email Templates"

2. Click "Create New Template" button

3. Template editor opens
```

### **3.2 Configure Template Settings**

```
Template Name: admin_new_purchase

To Name: Admin
To Email: {{to_email}}

From Name: Wolf FX System
From Email: (use your connected Gmail)

Reply To: aminfx.gh@gmail.com

Subject: 🔔 New Purchase Awaiting Verification - {{plan}}
```

### **3.3 Template Content**

**Copy and paste this EXACT template:**

```
Hello Admin,

A new license purchase has been submitted and requires your verification.

═══════════════════════════════════════════════
CUSTOMER INFORMATION
═══════════════════════════════════════════════

Name: {{customer_name}}
Email: {{customer_email}}
Country: {{country}}
WhatsApp: {{whatsapp}}

═══════════════════════════════════════════════
PURCHASE DETAILS
═══════════════════════════════════════════════

Plan: {{plan}}
Amount: ${{price}}
Duration: {{duration}} days

═══════════════════════════════════════════════
MT5 ACCOUNT DETAILS
═══════════════════════════════════════════════

MT5 Account: {{mt5}}
Broker: {{broker}}
Server: {{server}}

⚠️ License will be bound to this broker/server

═══════════════════════════════════════════════
PAYMENT INFORMATION
═══════════════════════════════════════════════

Payment Method: {{method}}
Transaction ID: {{txid}}

⚠️ IMPORTANT: VERIFY THIS TRANSACTION ID!

═══════════════════════════════════════════════
NEXT STEPS
═══════════════════════════════════════════════

1. Check your {{method}} wallet/account
2. Verify the transaction ID: {{txid}}
3. Confirm amount received: ${{price}}
4. Login to admin dashboard
5. Click "Approve & Generate Key"

Admin Dashboard: https://your-site-url.com

═══════════════════════════════════════════════

This is an automated notification from Wolf FX Trading Academy.

Do not reply to this email.
```

### **3.4 Save Template**

```
4. Review the template

5. Click "Save" button (bottom right)

6. Success message appears

7. IMPORTANT: Copy the Template ID
   You'll see: template_xxxxxxx
   Example: template_abc123xyz
   
   Write it down:
   Admin Template ID: _________________
```

---

## 📄 STEP 4: CREATE EMAIL TEMPLATE #2 (CUSTOMER ACTIVATION)

### **4.1 Create Second Template**

```
1. Still in "Email Templates" page

2. Click "Create New Template" again

3. New template editor opens
```

### **4.2 Configure Template Settings**

```
Template Name: customer_activation

To Name: {{customer_name}}
To Email: {{to_email}}

From Name: Wolf FX Trading Academy
From Email: (use your connected Gmail)

Reply To: aminfx.gh@gmail.com

Subject: 🎉 Your Wolf FX License is Activated!
```

### **4.3 Template Content**

**Copy and paste this EXACT template:**

```
Hello {{customer_name}},

Congratulations! Your payment has been verified and your Wolf FX EA license is now ACTIVE!

═══════════════════════════════════════════════
YOUR LICENSE DETAILS
═══════════════════════════════════════════════

License Key: {{license_key}}
Plan: {{plan}}
Valid Until: {{expiry_date}}

⚠️ IMPORTANT: Save your license key securely!

═══════════════════════════════════════════════
BROKER & SERVER BINDING (ANTI-PIRACY)
═══════════════════════════════════════════════

Your license is bound to:

MT5 Account: {{mt5_account}}
Broker: {{broker}}
Server: {{server}}

⚠️ This license will ONLY work on this specific broker and server combination. This is for your security and to prevent unauthorized use.

═══════════════════════════════════════════════
DOWNLOAD YOUR EA
═══════════════════════════════════════════════

Download Link: {{download_link}}

Installation Steps:
1. Download the EA file
2. Open your MT5 platform
3. Go to: File → Open Data Folder
4. Navigate to: MQL5 → Experts
5. Copy the EA file into this folder
6. Restart MT5
7. Drag the EA onto your chart
8. Enter your license key when prompted
9. The EA will verify your broker/server automatically
10. Start trading!

═══════════════════════════════════════════════
🚀 RECOMMENDED: GET A VPS FOR 24/7 TRADING
═══════════════════════════════════════════════

For uninterrupted trading and maximum EA performance, we highly recommend using a VPS (Virtual Private Server).

Benefits:
✅ 24/7 uptime - Never miss a trade
✅ No power outages or internet issues
✅ Faster execution speeds
✅ Professional trading environment
✅ Run EA continuously

Get VPS for as low as {{vps_price}}/month:
{{vps_link}}

Our recommended VPS provider offers:
- Optimized for MT5
- Low latency
- 99.9% uptime guarantee
- Easy setup

═══════════════════════════════════════════════
JOIN OUR TRADING COMMUNITY
═══════════════════════════════════════════════

WhatsApp Group: {{whatsapp_link}}

Get:
- Trading tips and strategies
- EA updates and announcements
- Support from our team
- Connect with other traders

═══════════════════════════════════════════════
NEED HELP?
═══════════════════════════════════════════════

Email: aminfx.gh@gmail.com
WhatsApp: See group link above

We're here to help you succeed!

═══════════════════════════════════════════════

Happy Trading!

Wolf FX Trading Academy Team

═══════════════════════════════════════════════

This email contains your license key. Please keep it secure.
```

### **4.4 Save Template**

```
4. Review the template

5. Click "Save" button

6. Success message appears

7. IMPORTANT: Copy the Template ID
   You'll see: template_xxxxxxx
   Example: template_def456xyz
   
   Write it down:
   Customer Template ID: _________________
```

---

## 🔑 STEP 5: GET YOUR PUBLIC KEY

### **5.1 Find Public Key**

```
1. Left sidebar → Click "Account"

2. Look for "API Keys" section

3. You'll see:
   - Public Key: xxxxxxxxxxxxxxxxxxx
   - Private Key: (don't need this)

4. IMPORTANT: Copy the Public Key
   Example: xYz123AbC456DeF789
   
   Write it down:
   Public Key: _________________

5. Keep this safe - you'll need it next!
```

---

## 📋 STEP 6: COLLECT ALL YOUR IDS

**You should now have 3 important values:**

```
1. Public Key: _________________
   (Example: xYz123AbC456DeF789)

2. Service ID: _________________
   (Example: service_abc123xyz)

3. Admin Template ID: _________________
   (Example: template_abc123)

4. Customer Template ID: _________________
   (Example: template_def456)
```

**✅ Make sure you have ALL 4 values before continuing!**

---

## 🔧 STEP 7: UPDATE YOUR WEBSITE

### **7.1 Download Your Current index.html**

```
1. Go to your hosting (Netlify/GitHub Pages)

2. Download your current index.html file

3. Open it with a text editor:
   - Notepad (Windows)
   - TextEdit (Mac)
   - VS Code (recommended)
   - Sublime Text
   - Notepad++
```

### **7.2 Find and Replace - Update #1**

**Search for this line (around line 217):**
```javascript
emailjs.init("YOUR_PUBLIC_KEY");
```

**Replace with:**
```javascript
emailjs.init("YOUR_ACTUAL_PUBLIC_KEY_HERE");
```

**Example:**
```javascript
emailjs.init("xYz123AbC456DeF789");
```

**✅ Make sure:**
- Keep the quotes ""
- No extra spaces
- Paste your actual Public Key

---

### **7.3 Find and Replace - Update #2**

**Search for this line (around line 301):**
```javascript
emailjs.send('YOUR_SERVICE_ID', 'YOUR_ADMIN_TEMPLATE_ID', {
```

**Replace with:**
```javascript
emailjs.send('service_abc123xyz', 'template_abc123', {
```

**Use YOUR actual Service ID and Admin Template ID!**

**✅ Make sure:**
- Keep the quotes ''
- Comma between the two IDs
- No extra spaces

---

### **7.4 Find and Replace - Update #3**

**Search for this line (around line 336):**
```javascript
emailjs.send('YOUR_SERVICE_ID', 'YOUR_ACTIVATION_TEMPLATE_ID', {
```

**Replace with:**
```javascript
emailjs.send('service_abc123xyz', 'template_def456', {
```

**Use YOUR actual Service ID and Customer Template ID!**

**✅ Make sure:**
- Keep the quotes ''
- Comma between the two IDs
- No extra spaces

---

### **7.5 Save the File**

```
1. Double-check all 3 updates:
   ✓ Public Key updated
   ✓ Admin template updated
   ✓ Customer template updated

2. Save the file (Ctrl+S or Cmd+S)

3. Keep the filename: index.html
```

---

## 🚀 STEP 8: UPLOAD UPDATED FILE

### **Option A: Netlify**

```
1. Go to: https://app.netlify.com

2. Find your site

3. Click on it

4. Go to "Deploys" tab

5. Drag your updated index.html file to the drop zone

6. Wait 30 seconds

7. ✅ Site updated!
```

### **Option B: GitHub Pages**

```
1. Go to your repository

2. Click on index.html

3. Click the pencil icon (Edit)

4. Delete all content

5. Copy and paste content from your updated file

6. Scroll down

7. Click "Commit changes"

8. Wait 2 minutes

9. ✅ Site updated!
```

---

## ✅ STEP 9: TEST EMAILS

### **9.1 Test Admin Notification**

```
1. Go to EmailJS dashboard

2. Click "Email Templates"

3. Click on "admin_new_purchase" template

4. Click "Test Email" button

5. Fill in test values:
   - to_email: aminfx.gh@gmail.com
   - customer_name: Test Customer
   - customer_email: test@example.com
   - plan: MONTHLY
   - price: 150
   - method: USDT
   - txid: TEST123456
   - mt5: 12345678
   - broker: IC Markets
   - server: Demo01
   - country: Ghana
   - whatsapp: +233501234567
   - duration: 30

6. Click "Send Test Email"

7. Check your email: aminfx.gh@gmail.com

8. ✅ If email arrives → Admin notification works!

9. ❌ If no email → Check spam folder
```

### **9.2 Test Customer Activation**

```
1. Still in EmailJS dashboard

2. Click "Email Templates"

3. Click on "customer_activation" template

4. Click "Test Email" button

5. Fill in test values:
   - to_email: aminfx.gh@gmail.com (test to yourself)
   - customer_name: Test Customer
   - license_key: WOLF-TEST-1234-5678
   - plan: MONTHLY
   - expiry_date: 2026-01-21
   - broker: IC Markets
   - server: ICMarkets-Demo01
   - mt5_account: 12345678
   - vps_link: https://my.hyonix.com/aff.php?aff=3926
   - vps_price: $6
   - download_link: https://yoursite.com/download
   - whatsapp_link: https://chat.whatsapp.com/yourlink

6. Click "Send Test Email"

7. Check your email: aminfx.gh@gmail.com

8. ✅ If email arrives → Customer activation works!

9. ❌ If no email → Check spam folder
```

---

## 🔍 STEP 10: TEST ON LIVE SITE

### **10.1 Test Full Purchase Flow**

```
1. Open your live website

2. Create a test account:
   - Name: Test Customer
   - Email: Use YOUR email (aminfx.gh@gmail.com)
   - Password: test123

3. Select a plan (e.g., Weekly $50)

4. Fill purchase form:
   - MT5: 12345678
   - Broker: IC Markets
   - Server: Demo01
   - Country: Ghana
   - WhatsApp: +233501234567

5. Select payment: USDT

6. Enter TX ID: TEST123456789

7. Click "Submit Purchase"

8. ✅ Check your email for admin notification

9. If email arrives → WORKING!
```

### **10.2 Test Approval Flow**

```
10. Login as admin:
    - Username: aminfx
    - Password: Amiena702$

11. See the pending test license

12. Click "Approve & Generate Key"

13. Confirm approval

14. ✅ Check your email for activation email

15. Email should have:
    - License key (generated)
    - VPS recommendation
    - Your referral link

16. If email arrives → FULLY WORKING!
```

---

## 🐛 TROUBLESHOOTING

### **Problem: No Emails Arriving**

**Check 1: Spam Folder**
```
- Check spam/junk folder
- EmailJS emails sometimes go to spam first
- Mark as "Not Spam"
```

**Check 2: Email Service Connected**
```
1. EmailJS Dashboard → Email Services
2. Your Gmail should show "Connected"
3. If shows "Disconnected" → Reconnect
```

**Check 3: Template IDs Correct**
```
1. Open index.html
2. Find the emailjs.send() lines
3. Check Template IDs match exactly
4. No typos, no extra spaces
```

**Check 4: Public Key Correct**
```
1. EmailJS Dashboard → Account → API Keys
2. Copy Public Key again
3. Replace in index.html
4. Must be EXACT match
```

**Check 5: Browser Console**
```
1. Open your site
2. Press F12 (Developer Tools)
3. Go to "Console" tab
4. Try submitting purchase
5. Look for errors:
   - "Invalid public key" → Wrong key
   - "Template not found" → Wrong template ID
   - "Service not found" → Wrong service ID
```

---

### **Problem: "401 Unauthorized" Error**

**Solution:**
```
1. Public Key is wrong
2. Go to EmailJS → Account → API Keys
3. Copy Public Key AGAIN carefully
4. Update in index.html line ~217
5. Make sure no extra spaces
6. Save and upload
```

---

### **Problem: "Template Not Found" Error**

**Solution:**
```
1. Template ID is wrong
2. Go to EmailJS → Email Templates
3. Click on template
4. Copy Template ID exactly
5. Update in index.html
6. Admin template at line ~301
7. Customer template at line ~336
8. Save and upload
```

---

### **Problem: Emails Going to Spam**

**Solution:**
```
1. Mark EmailJS emails as "Not Spam"
2. Add noreply@emailjs.com to contacts
3. Add aminfx.gh@gmail.com to contacts
4. Future emails will go to inbox
```

---

### **Problem: Gmail Not Connecting**

**Solution:**
```
1. EmailJS Dashboard → Email Services
2. Click on Gmail service
3. Click "Reconnect"
4. Login to Google again
5. Allow permissions
6. Should reconnect
```

---

## 📊 QUICK REFERENCE CARD

**Save this for easy access:**

```
═══════════════════════════════════════════════
EMAILJS CREDENTIALS
═══════════════════════════════════════════════

EmailJS Account: aminfx.gh@gmail.com
Password: (your EmailJS password)

Public Key: _________________
Service ID: _________________
Admin Template ID: _________________
Customer Template ID: _________________

═══════════════════════════════════════════════
CODE LOCATIONS IN index.html
═══════════════════════════════════════════════

Line ~217: emailjs.init("PUBLIC_KEY");
Line ~301: emailjs.send('SERVICE_ID', 'ADMIN_TEMPLATE_ID', {
Line ~336: emailjs.send('SERVICE_ID', 'CUSTOMER_TEMPLATE_ID', {

═══════════════════════════════════════════════
EMAIL TEMPLATES
═══════════════════════════════════════════════

Admin: admin_new_purchase
- Sent when customer submits purchase
- Goes to: aminfx.gh@gmail.com

Customer: customer_activation  
- Sent when admin approves
- Goes to: customer's email
- Includes VPS link

═══════════════════════════════════════════════
TESTING
═══════════════════════════════════════════════

1. EmailJS Dashboard → Email Templates
2. Click template → "Test Email"
3. Fill test values
4. Send
5. Check inbox (and spam)

═══════════════════════════════════════════════
```

---

## ✅ FINAL CHECKLIST

```
□ Created EmailJS account
□ Verified email
□ Connected Gmail service
□ Copied Service ID
□ Created admin_new_purchase template
□ Copied Admin Template ID
□ Created customer_activation template  
□ Copied Customer Template ID
□ Got Public Key from Account page
□ Updated line ~217 with Public Key
□ Updated line ~301 with Service ID + Admin Template ID
□ Updated line ~336 with Service ID + Customer Template ID
□ Saved index.html
□ Uploaded to hosting
□ Tested admin notification email
□ Tested customer activation email
□ Tested full purchase flow on live site
□ Verified emails arriving
□ ✅ EMAILS WORKING!
```

---

## 🎊 SUCCESS!

**When everything works, you'll have:**

1. ✅ Customer submits purchase → You get email notification
2. ✅ You approve purchase → Customer gets activation email with:
   - License key
   - Broker/Server binding info
   - VPS recommendation with YOUR referral link
   - Download link
   - WhatsApp group link

**Professional, automated, and hands-free!**

---

## 📞 NEED HELP?

**If stuck:**

1. **Check Browser Console**
   - F12 → Console tab
   - Look for red errors
   - Google the error message

2. **Re-verify All IDs**
   - Public Key
   - Service ID  
   - Both Template IDs
   - Must match EXACTLY

3. **Test Templates in EmailJS**
   - Use "Test Email" feature
   - If test works, code is wrong
   - If test fails, template is wrong

4. **Check Email Service**
   - Gmail must be "Connected"
   - If disconnected, reconnect it

---

**🔥 FOLLOW THIS GUIDE AND EMAILS WILL WORK! 🔥**

**📧 COMPLETE EMAILJS SETUP IN 15 MINUTES! 📧**

**✅ PROFESSIONAL AUTOMATED EMAILS! ✅**
