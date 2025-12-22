# ⚡ EMAILJS QUICK SETUP (15 MINUTES)

## 🎯 WHAT YOU NEED

3 Steps:
1. Setup EmailJS account (5 min)
2. Update website code (5 min)  
3. Test emails (5 min)

---

## 📝 STEP 1: EMAILJS ACCOUNT (5 MIN)

### **A. Sign Up**
```
→ Go to: https://www.emailjs.com/
→ Click "Sign Up"
→ Email: aminfx.gh@gmail.com
→ Password: (create one)
→ Verify email
✅ Done!
```

### **B. Connect Gmail**
```
→ Dashboard → "Email Services"
→ Click "Add New Service"
→ Select "Gmail"
→ Click "Connect Account"
→ Login to Google
→ Allow permissions
→ ✅ Copy Service ID: service_______
   Write it down!
```

### **C. Create Admin Template**
```
→ Dashboard → "Email Templates"
→ Click "Create New Template"
→ Name: admin_new_purchase

Settings:
- To Email: {{to_email}}
- From Name: Wolf FX System
- Subject: 🔔 New Purchase - {{plan}}

Content: (copy from EMAILJS_COMPLETE_GUIDE.md)

→ Click "Save"
→ ✅ Copy Template ID: template_______
   Write it down!
```

### **D. Create Customer Template**
```
→ Click "Create New Template" again
→ Name: customer_activation

Settings:
- To Email: {{to_email}}
- From Name: Wolf FX Trading Academy
- Subject: 🎉 Your License is Activated!

Content: (copy from EMAILJS_COMPLETE_GUIDE.md)

→ Click "Save"
→ ✅ Copy Template ID: template_______
   Write it down!
```

### **E. Get Public Key**
```
→ Dashboard → "Account"
→ Find "API Keys" section
→ ✅ Copy Public Key: ________________
   Write it down!
```

---

## 🔧 STEP 2: UPDATE WEBSITE (5 MIN)

### **You Now Have:**
```
✓ Public Key: ________________
✓ Service ID: ________________
✓ Admin Template ID: ________________
✓ Customer Template ID: ________________
```

### **Update index.html:**

**Change 1 - Line ~217:**
```javascript
// FIND:
emailjs.init("YOUR_PUBLIC_KEY");

// REPLACE WITH:
emailjs.init("YOUR_ACTUAL_PUBLIC_KEY");
```

**Change 2 - Line ~301:**
```javascript
// FIND:
emailjs.send('YOUR_SERVICE_ID', 'YOUR_ADMIN_TEMPLATE_ID', {

// REPLACE WITH:
emailjs.send('service_abc123', 'template_xyz789', {
```

**Change 3 - Line ~336:**
```javascript
// FIND:
emailjs.send('YOUR_SERVICE_ID', 'YOUR_ACTIVATION_TEMPLATE_ID', {

// REPLACE WITH:
emailjs.send('service_abc123', 'template_def456', {
```

**Save & Upload:**
```
→ Save index.html
→ Upload to Netlify/GitHub
→ Wait 1 minute
✅ Done!
```

---

## ✅ STEP 3: TEST EMAILS (5 MIN)

### **A. Test in EmailJS Dashboard**
```
→ EmailJS → Email Templates
→ Click "admin_new_purchase"
→ Click "Test Email"
→ Fill test values
→ Click "Send"
→ Check your email
✅ Email arrived? Admin template works!

→ Click "customer_activation"
→ Click "Test Email"  
→ Fill test values
→ Click "Send"
→ Check your email
✅ Email arrived? Customer template works!
```

### **B. Test on Live Site**
```
→ Go to your website
→ Create test account
→ Make test purchase
→ Check email
✅ Admin notification received?

→ Login as admin
→ Approve the test purchase
→ Check email
✅ Activation email received?

→ If BOTH emails work: SUCCESS! 🎉
```

---

## 🐛 QUICK TROUBLESHOOTING

**No emails?**
```
✓ Check spam folder
✓ Verify Service ID is correct
✓ Verify Template IDs are correct
✓ Verify Public Key is correct
✓ Check browser console (F12) for errors
```

**"401 Unauthorized"?**
```
→ Public Key is wrong
→ Copy it again from EmailJS
→ Update in index.html
```

**"Template not found"?**
```
→ Template ID is wrong
→ Copy it again from EmailJS
→ Update in index.html
```

---

## 📋 COPY & PASTE TEMPLATE

**Save this and fill in your values:**

```javascript
// ═══════════════════════════════════
// EMAILJS CONFIGURATION
// ═══════════════════════════════════

// Line ~217:
emailjs.init("YOUR_PUBLIC_KEY_HERE");

// Line ~301:
emailjs.send('YOUR_SERVICE_ID', 'YOUR_ADMIN_TEMPLATE_ID', {

// Line ~336:
emailjs.send('YOUR_SERVICE_ID', 'YOUR_CUSTOMER_TEMPLATE_ID', {

// ═══════════════════════════════════
// YOUR VALUES:
// ═══════════════════════════════════

Public Key: ________________
Service ID: ________________
Admin Template ID: ________________
Customer Template ID: ________________
```

---

## 🎯 FINAL RESULT

**When Working:**

Customer submits:
→ 📧 You get email: "New Purchase - Verify TX ID"

You approve:
→ 📧 Customer gets email: "License Activated + VPS Link"

**Fully automated! 🎉**

---

## ⚡ SUPER QUICK VERSION

```
1. emailjs.com → Sign up
2. Connect Gmail → Copy Service ID
3. Create 2 templates → Copy Template IDs
4. Get Public Key → Copy it
5. Update 3 lines in index.html
6. Upload file
7. Test emails
✅ Done! (15 minutes)
```

---

**🔥 FOLLOW THESE 3 STEPS AND EMAILS WILL WORK! 🔥**

**Need detailed instructions? See: EMAILJS_COMPLETE_GUIDE.md**
