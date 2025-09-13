# Professional Contact Form Setup

## Quick Setup (5 minutes)

### 1. Create EmailJS Account
- Go to [emailjs.com](https://www.emailjs.com/)
- Sign up with your Gmail account
- Verify your email

### 2. Add Gmail Service
- Dashboard → "Email Services" → "Add New Service"
- Choose "Gmail"
- Connect your Gmail account
- Copy the **Service ID** (e.g., `service_abc123`)

### 3. Create Professional Email Template
- Dashboard → "Email Templates" → "Create New Template"
- **Subject:** `New Portfolio Contact: {{subject}}`
- **Content:**
```
From: {{from_name}} ({{from_email}})
Subject: {{subject}}

Message:
{{message}}

---
Sent from your portfolio website
```

### 4. Get Your Public Key
- Dashboard → "Account" → Copy **Public Key** (e.g., `user_xyz789`)

### 5. Update Your Code
Open `script.js` and replace these lines:

```javascript
// Line 121: Replace with your public key
emailjs.init("user_xyz789");

// Line 169: Replace with your service and template IDs
emailjs.send('service_abc123', 'template_def456', templateParams)
```

### 6. Test
- Fill out the contact form
- Click "Send Message"
- Check your Gmail inbox

## Professional Features Included

✅ **Real-time email delivery** to mensaho313@gmail.com
✅ **Professional notifications** with success/error messages
✅ **Form validation** with email format checking
✅ **Loading states** with "Sending..." button
✅ **Auto-reset** after successful submission
✅ **Fallback email link** if EmailJS fails
✅ **Mobile responsive** design

## Troubleshooting

**Email not received?**
- Check spam folder
- Verify Gmail service is connected
- Check browser console for errors

**Form not working?**
- Ensure all IDs are correctly updated
- Check EmailJS dashboard for error logs
- Verify template is published

Your contact form will send professional emails directly to your inbox!
