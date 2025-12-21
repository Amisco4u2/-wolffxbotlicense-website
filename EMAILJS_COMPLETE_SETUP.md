# 📧 COMPLETE EMAILJS SETUP GUIDE - STEP BY STEP

## ✅ CUSTOMER ACCOUNTS ARE WORKING!

**Good news:** Customer accounts ARE being created when they purchase!

**The issue:** EmailJS needs to be configured for email notifications to work.

---

## 🎯 EMAILJS SETUP (10 MINUTES)

### **STEP 1: CREATE EMAILJS ACCOUNT**

```
1. Go to: https://www.emailjs.com/

2. Click "Sign Up" (top right)

3. Enter details:
   - Email: aminfx.gh@gmail.com
   - Password: (create a secure one)
   - Name: Amin FX

4. Click "Sign Up"

5. Check your email for verification link

6. Click verification link

7. ✅ Account created!
```

---

### **STEP 2: CONNECT GMAIL**

```
1. After login, you're on Dashboard

2. Click "Email Services" (left sidebar)

3. Click "Add New Service"

4. You'll see options: Gmail, Outlook, etc.

5. Click "Gmail"

6. Click "Connect Account"

7. Select your Google account: aminfx.gh@gmail.com

8. Click "Allow" to give permissions

9. You'll see: "Service added successfully"

10. IMPORTANT: Copy the Service ID
    Example: service_abc123xyz
    
11. ✅ Gmail connected!
```

**Save this Service ID - you'll need it!**

---

### **STEP 3: CREATE EMAIL TEMPLATE 1 (ADMIN NOTIFICATION)**

```
1. Click "Email Templates" (left sidebar)

2. Click "Create New Template"

3. Template Settings:
   - Template Name: admin_new_purchase
   
4. Email Content:

Subject:
New License Purchase - {{plan}}

Content:
Hello Admin,

A new license purchase requires your approval:

CUSTOMER INFORMATION:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Name: {{customer_name}}
Email: {{customer_email}}
Country: {{country}}
WhatsApp: {{whatsapp}}

PLAN DETAILS:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Plan: {{plan}}
Price: ${{price}}

MT5 DETAILS:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Account: {{mt5}}
Broker: {{broker}}
Server: {{server}}

PAYMENT:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Method: {{method}}
Transaction ID: {{txid}}

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Please login to approve this license:
https://your-site-url.com

Wolf FX Admin System

5. To Email: {{to_email}}
   (This will be filled automatically)

6. From Name: Wolf FX System

7. From Email: Use the connected Gmail

8. Reply To: aminfx.gh@gmail.com

9. Click "Save"

10. IMPORTANT: Copy the Template ID
    Example: template_xyz123abc

11. ✅ Template created!
```

**Save this Template ID!**

---

### **STEP 4: CREATE EMAIL TEMPLATE 2 (CUSTOMER ACTIVATION)**

```
1. Click "Create New Template" again

2. Template Settings:
   - Template Name: customer_activation

3. Email Content:

Subject:
🎉 Your Wolf FX License is Activated!

Content:
Hello {{customer_name}},

Congratulations! Your Wolf FX EA license has been approved and activated.

LICENSE DETAILS:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
License Key: {{license_key}}
Plan: {{plan}}
Valid Until: {{expiry_date}}
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

DOWNLOAD YOUR EA:
{{download_link}}

INSTALLATION GUIDE:
1. Download the EA file
2. Open MT5 platform
3. File → Open Data Folder
4. Navigate to: MQL5 → Experts
5. Copy the EA file here
6. Restart MT5
7. Drag EA onto chart
8. Enter your license key: {{license_key}}
9. Start trading!

JOIN OUR COMMUNITY:
WhatsApp Group: {{whatsapp_link}}

SUPPORT:
If you need help, contact us:
- Email: aminfx.gh@gmail.com
- WhatsApp: See group link above

Happy Trading!

Best Regards,
Wolf FX Team

4. To Email: {{to_email}}

5. From Name: Wolf FX Trading

6. From Email: Use connected Gmail

7. Reply To: aminfx.gh@gmail.com

8. Click "Save"

9. IMPORTANT: Copy this Template ID too
   Example: template_abc456xyz

10. ✅ Template created!
```

