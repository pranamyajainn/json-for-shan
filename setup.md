# 🚀 SmartScore.ai Partnership Workflow - Setup Guide

**Duration:** 15-20 minutes  
**Difficulty:** Easy ⭐⭐  
**Platform:** Make.com  

---

## What This Workflow Does

This automation helps you:
1. ✅ Monitor a Google Sheet for new company leads
2. ✅ Fetch company websites automatically
3. ✅ Analyze company details with AI
4. ✅ Generate personalized partnership emails
5. ✅ Save results back to Google Sheets
6. ✅ Send emails automatically

---

## 🚀 Setup Instructions (4 Simple Steps)

### **Step 1: Import the Workflow (2 minutes)**

1. Open **Make.com** in your browser
2. Click **Create a new scenario** (top right)
3. Click the **gear icon** (bottom left area)
4. Click **Import Blueprint**
5. Paste the provided JSON file
6. Click **Import**

✅ **Result:** You'll see 8 connected modules in your scenario

---

### **Step 2: Connect Google Sheets (3 minutes)**

#### Module 9 (Watch for new rows):
1. Click on **Module 9** (first blue box labeled "google-sheets:watchRows")
2. On the right panel, find **"Connection"**
3. Click the dropdown arrow
4. You'll see existing Google connections OR **"Add"** button
5. Select a Google connection (or create one if needed)
6. Scroll down and click **OK** or **Save**

#### Module 8 (Save results):
1. Click on **Module 8** (blue box labeled "google-sheets:addRow")
2. Find **"Connection"** on the right
3. Click the dropdown
4. **Select the SAME Google connection** as Module 9
5. Click **OK** or **Save**

✅ **Google Sheets is now connected!**

---

### **Step 3: Connect OpenAI (3 minutes)**

#### Module 5 (AI Analysis):
1. Click on **Module 5** (purple box labeled "openai-gpt-3:CreateCompletion")
2. Find **"Connection"** on the right
3. Click the dropdown
4. Select your OpenAI connection OR **Add** a new one
5. Click **OK** or **Save**

#### Module 7 (Email Generation):
1. Click on **Module 7** (next purple box labeled "openai-gpt-3:CreateCompletion")
2. Repeat the same steps as Module 5
3. **Use the SAME OpenAI connection**
4. Click **OK** or **Save**

✅ **OpenAI is now connected!**

---

### **Step 4: Connect Zoho Mail (5 minutes) - MOST IMPORTANT** 🎯

#### Module 11 (Send Email):
1. Click on **Module 11** (green/teal box labeled "zoho-mail:sendMail")
2. Find **"Connection"** on the right panel
3. Click the dropdown arrow

**You'll see 2 scenarios:**

**Scenario A: If you see "Zoho Mail" in the dropdown**
- Simply click to select it
- Click **OK** or **Save**
- ✅ Done!

**Scenario B: If you DON'T see "Zoho Mail" connection**
- Click the **"Add"** button
- You'll see app list → Search for **"Zoho Mail"**
- Click **Zoho Mail** to add it
- You'll be taken to Zoho login page
- **Login with your Zoho account** (the one sending emails)
- Click **"Allow"** to authorize
- You'll be redirected back to Make.com
- The connection will auto-select
- Click **OK** or **Save**
- ✅ Done!

✅ **Zoho Mail is now connected!**

---

## 📊 Test Your Workflow (5 minutes)

### Step 1: Add a Test Row to Google Sheets

1. Open your **source Google Sheet** (the one you connected in Module 9)
2. Add a new row with this test data:
   - **Column A (Name):** "Test Company"
   - **Column B (Email):** your-email@example.com
   - **Column C (Website):** smartscore.ai
3. Leave other columns empty (optional)

### Step 2: Run the Test

