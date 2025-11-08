# Crensa Creator Beta Program Landing Page

A modern, responsive landing page for the Crensa Creator Beta Program with form submission and database integration.

## 🌐 Live Site
**URL:** https://crensa-3545a.web.app

## 📁 Project Structure
```
Crensa/
├── public/
│   └── index.html          # Main landing page
├── .firebase/              # Firebase cache (auto-generated)
├── firebase.json           # Firebase hosting configuration
├── .firebaserc            # Firebase project settings
├── .gitignore             # Git ignore rules
└── README.md              # This file
```

## 🚀 Features
- ✅ Responsive design (mobile & desktop)
- ✅ Interactive swipe cards for mobile
- ✅ Testimonial slideshow
- ✅ Supabase database integration
- ✅ Form with scroll effects
- ✅ Email confirmation ready (EmailJS)
- ✅ Professional animations

## 🔧 Technologies Used
- **Frontend:** HTML5, Tailwind CSS, JavaScript
- **Hosting:** Firebase Hosting
- **Database:** Supabase
- **Email:** EmailJS (optional)

## 📝 Form Fields
- Full Name
- Email Address
- Mobile Number
- Creator URL/Portfolio Link
- Example Video Link (optional)
- Story Idea (optional)

## 🛠️ Deployment

### Deploy to Firebase
```bash
firebase deploy
```

### Local Development
Simply open `public/index.html` in a browser or use a local server:
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve public
```

## 🔐 Configuration

### Supabase Setup
Update the credentials in `public/index.html`:
```javascript
const SUPABASE_URL = 'your-supabase-url';
const SUPABASE_ANON_KEY = 'your-anon-key';
```

### EmailJS Setup (Optional)
Update the credentials in `public/index.html`:
```javascript
const EMAILJS_PUBLIC_KEY = 'your-public-key';
const EMAILJS_SERVICE_ID = 'your-service-id';
const EMAILJS_TEMPLATE_ID = 'your-template-id';
```

## 📊 Database Schema
```sql
CREATE TABLE creator_applications (
  id BIGSERIAL PRIMARY KEY,
  full_name TEXT NOT NULL,
  email TEXT NOT NULL UNIQUE,
  mobile_number TEXT NOT NULL,
  portfolio_url TEXT NOT NULL,
  example_video_url TEXT,
  story_idea TEXT,
  application_status TEXT DEFAULT 'pending',
  submitted_at TIMESTAMPTZ DEFAULT NOW(),
  user_agent TEXT,
  referrer TEXT,
  created_at TIMESTAMPTZ DEFAULT NOW(),
  updated_at TIMESTAMPTZ DEFAULT NOW()
);
```

## 🎨 Color Palette
- Navy: `#01164D`
- Green: `#62CF6F`
- Teal: `#00BA9C`
- Lime: `#D5E73C`
- Yellow: `#CCE53F`
- Magenta: `#85125E`
- Pink: `#C81D84`
- Rose: `#D9208F`

## 📱 Browser Support
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## 📄 License
All rights reserved - Crensa

## 👥 Contact
For support or inquiries, contact the Crensa team.