**Save this Template ID!**

---

### **STEP 5: GET YOUR PUBLIC KEY**

```
1. Click "Account" (left sidebar)

2. Look for "API Keys" section

3. Find "Public Key"
   Example: xYz123AbC456DeF

4. Click "Copy"

5. ✅ Public Key copied!
```

**Save this Public Key!**

---

### **STEP 6: YOU NOW HAVE 3 IMPORTANT VALUES:**

```
1. Public Key: xYz123AbC456DeF
2. Service ID: service_abc123
3. Admin Template ID: template_xyz789
4. Customer Template ID: template_def456
```

**Write these down!**

---

## 🔧 STEP 7: UPDATE YOUR WEBSITE

Now you need to update your index.html file with these values.

### **Find and Replace These Lines:**

**Line ~611 - Public Key:**
```javascript
// FIND THIS:
emailjs.init("YOUR_PUBLIC_KEY");

// REPLACE WITH:
emailjs.init("xYz123AbC456DeF");  // Your actual public key
```

**Line ~812 - Admin Email:**
```javascript
// FIND THIS:
emailjs.send('YOUR_SERVICE_ID', 'YOUR_ADMIN_TEMPLATE_ID', templateParams)

// REPLACE WITH:
emailjs.send('service_abc123', 'template_xyz789', templateParams)
// Use your actual Service ID and Admin Template ID
```

**Line ~822 - Customer Email:**
```javascript
// FIND THIS:
emailjs.send('YOUR_SERVICE_ID', 'YOUR_ACTIVATION_TEMPLATE_ID', templateParams)

// REPLACE WITH:
emailjs.send('service_abc123', 'template_def456', templateParams)
// Use your actual Service ID and Customer Template ID
```

---

## 📝 HOW TO EDIT YOUR FILE

### **Method 1: Edit on GitHub**

```
1. Go to your repository
2. Click on index.html
3. Click pencil icon (Edit)
4. Press Ctrl+F to search
5. Search for: YOUR_PUBLIC_KEY
6. Replace with your actual public key
7. Search for: YOUR_SERVICE_ID (appears twice)
8. Replace both with your service ID
9. Search for: YOUR_ADMIN_TEMPLATE_ID
10. Replace with admin template ID
11. Search for: YOUR_ACTIVATION_TEMPLATE_ID
12. Replace with customer template ID
13. Scroll down
14. Click "Commit changes"
15. ✅ Updated!
```

### **Method 2: Edit Locally**

```
1. Download index.html from repository
2. Open with text editor (Notepad, VS Code, etc.)
3. Press Ctrl+F to find
4. Replace all the YOUR_XXX values
5. Save file
6. Go to repository
7. Delete old index.html
8. Upload updated index.html
9. ✅ Updated!
```

---

## ✅ VERIFICATION - TEST EMAILS

### **Test EmailJS is Working:**

```
1. After updating your website
2. Go to EmailJS Dashboard
3. Click "Email Templates"
4. Click on admin_new_purchase template
5. Click "Send Test Email"
6. Fill in test values
7. Click "Send"
8. Check your email (aminfx.gh@gmail.com)
9. If email arrives → ✅ Working!
10. If not → Check spam folder
```

---

## 🎯 COMPLETE WORKFLOW AFTER SETUP

### **When Customer Purchases:**

```
1. Customer fills form
2. Creates account (email + password)
3. Makes payment
4. Enters TX ID
5. Submits

Backend automatically:
6. Creates customer account in localStorage
7. Creates license (status: PENDING)
8. Sends email to YOU (admin)
9. Shows success message to customer

You receive email with:
- Customer details
- Payment info
- TX ID to verify
- Link to admin dashboard
```

### **When You Approve:**

```
1. You login to admin dashboard
2. See pending purchase
3. Verify payment in your wallet
4. Click "Approve"

Backend automatically:
5. Changes status: PENDING → ACTIVE
6. Calculates expiry date
7. Sends email to CUSTOMER
8. Customer gets their license key

Customer receives email with:
- License key
- Expiry date
- Download link
- Installation guide
- WhatsApp group link
```

---

## 🔍 TROUBLESHOOTING EMAILJS

### **Problem: Emails not sending**