1. Go back to **Make.com**
2. At the bottom of the screen, click the **Play/Run button** (▶️)
3. Watch each module execute (they'll light up in sequence)

### Step 3: Check If It Worked

Watch for these green checkmarks ✅:
- ✅ **Module 9:** Found your test row
- ✅ **Module 10:** Set the URL correctly
- ✅ **Module 3:** Fetched the website
- ✅ **Module 4:** Extracted text from website
- ✅ **Module 5:** Generated AI analysis
- ✅ **Module 7:** Created personalized email
- ✅ **Module 8:** Saved results to output sheet
- ✅ **Module 11:** Sent email successfully

### Step 4: Check Your Email

You should receive an email like this:

```
Subject: Partnership Exploration: Let's Build Something That Matters

Hey [Company Contact Name],

I came across [their specific product], and I was impressed 
by how it [positive outcome]...

[Personalized content about SmartScore.ai partnership]

Best regards,
Deasa M
Co-Founder and CRO | SmartScore.AI
```

---

## 🎯 Enable Automation (Schedule It)

After testing, follow these steps to run it automatically:

1. Click the **clock icon** ⏰ (bottom left of Make.com)
2. Select **"How often should the scenario run?"**
3. Choose:
   - **Every 15 minutes** (for active lead lists)
   - **Every hour** (standard)
   - **Daily** (for daily lead batches)
4. Click **Save**
5. Toggle the **ON/OFF switch** to **ON** (blue)

**Now the workflow runs automatically on your schedule!**

---

## 📊 Workflow Flow

```
You add a row to Google Sheet
        ↓
Workflow detects new row
        ↓
Fetches company website
        ↓
Extracts website content
        ↓
AI analyzes the company
        ↓
AI generates personalized email
        ↓
Saves analysis to results sheet
        ↓
Sends email automatically
        ↓
✅ DONE!
```

---

## 🆘 Troubleshooting Guide

### ❌ "Connection not found" or "Connection failed"

**Problem:** One of your connections isn't configured correctly

**Fix:**
1. Click the module with the error (red X)
2. Find the **"Connection"** dropdown
3. Re-select or re-add the connection
4. Click **OK** or **Save**
5. Run the test again

---

### ❌ Email not sent (Module 11 error)

**Problem:** Zoho Mail connection issue

**Fix:**
1. Open Zoho Mail account (zoho.com)
2. Check if your account is active
3. In Make.com, delete the Zoho connection and re-add it
4. Make sure you're logged into the correct Zoho account

---

### ❌ Website fetch timeout (Module 3 error)

**Problem:** Website is slow or unreachable

**Fix:** This is normal - the workflow will skip that row and continue with the next one

---

### ❌ OpenAI quota exceeded

**Problem:** You've used all your OpenAI API credits

**Fix:** Add credits to your OpenAI account at platform.openai.com

---

### ❌ "Sheet not found" (Module 8 error)

**Problem:** Output sheet doesn't exist or wrong sheet name

**Fix:**
1. Make sure you have a "Sheet3" or rename the output sheet
2. In Module 8, update the sheet name in settings

---

## 📝 Important Notes

✅ **Your passwords are safe** - They're encrypted in Make.com  
✅ **Only YOU can trigger this** - It's secure  
✅ **API costs are minimal** - OpenAI charges per request (usually <$0.01 per email)  
✅ **You control the schedule** - Run it every 15 mins or daily, your choice  

---

## ✅ Workflow Is Now Live!

**Your automation will:**
- 🔄 Check for new leads every 15 minutes (or your chosen schedule)
- 📧 Generate personalized emails for each lead
- 💾 Save results automatically
- 📤 Send emails without any manual work

**Start adding leads to your Google Sheet and watch it work!**

---

## 📞 Quick Reference

| What | Where |
|------|-------|
| Run manually | Click ▶️ button (bottom left) |
| Change schedule | Click ⏰ icon (bottom left) |
| Turn on/off | Toggle ON/OFF switch (bottom left) |
| View results | Check Module 8 output sheet (Sheet3) |
| Check logs | Click "Execution History" at bottom |

---

**Setup Complete! You're ready to go! 🎉**
