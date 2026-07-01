# Setup & Configuration Guide

## 🚀 Quick Start

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Text editor (VS Code recommended)
- Git (for version control)

### Installation Steps

1. **Clone Repository**
```bash
git clone https://github.com/pranusignup-ctrl/medical-website.git
cd medical-website
```

2. **Open in Browser**
```bash
# Option 1: Direct
open index.html

# Option 2: Using Python
python -m http.server 8000
# Visit: http://localhost:8000

# Option 3: Using Node.js
npx http-server
```

3. **Verify Installation**
- Check all navigation links work
- Test appointment booking form
- Toggle dark mode
- Test mobile responsiveness

## ⚙️ Configuration

### Doctor Information

Edit these in `index.html`:

```html
<!-- Update Doctor Name -->
<h2>Dr. [Your Name]</h2>

<!-- Update Qualification -->
<p class="qualification">Your Qualification</p>

<!-- Update Hero Subtitle -->
<p class="hero-subtitle">Your professional statement</p>

<!-- Update Statistics -->
<div class="stat-card">
    <h3 class="stat-number" data-target="YOUR_NUMBER">0</h3>
    <p class="stat-label">Your Stat</p>
</div>
```

### Contact Information

Update in `index.html`:

```html
<!-- Phone Number -->
<a href="tel:+919876543210">+91 YOUR PHONE</a>

<!-- Email -->
<a href="mailto:hello@drpranay.com">YOUR EMAIL</a>

<!-- WhatsApp -->
<a href="https://wa.me/919876543210">YOUR WHATSAPP NUMBER</a>

<!-- Clinic Address -->
<p>YOUR CLINIC ADDRESS</p>

<!-- Clinic Timings -->
<p>YOUR CLINIC HOURS</p>
```

### Color Customization

Edit CSS variables in `styles.css`:

```css
:root {
    --primary-blue: #0066cc;      /* Main brand color */
    --dark-blue: #004499;         /* Hover/active states */
    --gold: #d4af37;              /* Accent color */
    --white: #ffffff;             /* Background */
    --text-color: #2c3e50;        /* Text color */
}
```

### Service Customization

Update services in `index.html`:

```html
<div class="service-card glass-effect">
    <div class="service-icon">
        <i class="fas fa-your-icon"></i>
    </div>
    <h3>Your Service Name</h3>
    <p>Your service description</p>
</div>
```