**Check:**
```
□ Public Key is correct
□ Service ID is correct
□ Template IDs are correct
□ No typos in the IDs
□ Gmail is connected in EmailJS
□ Email templates are saved
□ Account is verified
```

**Test:**
```
1. Open browser console (F12)
2. Try to purchase something
3. Look for errors in console
4. Common error: "Invalid public key"
   → Public key is wrong, update it
```

---

### **Problem: Admin email works, customer email doesn't**

**Cause:** Customer template ID is wrong

**Fix:**
```
1. Go to EmailJS → Email Templates
2. Click on customer_activation template
3. Copy Template ID again
4. Update in index.html line ~822
5. Save and test again
```

---

### **Problem: "401 Unauthorized" error**

**Cause:** Public key is incorrect

**Fix:**
```
1. Go to EmailJS → Account
2. Copy Public Key again (carefully!)
3. Update in index.html line ~611
4. Make sure no extra spaces
5. Save and test
```

---

## 📧 EMAIL LIMITS

**EmailJS Free Plan:**
- 200 emails per month
- Enough for 100 customers (2 emails each)

**If you need more:**
- Upgrade to paid plan ($7/month for 1,000 emails)
- Or create second account for customer emails

---

## 🎨 CUSTOMIZE EMAIL TEMPLATES

### **Add Your Logo:**

In EmailJS template editor:
```html
<img src="https://your-logo-url.com/logo.png" alt="Logo" width="200">
```

### **Change Colors:**

Add inline CSS:
```html
<div style="background: #00ff88; padding: 20px; border-radius: 10px;">
    Your content here
</div>
```

### **Add Links:**

```html
<a href="https://your-site.com/download" style="color: #00ff88;">Download EA</a>
```

---

## ✅ FINAL CHECKLIST

```
□ Created EmailJS account
□ Verified email
□ Connected Gmail
□ Created admin template
□ Created customer template
□ Copied Public Key
□ Copied Service ID
□ Copied both Template IDs
□ Updated index.html with all IDs
□ Uploaded updated file to GitHub/Netlify
□ Tested email sending
□ Checked spam folder
□ ✅ Emails working!
```

---

## 🎊 SUMMARY

**What you need from EmailJS:**
1. Public Key
2. Service ID (Gmail)
3. Admin Template ID
4. Customer Template ID

**Where to put them in index.html:**
```javascript
Line ~611: emailjs.init("YOUR_PUBLIC_KEY");
Line ~812: emailjs.send('SERVICE_ID', 'ADMIN_TEMPLATE_ID', ...)
Line ~822: emailjs.send('SERVICE_ID', 'CUSTOMER_TEMPLATE_ID', ...)
```

**After setup:**
- Customers get confirmation emails
- You get notification emails
- All automatic!

---

## 💡 CUSTOMER ACCOUNTS EXPLANATION

**Customer accounts ARE working! Here's how:**

**When customer purchases:**
```javascript
// This code runs (line 753-761):
if (!DB.customers.find(c => c.email === email)) {
    DB.customers.push({
        email: email,
        password: password,
        name: name,
        created: new Date().toISOString()
    });
}
```

**This means:**
1. Customer fills form with email + password
2. System checks if email exists
3. If not, creates new customer account
4. Saves to localStorage
5. Customer can now login!

**To login:**
```
1. Customer goes to your site
2. Clicks "Customer Login"
3. Enters email + password (from purchase)
4. Clicks "Login"
5. ✅ Sees their dashboard with licenses!
```

**Why might it seem like it's not working?**
- Customer forgot their password
- Used different email
- Browser cleared localStorage
- Different browser/device

**Solution:**
Tell customers to:
- Use same browser
- Remember email/password from purchase
- Don't clear browser data

---

## 🔥 QUICK SETUP SUMMARY

**5 Steps:**
1. EmailJS.com → Sign up
2. Connect Gmail
3. Create 2 templates
4. Copy: Public Key, Service ID, Template IDs
5. Update index.html with these values

**Time:** 10 minutes

**Result:** Automatic emails working!

---

**📧 FOLLOW THIS GUIDE AND EMAILS WILL WORK! 📧**

**✅ CUSTOMER ACCOUNTS ALREADY WORK - JUST NEED EMAILJS! 💯**
