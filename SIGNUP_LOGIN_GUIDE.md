# 🔐 Complete Signup & Login System Guide

## 📌 Overview
This school management website now features a **complete signup and login system** where users must register with their email and password before they can access their portals.

---

## ✨ Key Features

✅ **Email-based Registration** - Students and teachers signup with email  
✅ **Password Protection** - Secure password authentication  
✅ **Persistent Storage** - Data saved in browser's localStorage  
✅ **Session Management** - Login sessions maintained  
✅ **Duplicate Prevention** - No duplicate emails or roll numbers  
✅ **Real-time Validation** - Form validation on submit  
✅ **Auto-login After Signup** - Redirects to login after successful signup  

---

## 👨‍🎓 For Students

### Step 1: Signup
1. Go to `student-signup.html` or click "Signup here" on login page
2. Fill in the registration form:
   - **Full Name**: Your complete name
   - **Email Address**: Your email (will be used for login)
   - **Roll Number**: Your student roll number
   - **Class**: Select your class (Nursery to 12)
   - **Password**: Create a password (minimum 6 characters)
   - **Confirm Password**: Re-enter your password
3. Accept Terms & Conditions
4. Click "Create Account"
5. You'll see a success message with your details
6. You'll be redirected to the login page

### Step 2: Login
1. Go to `student-login.html`
2. Enter your **email** OR **roll number**
3. Enter your **password**
4. Click "Login"
5. You'll be redirected to `student-dashboard.html`

### Example:
```
SIGNUP:
- Name: Rahul Kumar
- Email: rahul.kumar@student.bfa.edu.in
- Roll Number: 2024101
- Class: 10
- Password: student@123

LOGIN:
- Username: rahul.kumar@student.bfa.edu.in (or 2024101)
- Password: student@123
```

---

## 👨‍🏫 For Teachers

### Step 1: Signup
1. Go to `teacher-signup.html` or click "Signup here" on login page
2. Fill in the registration form:
   - **Full Name**: Your complete name
   - **Email Address**: Your email (will be used for login)
   - **Employee ID**: Your employee ID number
   - **Subject/Department**: Your teaching subject
   - **Phone Number**: 10-digit phone number
   - **Password**: Create a password (minimum 6 characters)
   - **Confirm Password**: Re-enter your password
3. Accept Terms & Conditions
4. Click "Create Account"
5. You'll see a success message
6. You'll be redirected to the login page

### Step 2: Login
1. Go to `teacher-login.html`
2. Enter your **email** OR **employee ID**
3. Enter your **password**
4. Click "Login"
5. Success! (Teacher dashboard coming soon)

### Example:
```
SIGNUP:
- Name: Rajesh Verma
- Email: rajesh.verma@bfa.edu.in
- Employee ID: TCH001
- Subject: Mathematics
- Phone: 9876543210
- Password: teacher@123

LOGIN:
- Username: rajesh.verma@bfa.edu.in (or TCH001)
- Password: teacher@123
```

---

## 👨‍💼 For Admins

### Default Admin Account
**Email:** `admin@brightfutureacademy.edu.in`  
**Password:** `admin123`

### Login:
1. Go to `admin-login.html`
2. Enter admin email
3. Enter password
4. Click "Login"

*Note: Admin signup is restricted. Contact system administrator for new admin accounts.*

---

## 🗂️ File Structure

```
New Files Added:
├── student-signup.html        # Student registration page
├── teacher-signup.html        # Teacher registration page
├── js/
│   └── auth.js               # Authentication logic (signup/login)

Updated Files:
├── student-login.html        # Now uses auth.js, has signup link
├── teacher-login.html        # Now uses auth.js, has signup link
├── admin-login.html          # Now uses auth.js
├── student-dashboard.html    # Protected, requires login
```

---

## 💾 Data Storage

### LocalStorage Keys:
- `bfa_students` - Array of all registered students
- `bfa_teachers` - Array of all registered teachers
- `bfa_admins` - Array of admin accounts

