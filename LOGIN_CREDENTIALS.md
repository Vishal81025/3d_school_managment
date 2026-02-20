# 🔐 Test Login Credentials

## Important Note
These are **TEST CREDENTIALS ONLY** for demonstration purposes. In production, implement proper authentication with secure password hashing.

---

## 👨‍🎓 Student Portal Login
**URL:** `student-login.html`

### Test Student Accounts:

**Student 1:**
- **Username:** `2024101` or `rahul.kumar`
- **Password:** `student123`
- **Details:** Rahul Kumar, Class 10-A, Roll No: 2024101

**Student 2:**
- **Username:** `2024202` or `priya.sharma`
- **Password:** `student123`
- **Details:** Priya Sharma, Class 12-B, Roll No: 2024202

**Student 3:**
- **Username:** `2024303` or `amit.singh`
- **Password:** `student123`
- **Details:** Amit Singh, Class 9-C, Roll No: 2024303

---

## 👨‍🏫 Teacher Portal Login
**URL:** `teacher-login.html`

### Test Teacher Accounts:

**Teacher 1:**
- **Username:** `TCH001` or `rajesh.verma@bfa.edu.in`
- **Password:** `teacher123`
- **Details:** Mr. Rajesh Verma, Mathematics Teacher

**Teacher 2:**
- **Username:** `TCH002` or `meena.gupta@bfa.edu.in`
- **Password:** `teacher123`
- **Details:** Mrs. Meena Gupta, English Teacher

**Teacher 3:**
- **Username:** `TCH003` or `suresh.kumar@bfa.edu.in`
- **Password:** `teacher123`
- **Details:** Mr. Suresh Kumar, Science Teacher

---

## 👨‍💼 Admin Portal Login
**URL:** `admin-login.html`

### Test Admin Accounts:

**Super Admin:**
- **Username:** `admin` or `superadmin`
- **Password:** `admin123`
- **Details:** System Administrator, Full Access

**Principal:**
- **Username:** `principal` or `dr.rajesh.kumar`
- **Password:** `principal123`
- **Details:** Dr. Rajesh Kumar, School Principal

**Admission Officer:**
- **Username:** `admission` or `admission.officer`
- **Password:** `admission123`
- **Details:** Admission Department Access

---

## 🔑 Quick Reference Table

| Portal | Username | Password | Access Level |
|--------|----------|----------|--------------|
| **STUDENT** |
| Student 1 | `2024101` or `rahul.kumar` | `student123` | Class 10-A |
| Student 2 | `2024202` or `priya.sharma` | `student123` | Class 12-B |
| Student 3 | `2024303` or `amit.singh` | `student123` | Class 9-C |
| **TEACHER** |
| Teacher 1 | `TCH001` or `rajesh.verma@bfa.edu.in` | `teacher123` | Mathematics |
| Teacher 2 | `TCH002` or `meena.gupta@bfa.edu.in` | `teacher123` | English |
| Teacher 3 | `TCH003` or `suresh.kumar@bfa.edu.in` | `teacher123` | Science |
| **ADMIN** |
| Super Admin | `admin` or `superadmin` | `admin123` | Full Access |
| Principal | `principal` or `dr.rajesh.kumar` | `principal123` | Principal |
| Admission | `admission` or `admission.officer` | `admission123` | Admissions |

---

## 🎯 Testing Instructions

### For Students:
1. Go to `student-login.html`
2. Enter any student username (e.g., `2024101`)
3. Enter password: `student123`
4. Click Login
5. You'll be redirected to `student-dashboard.html`

### For Teachers:
1. Go to `teacher-login.html`
2. Enter any teacher username (e.g., `TCH001`)
3. Enter password: `teacher123`
4. Click Login
5. Alert will confirm successful login

### For Admins:
1. Go to `admin-login.html`
2. Enter admin username (e.g., `admin`)
3. Enter password: `admin123`
4. Click Login
5. Alert will confirm successful login

---

## ⚠️ Security Warnings

### FOR PRODUCTION USE:
1. **NEVER use these credentials in production**
2. **Implement proper authentication:**
   - Use secure password hashing (bcrypt, Argon2)
   - Implement session management
   - Add CSRF protection
   - Use HTTPS only
   - Add rate limiting
   - Implement 2FA for admin accounts

3. **Database Integration Required:**
   - Store credentials in secure database
   - Hash all passwords
   - Implement password reset functionality
   - Add account lockout after failed attempts

4. **Additional Security Measures:**
   - Implement JWT tokens
   - Add OAuth/SSO options
   - Enable audit logging
   - Regular security audits
   - Input validation and sanitization

---

## 🔧 How to Change Credentials

### In JavaScript (script.js):
Look for the `testCredentials` object and modify:

```javascript
const testCredentials = {
    student: [
        { username: 'YOUR_USERNAME', password: 'YOUR_PASSWORD', name: 'Student Name' }
    ],
    teacher: [
        { username: 'YOUR_USERNAME', password: 'YOUR_PASSWORD', name: 'Teacher Name' }
    ],
    admin: [
        { username: 'YOUR_USERNAME', password: 'YOUR_PASSWORD', name: 'Admin Name' }
    ]
};
```

---

## 📝 Notes

- All passwords are intentionally simple for testing
- The system will accept both username formats (ID or email)
- Case-sensitive login
- No account lockout in test mode
- Session management is simulated (not secure)

---

## 🚀 Next Steps for Production

1. Set up MySQL/PostgreSQL database
2. Create users table with hashed passwords
3. Implement PHP/Node.js backend authentication
4. Add session management
5. Implement forgot password functionality
6. Add email verification
7. Set up role-based access control (RBAC)
8. Enable audit logging
9. Add password strength requirements
10. Implement 2FA for sensitive accounts

---

**Remember: These are DEMO credentials only. Always implement proper security measures for production use!**
