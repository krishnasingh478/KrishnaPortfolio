# Krishna Singh — Premium Full-Stack Developer Portfolio

> **BCA Second-Year Student • IEEE Member • Aspiring Full-Stack Web Developer**

A custom-built, responsive, full-stack personal portfolio and administrative management system engineered specifically for **Krishna Singh**. Crafted without heavy frontend frameworks to showcase mastery of core **HTML5, CSS3, Vanilla JavaScript (ES6+), Node.js, Express.js, and MongoDB**.

---

## ⚡ Design Vision: Futuristic Neon Red × Neon Blue

The portfolio incorporates a developer-centric aesthetic featuring controlled neon lighting and ambient depth:
- **Neon Red (`#FF1744`)**: Accents critical actions, featured project badges, alert states, and subtle glowing highlights.
- **Neon Blue (`#00B8FF`)**: Anchors primary navigation, links, telemetry borders, and futuristic lighting.
- **Dark Theme (Default)**: Deep obsidian canvas (`#080A10`), graphite surfaces (`#11141D`), and high-contrast typography (`#F5F7FF`).
- **Light Theme**: Clean off-white background (`#F5F7FB`), crisp white card elevations (`#FFFFFF`), and charcoal typography (`#171923`).
- **Zero-Flash Persistence**: Persists user choice in `localStorage` and gracefully honors the visitor's OS `prefers-color-scheme`.

---

## 🛠️ Technology Stack

| Layer | Technologies & Tools |
| :--- | :--- |
| **Frontend** | Pure HTML5, Semantic CSS3 (CSS Variables, Grid, Flexbox), Vanilla JavaScript (ES6+), Fetch API, IntersectionObserver |
| **Backend** | Node.js, Express.js, REST API Architecture |
| **Database** | MongoDB, Mongoose ODM (with automatic in-memory fallback for zero-dependency local testing) |
| **Security** | Helmet HTTP headers, Rate Limiting (express-rate-limit), Bcrypt password hashing, Secure HTTP-only Sessions, Server-side sanitization |
| **Tooling** | npm, Git, GitHub |

*Strict rule adherence: No React, Vue, Angular, TypeScript, Tailwind, Bootstrap, or jQuery were used.*

---

## 📂 Project Structure

```
Krishna Singh Portfolio/
├── client/                      # Pure Vanilla JS Frontend
│   ├── index.html               # Main public portfolio page
│   ├── admin.html               # Administrative console portal
│   ├── css/
│   │   ├── style.css            # Base layouts, components, typography
│   │   ├── themes.css           # Neon design tokens & light/dark variables
│   │   └── responsive.css       # Mobile (320px, 375px, 430px) & desktop breakpoints
│   ├── js/
│   │   ├── main.js              # Navbar scroll, mobile drawer, active section highlighting
│   │   ├── theme.js             # Theme switcher and persistence engine
│   │   ├── projects.js          # Project grid fetcher, filters, and modal dialog
│   │   ├── contact.js           # Contact form validation and async submission
│   │   └── admin.js             # Admin dashboard controller (auth, CRUD, messages)
│   └── assets/
│       ├── images/              # Custom SVG vectors & project concept illustrations
│       └── icons/               # KS monogram favicon and SVG glyphs
├── server/                      # Node.js & Express REST Backend
│   ├── server.js                # Express app entry point & static server
│   └── src/
│       ├── config/
│       │   ├── db.js            # Mongoose connection with resilient fallback
│       │   └── memoryStore.js   # In-memory store for instant zero-setup local dev
│       ├── models/
│       │   ├── Project.js       # Mongoose project schema
│       │   ├── Contact.js       # Mongoose contact submissions schema
│       │   └── Admin.js         # Mongoose admin authentication schema
│       ├── routes/
│       │   ├── projectRoutes.js # GET /api/projects, GET /api/projects/:slug
│       │   ├── contactRoutes.js # POST /api/contact
│       │   ├── authRoutes.js    # POST /api/auth/login, logout, me
│       │   └── adminRoutes.js   # Protected project CRUD & message moderation
│       ├── controllers/         # Request handling logic
│       ├── middleware/          # Auth guards, rate limiters, error handling
│       ├── validators/          # Input sanitization and slugification
│       └── scripts/
│           └── seed.js          # Database initial seeder script
├── docs/
│   └── API.md                   # Comprehensive REST API documentation
├── .env.example                 # Template for environment variables
├── .env                         # Local runtime environment configuration
├── .gitignore                   # Ignored files (node_modules, credentials)
├── package.json                 # Project dependencies and npm scripts
└── README.md                    # Project documentation
```