### SessionStorage Keys (during login):
- `loggedIn` - true/false
- `userType` - student/teacher/admin
- `userId` - Unique user ID
- `userName` - Full name
- `userEmail` - Email address
- Plus role-specific data (class, roll number, subject, etc.)

### View Stored Data:
Open browser console (F12) and type:
```javascript
viewAllUsers()  // See all registered users
```

### Clear All Data:
```javascript
clearAllData()  // Delete all registrations (use carefully!)
```

---

## 🔒 Security Features

✅ **Password Validation** - Minimum 6 characters  
✅ **Duplicate Check** - Prevents duplicate emails/roll numbers  
✅ **Session Management** - Auto-logout on browser close  
✅ **Protected Routes** - Dashboard requires login  
✅ **Form Validation** - Client-side validation  

⚠️ **Important for Production:**
- Current system stores passwords in plain text (localStorage)
- For production, implement:
  - Backend server (PHP/Node.js)
  - Database (MySQL/MongoDB)
  - Password hashing (bcrypt)
  - HTTPS encryption
  - JWT tokens
  - Rate limiting
  - Email verification

---

## 📝 Testing the System

### Test Student Signup:
1. Open `student-signup.html`
2. Fill form with test data
3. Click "Create Account"
4. Verify success message
5. Go to `student-login.html`
6. Login with your email and password
7. Access `student-dashboard.html`

### Test Teacher Signup:
1. Open `teacher-signup.html`
2. Fill form with test data
3. Click "Create Account"
4. Verify success message
5. Go to `teacher-login.html`
6. Login with your email and password

### Test Admin Login:
1. Open `admin-login.html`
2. Use default credentials:
   - Email: `admin@brightfutureacademy.edu.in`
   - Password: `admin123`
3. Click "Login"

---

## ❌ Common Errors & Solutions

### "This email is already registered"
**Solution:** Use a different email or login instead of signing up

### "Passwords do not match"
**Solution:** Make sure password and confirm password are exactly the same

### "Please login first"
**Solution:** You tried to access dashboard without logging in. Go to login page first

### "No account found"
**Solution:** You haven't signed up yet. Click "Signup here" link

### "Incorrect password"
**Solution:** Check your password. It's case-sensitive

---

## 🔧 Customization

### Change Password Requirements:
In `auth.js`, modify:
```javascript
if (password.length < 6) {
    // Change 6 to your desired minimum length
}
```

### Add Email Verification:
1. Integrate EmailJS or similar service
2. Send verification code on signup
3. Verify before allowing login

### Add Forgot Password:
1. Create password reset page
2. Send reset link via email
3. Update password in localStorage

---

## 🚀 Next Steps for Production

1. **Backend Development:**
   - Create REST API (Node.js/PHP/Python)
   - Set up database (MySQL/PostgreSQL/MongoDB)
   - Implement password hashing

2. **Security Enhancements:**
   - Add HTTPS
   - Implement JWT tokens
   - Add 2FA (Two-Factor Authentication)
   - Rate limiting for login attempts
   - CAPTCHA for signup

3. **Email Integration:**
   - Email verification on signup
   - Password reset via email
   - Welcome emails
   - Notification emails

4. **Advanced Features:**
   - Remember me option
   - Social login (Google, Facebook)
   - Profile picture upload
   - Account settings page
   - Activity logs

---

## 📞 Support

### For Issues:
1. Check browser console (F12) for errors
2. Clear browser data and try again
3. Make sure JavaScript is enabled
4. Use modern browser (Chrome, Firefox, Edge)

### Debug Commands:
```javascript
// In browser console
viewAllUsers()      // See all registered users
clearAllData()      // Reset everything
localStorage.clear() // Clear all localStorage
sessionStorage.clear() // Clear session
```

---

## ✅ Quick Start Checklist

- [ ] Open website in browser
- [ ] Go to student-signup.html
- [ ] Fill registration form
- [ ] Create account successfully
- [ ] Go to student-login.html
- [ ] Login with your credentials
- [ ] Access student dashboard
- [ ] Test logout functionality
- [ ] Repeat for teacher signup/login

---

**🎓 Happy Learning with Bright Future Academy!**
