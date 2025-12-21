# ⚡ EMAILJS QUICK UPDATE GUIDE

## 🎯 WHAT YOU NEED

After setting up EmailJS, you'll have these 4 values:

```
1. Public Key:           ABC123XYZ456
2. Service ID:           service_abc123
3. Admin Template ID:    template_xyz789
4. Customer Template ID: template_def456
```

---

## 📝 WHERE TO UPDATE IN INDEX.HTML

### **UPDATE 1: Line ~611 - Initialize EmailJS**

**FIND:**
```javascript
emailjs.init("YOUR_PUBLIC_KEY");
```

**REPLACE WITH:**
```javascript
emailjs.init("ABC123XYZ456");
```
*Use YOUR actual Public Key*

---

### **UPDATE 2: Line ~812 - Admin Email Function**

**FIND:**
```javascript
emailjs.send('YOUR_SERVICE_ID', 'YOUR_ADMIN_TEMPLATE_ID', templateParams)
```

**REPLACE WITH:**
```javascript
emailjs.send('service_abc123', 'template_xyz789', templateParams)
```
*Use YOUR actual Service ID and Admin Template ID*

---

### **UPDATE 3: Line ~822 - Customer Email Function**

**FIND:**
```javascript
emailjs.send('YOUR_SERVICE_ID', 'YOUR_ACTIVATION_TEMPLATE_ID', templateParams)
```

**REPLACE WITH:**
```javascript
emailjs.send('service_abc123', 'template_def456', templateParams)
```
*Use YOUR actual Service ID and Customer Template ID*

---

## 🔧 HOW TO EDIT

### **Option 1: Edit on GitHub**
```
1. Go to repository
2. Click index.html
3. Click pencil icon (Edit)
4. Press Ctrl+F
5. Search: YOUR_PUBLIC_KEY
6. Replace with your key
7. Search: YOUR_SERVICE_ID (2 times!)
8. Replace both with your service ID
9. Search: YOUR_ADMIN_TEMPLATE_ID
10. Replace with admin template ID
11. Search: YOUR_ACTIVATION_TEMPLATE_ID
12. Replace with customer template ID
13. Commit changes
14. ✅ Done!
```

### **Option 2: Edit on Netlify**
```
1. Download index.html from Netlify
2. Open in text editor
3. Find and replace all 4 values
4. Save file
5. Drag to Netlify Drop
6. ✅ Done!
```

---

## ✅ VERIFICATION

**After updating, test:**

```
1. Try to purchase something (use fake details)
2. Fill all fields
3. Submit
4. Check console (F12) for errors
5. Check your email (aminfx.gh@gmail.com)
6. Should receive notification
7. ✅ Working!
```

---

## 🎊 COMPLETE EXAMPLE

**If your EmailJS values are:**
```
Public Key: xYz789AbC123
Service ID: service_wolffx
Admin Template: template_admin123
Customer Template: template_customer456
```

**Your code should be:**

```javascript
// Line ~611
emailjs.init("xYz789AbC123");

// Line ~812
emailjs.send('service_wolffx', 'template_admin123', templateParams)

// Line ~822
emailjs.send('service_wolffx', 'template_customer456', templateParams)
```

---

## 🔍 FIND EXACT LINES

**Use Ctrl+F and search for these:**

1. Search: `emailjs.init("YOUR_PUBLIC_KEY")`
   → Replace `YOUR_PUBLIC_KEY` with your key

2. Search: `YOUR_SERVICE_ID`
   → Will find 2 occurrences
   → Replace both

3. Search: `YOUR_ADMIN_TEMPLATE_ID`
   → Replace with admin template ID

4. Search: `YOUR_ACTIVATION_TEMPLATE_ID`
   → Replace with customer template ID

---

## 💡 COMMON MISTAKES

❌ **Wrong:** Leaving quotes inside quotes
```javascript
emailjs.init(""ABC123"");  // WRONG!
```

✅ **Right:** Just the value
```javascript
emailjs.init("ABC123");  // CORRECT!
```

❌ **Wrong:** Extra spaces
```javascript
emailjs.init(" ABC123 ");  // WRONG!
```

✅ **Right:** No spaces
```javascript
emailjs.init("ABC123");  // CORRECT!
```

---

## ⚡ FASTEST METHOD

**Copy this template and fill in your values:**

```javascript
// Save this, then copy-paste into your file

// Line ~611 - REPLACE THIS LINE:
emailjs.init("YOUR_PUBLIC_KEY_HERE");

// Line ~812 - REPLACE THIS LINE:
emailjs.send('YOUR_SERVICE_ID_HERE', 'YOUR_ADMIN_TEMPLATE_ID_HERE', templateParams)

// Line ~822 - REPLACE THIS LINE:
emailjs.send('YOUR_SERVICE_ID_HERE', 'YOUR_CUSTOMER_TEMPLATE_ID_HERE', templateParams)
```

**Then:**
1. Fill in YOUR values
2. Copy each line
3. Find the corresponding line in index.html
4. Replace it
5. ✅ Done!

---

## 📧 EMAIL TEMPLATE VARIABLES

**Make sure your EmailJS templates have these variables:**

**Admin Template:**
```
{{customer_name}}
{{customer_email}}
{{plan}}
{{price}}
{{txid}}
{{mt5}}
{{broker}}
{{server}}
{{to_email}}
```

**Customer Template:**
```
{{customer_name}}
{{license_key}}
{{plan}}
{{expiry_date}}
{{download_link}}
{{whatsapp_link}}
{{to_email}}
```

---

## ✅ CHECKLIST

```
□ Got Public Key from EmailJS
□ Got Service ID from EmailJS
□ Got Admin Template ID from EmailJS
□ Got Customer Template ID from EmailJS
□ Updated line ~611 with Public Key
□ Updated line ~812 with Service ID + Admin Template
□ Updated line ~822 with Service ID + Customer Template
□ Saved file
□ Uploaded to GitHub/Netlify
□ Tested with purchase
□ Received email
□ ✅ Working!
```

---

**🔥 JUST UPDATE THESE 3 LINES AND EMAILS WILL WORK! 🔥**

**✅ SUPER SIMPLE - TAKES 2 MINUTES! 💯**