Browse icons at: [Font Awesome Icons](https://fontawesome.com/icons)

## 🔧 Advanced Configuration

### Environment Variables

Create `.env` file for production:

```bash
# API Configuration
VITE_API_URL=https://api.yourdomain.com
VITE_API_KEY=your_api_key

# Email Configuration
VITE_EMAIL_SERVICE=sendgrid
VITE_EMAIL_API_KEY=your_email_key

# SMS Configuration
VITE_SMS_SERVICE=twilio
VITE_SMS_ACCOUNT_SID=your_account_sid
VITE_SMS_AUTH_TOKEN=your_auth_token

# Google Maps
VITE_GOOGLE_MAPS_KEY=your_maps_key
```

### Form Customization

Modify appointment types in `script.js`:

```javascript
const appointmentTypes = {
    'general': 'General Consultation',
    'assessment': 'Cardiovascular Assessment',
    'followup': 'Follow-up Visit',
    // Add your custom types
    'custom': 'Your Custom Type'
};
```

### Time Slots Configuration

Edit available time slots in `index.html`:

```html
<select name="timeSlot" required>
    <option value="">Select Time Slot</option>
    <option value="10:00 AM">10:00 AM</option>
    <option value="10:30 AM">10:30 AM</option>
    <!-- Add or remove as needed -->
</select>
```

### Analytics Integration

Add Google Analytics to `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'GA_ID');
</script>
```

## 🎨 Customization Options

### Header Logo

Replace heartbeat icon in `index.html`:

```html
<div class="nav-logo">
    <i class="fas fa-hospital"></i> <!-- Change icon -->
    <span>Your Clinic Name</span>
</div>
```

### Hero Image Placeholder

Customize in `styles.css`:

```css
.doctor-image-placeholder {
    background: linear-gradient(135deg, #e6f2ff, #f0e6d2);
    /* Change gradient colors */
    font-size: 120px;
    color: #0066cc;
    /* Change icon color */
}
```

### Font Customization

Add custom fonts in `styles.css`:

```css
@import url('https://fonts.googleapis.com/css2?family=Your+Font:wght@400;600;700&display=swap');

body {
    font-family: 'Your Font', 'Segoe UI', sans-serif;
}
```

## 📱 Mobile Optimization

### Responsive Testing

Test at these breakpoints:
- Desktop: 1200px+
- Tablet: 768px - 1199px
- Mobile: 480px - 767px
- Small Mobile: < 480px

### Mobile Menu

Hamburger menu auto-activates below 768px. Adjust in `styles.css`:

```css
@media (max-width: 768px) {
    .hamburger {
        display: flex; /* Shows hamburger */
    }
    
    .nav-menu {
        display: none; /* Hides desktop menu */
    }
}
```

## 🔐 Security Setup

### HTTPS Configuration

```bash
# Generate SSL certificate
openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
    -keyout server.key -out server.crt
```

### Security Headers

Add to your server configuration:

```
Strict-Transport-Security: max-age=31536000; includeSubDomains
X-Content-Type-Options: nosniff
X-Frame-Options: DENY
X-XSS-Protection: 1; mode=block
Content-Security-Policy: default-src 'self'
```

## 🚀 Deployment

### GitHub Pages

1. Push to GitHub
2. Go to Settings → Pages
3. Select `main` branch
4. Site will be live at: `https://yourusername.github.io/medical-website`

### Netlify

1. Connect GitHub repo
2. Set build settings:
   - Build command: (leave blank)
   - Publish directory: `.`
3. Deploy

### Server Deployment

```bash
# SSH to server
ssh user@yourserver.com

# Clone repository
git clone https://github.com/pranusignup-ctrl/medical-website.git
cd medical-website

# Install dependencies (if needed)
npm install

# Start local server
python -m http.server 8000
```

## 📊 Data Management

### Exporting Appointments

```javascript
// Call this function to export appointments
exportAppointments();
```

Appointments are saved in localStorage as JSON.

### Backup Data

```javascript
// Backup appointments
const appointments = localStorage.getItem('appointments');
const blob = new Blob([appointments], {type: 'application/json'});
const url = URL.createObjectURL(blob);
const a = document.createElement('a');
a.href = url;
a.download = 'backup.json';
a.click();
```

## 🔄 Integration Examples

### Email Integration (Nodemailer)

```javascript
// Backend: server.js
const nodemailer = require('nodemailer');

const transporter = nodemailer.createTransport({
    service: 'gmail',
    auth: {
        user: process.env.EMAIL,
        pass: process.env.PASSWORD
    }
});

app.post('/api/appointments', (req, res) => {
    const mailOptions = {
        from: process.env.EMAIL,
        to: req.body.email,
        subject: 'Appointment Confirmation',
        html: `<h1>Appointment Confirmed</h1><p>Your appointment is on ${req.body.date}</p>`
    };
    
    transporter.sendMail(mailOptions, (err, info) => {
        if (err) {
            res.status(500).send('Error');
        } else {
            res.status(200).send('Email sent');
        }
    });
});
```

### SMS Integration (Twilio)

```javascript
// Backend: server.js
const twilio = require('twilio');

const client = twilio(
    process.env.TWILIO_ACCOUNT_SID,
    process.env.TWILIO_AUTH_TOKEN
);

app.post('/api/send-sms', (req, res) => {
    client.messages.create({
        body: `Appointment confirmed for ${req.body.date}`,
        from: process.env.TWILIO_PHONE,
        to: req.body.phone
    })
    .then(() => res.status(200).send('SMS sent'))
    .catch(err => res.status(500).send('Error'));
});
```

### Payment Integration (Razorpay)

```javascript
// Frontend: Add to script.js
const handlePayment = async (appointmentData) => {
    const response = await fetch('/api/create-order', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(appointmentData)
    });
    
    const order = await response.json();
    
    const options = {
        key: process.env.VITE_RAZORPAY_KEY,
        amount: order.amount,
        currency: "INR",
        order_id: order.id,
        handler: function (response) {
            // Handle payment success
        }
    };
    
    const rzp = new Razorpay(options);
    rzp.open();
};
```

## 🧪 Testing

### Manual Testing Checklist

- [ ] Form validation works
- [ ] Email format validation
- [ ] Phone number validation
- [ ] Date picker works
- [ ] Time slots display correctly
- [ ] Dark mode toggles
- [ ] Mobile menu opens/closes
- [ ] Animations are smooth
- [ ] Modal dialogs open/close
- [ ] Emergency button works
- [ ] WhatsApp button opens
- [ ] Email link works
- [ ] Phone link works
- [ ] Responsive at all breakpoints

### Automated Testing

```bash
# Install testing tools
npm install --save-dev jest @testing-library/jest-dom

# Run tests
npm test
```

## 📝 Documentation

### Updating Documentation

- Keep README.md current
- Document API endpoints
- Update configuration options
- Add troubleshooting guide
- Maintain changelog

### Code Comments

```javascript
// Good: Clear and purposeful
function validatePhoneNumber(phone) {
    // Indian phone numbers are 10 digits
    const regex = /^[0-9]{10}$/;
    return regex.test(phone);
}

// Bad: Obvious or unclear
function validate(p) {
    // Check phone
    const r = /^[0-9]{10}$/;
    return r.test(p);
}
```

## 🐛 Troubleshooting

### Common Issues

**Issue: Styles not loading**
- Clear browser cache (Ctrl+Shift+Del)
- Hard refresh (Ctrl+Shift+R)
- Check file paths

**Issue: Form not submitting**
- Check console for errors (F12)
- Verify all required fields filled
- Check localStorage permissions

**Issue: Dark mode not working**
- Check browser localStorage enabled
- Verify theme toggle element exists
- Clear localStorage and refresh

**Issue: Mobile menu not appearing**
- Check viewport meta tag
- Verify CSS media queries
- Test on actual mobile device

## 📞 Support

For configuration help:
- Email: hello@drpranay.com
- Phone: +91 98765 43210
- Create GitHub issue with details

## ✅ Deployment Checklist

- [ ] All contact info updated
- [ ] Doctor information verified
- [ ] Images optimized
- [ ] SEO meta tags set
- [ ] Analytics configured
- [ ] Security headers set
- [ ] HTTPS enabled
- [ ] Mobile responsive tested
- [ ] All forms tested
- [ ] Dark mode tested
- [ ] Performance optimized
- [ ] Accessibility verified
- [ ] Backup created

---

**Last Updated:** July 2024
**Version:** 1.0.0

For updates and new versions, visit the GitHub repository.