---

## 🚀 Getting Started

### 1. Prerequisites
- **Node.js** (v18.0.0 or higher recommended)
- **npm** (v9.0.0 or higher)
- **MongoDB** (Optional for local testing; local instance or MongoDB Atlas URI)

### 2. Installation
Clone or navigate to the repository directory and install dependencies:
```bash
cd "Krishna Singh Portfolio"
npm install
```

### 3. Environment Configuration
The application comes pre-configured with a default `.env` file. To customize, adjust the variables:
```env
PORT=5000
NODE_ENV=development
MONGODB_URI=mongodb://127.0.0.1:27017/krishna_portfolio
SESSION_SECRET=dev-secret-krishna-singh-portfolio-2026
ADMIN_USERNAME=admin
ADMIN_EMAIL=admin@krishnasingh.dev
ADMIN_PASSWORD=AdminSecurePassword123!
```

### 4. Database Seeding (Optional)
If running a local MongoDB server or Atlas cluster, populate it with initial sample projects and the admin account:
```bash
npm run seed
```
*(Note: If MongoDB is offline, the backend automatically utilizes the built-in resilient in-memory store so you can still view, test, and filter projects immediately without errors).*

### 5. Running the Application
Start the server:
```bash
npm start
```
Or run with automatic file watching in development:
```bash
npm run dev
```

Visit the application in your browser:
- 🌐 **Public Portfolio**: [http://localhost:5000](http://localhost:5000)
- 🔒 **Admin Portal**: [http://localhost:5000/admin](http://localhost:5000/admin)
- 🩺 **API Health Check**: [http://localhost:5000/api/health](http://localhost:5000/api/health)

---

## 🔑 Administrator Portal (`/admin`)

The portfolio includes a password-protected administrative interface:
- **Default Username**: `admin`
- **Default Password**: `AdminSecurePassword123!`
- **Dashboard Features**:
  - Live statistics: Total projects, Featured project count, Total inquiries, Unread inquiries.
  - Project Management: Add new projects, edit descriptions/technologies, toggle featured status, and delete entries.
  - Contact Inquiries: View submitted messages, mark as read/unread, and delete old messages.
  - Rate limiting & brute-force protection enabled.

---

## ✏️ Personalization Checklist for Krishna Singh

Update the following editable placeholders in `client/index.html` to reflect your exact details:
1. **College Name**: Search for `[ADD COLLEGE / UNIVERSITY NAME]` in `client/index.html` and insert your actual college.
2. **Contact Email**: Update `[YOUR-EMAIL-ADDRESS]` in `client/index.html` with your professional inbox.
3. **GitHub Profile**: Replace `[YOUR-GITHUB-USERNAME]` with your GitHub handle.
4. **LinkedIn Profile**: Replace `[YOUR-LINKEDIN-USERNAME]` with your LinkedIn vanity URL.
5. **Resume**: Replace the anchor link or drop your resume PDF file into `client/assets/resume.pdf`.
6. **Coursework**: Customize the course tags in the Education section.

---

## 🔒 Security Best Practices Implemented

- **Helmet**: Secures HTTP response headers and configures strict Content Security Policy (CSP).
- **Rate Limiting**: Protects against spam submissions (`5 requests / 15 min`) and brute-force logins (`10 attempts / 15 min`).
- **Bcrypt Hashing**: Secure password hashing with salt rounds.
- **Session Protection**: HTTP-only, SameSite lax session cookies with regeneration on login.
- **XSS Prevention**: Safe DOM rendering and server-side tag sanitization.
- **Environment Isolation**: No credentials or secrets exposed to client-side scripts.

---

## 🚢 Deployment Guide

### Deploying to Render / Railway / DigitalOcean
1. Push your repository to GitHub.
2. Create a new **Web Service** pointing to your repository.
3. Configure the build and start commands:
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`
4. Set the Environment Variables in the hosting dashboard:
   - `NODE_ENV=production`
   - `MONGODB_URI=<your-mongodb-atlas-connection-string>`
   - `SESSION_SECRET=<a-long-random-string>`
   - `ADMIN_USERNAME=<your-chosen-admin-username>`
   - `ADMIN_PASSWORD=<your-strong-password>`
5. Your portfolio and admin dashboard will be live on your custom domain or sub-domain with HTTPS enabled.

---

## 📄 License
This project is open-source and available under the **MIT License**.

