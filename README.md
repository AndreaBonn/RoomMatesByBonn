# 🏠 RoomMate App

> **[🇮🇹 Leggi in Italiano](./README_IT.md)** | **🇬🇧 English**

[![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=flat&logo=firebase&logoColor=black)](https://firebase.google.com/)
[![React](https://img.shields.io/badge/React-18.2-61DAFB?style=flat&logo=react&logoColor=black)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.3-3178C6?style=flat&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.3-38B2AC?style=flat&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![PWA](https://img.shields.io/badge/PWA-Enabled-5A0FC8?style=flat&logo=pwa&logoColor=white)](https://web.dev/progressive-web-apps/)

**A comprehensive web application for seamless roommate living management**

---

## 📖 Table of Contents

- [What is RoomMate App?](#-what-is-roommate-app)
- [Key Features](#-key-features)
- [How to Use](#-how-to-use)
- [Technology Stack](#-technology-stack)
- [Installation & Setup](#-installation--setup)
- [Project Structure](#-project-structure)
- [Feedback & Support](#-feedback--support)
- [Security](#-security)
- [License](#-license)
- [Author](#-author)

---

## 🎯 What is RoomMate App?

**RoomMate App** is a modern, full-featured Progressive Web Application designed to simplify shared living. Whether you're a university student, young professional, or anyone sharing a home, this app provides all the tools you need to manage your household efficiently and harmoniously.

### Why RoomMate App?

Living with roommates can be challenging. From splitting bills fairly to coordinating cleaning schedules, managing a shared household requires organization and clear communication. RoomMate App solves these challenges by providing:

- **Financial Transparency**: Track shared expenses with automatic balance calculations and smart transaction minimization
- **Organized Cleaning**: AI-powered cleaning schedules with automatic rotation and reminders
- **Seamless Communication**: Announcements, polls, and house rules all in one place
- **Smart Coordination**: Shared shopping lists, maintenance tracking, and waste collection reminders
- **Offline Support**: Full PWA capabilities with offline functionality and automatic sync

### Who is it for?

- 🎓 University students in shared apartments
- 💼 Young professionals in co-living spaces
- 👥 Groups of friends sharing a home
- 🏘️ Anyone managing a shared household

---

## ✨ Key Features

### 💰 Advanced Expense Management

- **Smart Expense Splitting**: Divide expenses equally, by custom amounts, or by percentage
- **Automatic Balance Calculation**: Real-time balance tracking with transaction minimization algorithm
- **Recurring Expenses**: Set up automatic monthly bills (rent, utilities, subscriptions)
- **Expense Categories**: Organize by type (bills, groceries, rent, cleaning, maintenance)
- **Detailed Analytics**: Monthly charts, category breakdowns, and spending insights
- **Export Capabilities**: Generate PDF/CSV reports for any time period
- **Reimbursement Tracking**: Request and track money owed between roommates

### 🧹 Intelligent Cleaning Management

- **Multiple Scenarios**: Create different cleaning schedules (weekly, bi-weekly, monthly)
- **Flexible Rotation**: Automatic rotation among roommates with customizable patterns
- **Cleaning Types**: Kitchen, bathroom, general, trash, and more
- **AI Schedule Generation**: Let AI create optimized cleaning schedules based on preferences
- **Completion Tracking**: Checklist items with completion timestamps
- **Smart Reminders**: Automatic notifications for upcoming and overdue tasks
- **Special Shifts**: Add one-time or exceptional cleaning tasks

### 🛒 Real-Time Shopping List

- **Live Synchronization**: Instant updates across all devices
- **Smart Categories**: Automatic categorization (food, beverages, household, personal care)
- **Priority Levels**: Mark items as high, medium, or low priority
- **Purchase Tracking**: Track who bought what and when
- **Auto-Expense Creation**: Convert purchased items into shared expenses
- **Urgent Notifications**: Alerts for high-priority items

### 📅 Unified Calendar

- **All-in-One View**: See cleaning shifts, maintenance, waste collection, and events
- **Event Management**: Create and manage house events with descriptions
- **Smart Filtering**: Filter by event type for focused views
- **Color Coding**: Visual distinction between different event types
- **Export Options**: Generate PDF calendars for printing

### ♻️ Waste Collection Management

- **Collection Schedules**: Set up recurring waste collection days
- **Multiple Waste Types**: Organic, plastic, paper, glass, metal, hazardous, and more
- **Automatic Reminders**: Notifications the day before collection
- **Multiple Scenarios**: Different schedules for different seasons or locations

### 🔧 Maintenance Tracking

- **Task Management**: Create, assign, and track maintenance tasks
- **Priority Levels**: Organize by urgency (low, medium, high, urgent)
- **Status Tracking**: Monitor progress from reported to completed
- **Email Notifications**: Automatic reminders for pending maintenance
- **History Log**: Complete record of all maintenance activities

### 📢 Communication Tools

- **Announcement Board**: Post important messages with priority levels
- **Pin Important Posts**: Keep critical announcements at the top
- **Polls & Surveys**: Create polls with single or multiple choice options
- **Real-Time Results**: See voting results as they come in
- **Email Integration**: Send announcements and polls via email

### 📋 House Rules System

- **Democratic Proposals**: Any member can propose new rules
- **Voting System**: Approve or reject rule changes democratically
- **Rule Categories**: Organize by type (cleaning, expenses, guests, noise, etc.)
- **Rule History**: Track all changes and proposals
- **PDF Export**: Generate a complete house rulebook

### 📞 Shared Contacts

- **Contact Directory**: Store important contacts (landlord, plumber, electrician, etc.)
- **Categorization**: Organize by role and add custom tags
- **Favorites**: Quick access to frequently used contacts
- **Click-to-Call/Email**: Direct communication from the app
- **Export Options**: Generate PDF contact lists

### 🤖 AI Assistant Integration

- **Multi-Provider Support**: Works with OpenAI, Anthropic Claude, Google Gemini, and Groq
- **Flexible API Key Storage**: Choose between local (browser) or cloud (Firebase) storage
- **AI Chatbot**: Get help and suggestions (conversation interface)
- **Smart Schedule Generation**: AI creates optimized cleaning schedules based on preferences
- **Provider Preference**: Set your preferred AI provider with automatic fallback

### � Member Management

- **Real Members**: Full accounts with authentication
- **Virtual Members (NPCs)**: Add roommates without accounts for expense tracking
- **Role System**: Admin and member roles with different permissions
- **Member Merging**: Combine duplicate profiles when someone creates an account
- **Invite System**: Unique invite codes for joining houses

### 🌍 Multi-Language Support

- **English & Italian**: Full translations for all features
- **Instant Switching**: Change language from user profile
- **Localized Formatting**: Dates, times, and currencies adapted to locale

### 📱 Progressive Web App (PWA)

- **Installable**: Add to home screen on mobile and desktop
- **Offline Support**: Core features work without internet connection
- **Push Notifications**: Native notifications for important events
- **Auto-Sync**: Automatic synchronization when connection is restored
- **Fast Loading**: Optimized caching for instant access
- **Auto-Updates**: Seamless updates with user notification

### 🔒 Security & Privacy

- **Firebase Authentication**: Secure email/password authentication
- **Role-Based Access**: Granular permissions for admins and members
- **Firestore Security Rules**: Database-level security enforcement
- **HTTPS Encryption**: All communications encrypted
- **API Key Protection**: Encrypted storage options for AI provider keys
- **Data Privacy**: Your data belongs to you

---

## 🚀 How to Use

### Getting Started

1. **Access the App**
   - Visit the deployed application URL
   - Or install it as a PWA on your device

2. **Create an Account**
   - Click "Register" and provide your email, name, and password
   - Verify your email address

3. **Set Up Your House**
   - **Create a New House**: Enter house name, address, and details
   - **Join an Existing House**: Use the invite code provided by your roommate

4. **Invite Roommates**
   - Go to House Settings
   - Share the unique invite code with your roommates
   - They can join using the code after registering

### Managing Expenses

1. **Add an Expense**
   - Navigate to "Expenses" page
   - Click "Add Expense"
   - Enter title, amount, category, and date
   - Select which roommates are involved
   - Choose splitting method (equal, custom, or percentage)
   - Save the expense

2. **View Balances**
   - Check the "Balances" section to see who owes whom
   - The app automatically calculates the minimum number of transactions needed
   - Mark transactions as completed when paid

3. **Track Reimbursements**
   - Go to "Reimbursements" page
   - Create reimbursement requests for money owed
   - Track status (pending/completed)

4. **Analyze Spending**
   - View monthly expense charts
   - See category breakdowns
   - Export reports as PDF or CSV

### Organizing Cleaning

1. **Create a Cleaning Scenario**
   - Go to "Cleaning Shifts" page
   - Click "New Scenario"
   - Choose frequency (weekly, bi-weekly, monthly)
   - Assign cleaning tasks to specific days
   - Select which roommates participate
   - Activate the scenario

2. **Use AI to Generate Schedule**
   - Click "AI Schedule Generator"
   - Configure your API key (if not already set)
   - Specify preferences (rooms, frequency, participant preferences)
   - Let AI create an optimized schedule
   - Review and adjust as needed
   - Save the scenario

3. **Complete Shifts**
   - View your assigned shifts on the calendar
   - Check off tasks as you complete them
   - Mark the shift as complete
   - Receive automatic reminders for upcoming shifts

4. **Manage Exceptions**
   - Add special one-time cleaning tasks
   - Modify existing shifts if needed
   - Track completion history

### Using the Shopping List

1. **Add Items**
   - Navigate to "Shopping List"
   - Click "Add Item"
   - Enter product name, category, and priority
   - Save the item

2. **Shop Together**
   - All roommates see the same list in real-time
   - Check off items as you buy them
   - Add the actual cost if desired

3. **Create Expense from List**
   - After shopping, click "Create Expense from List"
   - The app automatically generates an expense with all purchased items
   - Adjust and save

### Managing Maintenance

1. **Report an Issue**
   - Go to "Maintenance" page
   - Click "New Task"
   - Describe the problem, set priority
   - Assign to a responsible person (optional)
   - Save the task

2. **Track Progress**
   - Update task status as work progresses
   - Add notes and updates
   - Mark as completed when done
   - Receive email reminders for pending tasks

### Setting Up Waste Collection

1. **Create Collection Schedule**
   - Navigate to "Waste Collection"
   - Click "New Scenario"
   - Select waste types (organic, plastic, paper, glass, etc.)
   - Assign collection days for each type
   - Choose frequency (weekly/bi-weekly)
   - Activate the scenario

2. **Receive Reminders**
   - Get automatic notifications the evening before collection day
   - View upcoming collections on the dashboard
   - Check the calendar for the full schedule

### Communication & Rules

1. **Post Announcements**
   - Go to House page
   - Click "New Announcement"
   - Write your message, set priority
   - Pin important announcements
   - Roommates receive notifications

2. **Create Polls**
   - Click "New Poll"
   - Enter question and options
   - Choose single or multiple choice
   - Set closing date
   - View results in real-time

3. **Propose House Rules**
   - Navigate to "House Rules"
   - Click "Propose Rule"
   - Enter rule title, description, and category
   - Submit for voting
   - Rules are approved by majority vote

### Using the Calendar

1. **View Events**
   - Go to "Calendar" page
   - See all events, shifts, maintenance, and collections
   - Filter by type for focused view
   - Click events for details

2. **Add Events**
   - Click "Add Event"
   - Enter title, description, date/time
   - Select event type
   - Choose participants
   - Save the event

3. **Export Calendar**
   - Click "Export" button
   - Choose PDF format
   - Download and print if needed

### Configuring AI Assistant

1. **Set Up API Keys**
   - Go to User Profile
   - Click "AI Settings"
   - Choose your preferred AI provider (OpenAI, Anthropic, Gemini, or Groq)
   - Enter your API key
   - Choose storage location (local browser or cloud)
   - Save settings

2. **Set Provider Preference**
   - Arrange providers in order of preference
   - The app will use the first available provider
   - Automatic fallback if primary provider fails

3. **Use AI Features**
   - AI Cleaning Schedule Generator
   - AI Chatbot for assistance (coming soon)

### Managing Your Profile

1. **Edit Profile**
   - Click on your name/avatar
   - Update name, nickname, phone
   - Upload profile picture
   - Change language preference
   - Save changes

2. **Notification Settings**
   - Enable/disable push notifications
   - Test notifications
   - Configure notification preferences

3. **Leave a House**
   - Go to House Settings
   - Click "Leave House"
   - Confirm your decision
   - Your data remains for historical purposes

### Offline Usage

1. **Install as PWA**
   - Click the install prompt when it appears
   - Or use browser menu: "Install App" / "Add to Home Screen"

2. **Work Offline**
   - Core features work without internet
   - Changes are queued automatically
   - Data syncs when connection is restored

3. **Check Sync Status**
   - Look for the online/offline indicator
   - View pending changes in settings

---

## 🛠 Technology Stack

### Frontend

- **React 18.2** - Modern UI framework with hooks
- **TypeScript 5.3** - Type-safe development
- **Vite 5.0** - Lightning-fast build tool
- **Tailwind CSS 3.3** - Utility-first CSS framework
- **React Router 6.20** - Client-side routing
- **Zustand 4.4** - Lightweight state management
- **React Query 5.14** - Data fetching and caching
- **React Hook Form 7.49** - Performant form management
- **Zod 3.22** - TypeScript-first schema validation
- **Lucide React 0.294** - Modern icon library
- **Recharts 3.5** - Composable charting library
- **date-fns 3.0** - Modern date utility library
- **jsPDF 3.0 + jsPDF-AutoTable 5.0** - Client-side PDF generation

### Backend & Infrastructure

- **Firebase Authentication** - User management and authentication
- **Cloud Firestore** - Real-time NoSQL database
- **Firebase Hosting** - Fast and secure static hosting
- **Node.js + Express** - Email microservice
- **Brevo (Sendinblue)** - Transactional email service

### AI Integration

- **OpenAI GPT** - Advanced language model
- **Anthropic Claude** - Conversational AI
- **Google Gemini** - Google's AI model
- **Groq** - Fast inference AI

### DevOps & Tools

- **Git** - Version control
- **npm** - Package management
- **Firebase CLI** - Deployment and management
- **ESLint** - Code linting
- **PostCSS** - CSS processing

---

## 📦 Installation & Setup

> **Note**: This repository provides documentation and usage instructions. The source code is private. For access inquiries, please contact the author.

### Prerequisites

- **Node.js** 18.0.0 or higher
- **npm** 9.0.0 or higher
- **Firebase Account** (free tier available)
- **Brevo Account** for email service (optional)
- **AI Provider API Key** (optional, for AI features)

### Firebase Setup

1. Create a new project on [Firebase Console](https://console.firebase.google.com/)
2. Enable **Authentication** with Email/Password provider
3. Create a **Cloud Firestore** database
4. Enable **Firebase Hosting**
5. Download configuration file

### Frontend Configuration

Create `frontend/.env`:

```env
VITE_FIREBASE_API_KEY=your_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id
VITE_EMAIL_SERVICE_URL=http://localhost:3001
```

### Email Service Configuration (Optional)

Create `email-service/.env`:

```env
PORT=3001
BREVO_API_KEY=your_brevo_api_key
SENDER_EMAIL=noreply@yourdomain.com
SENDER_NAME=RoomMate App
FIREBASE_PROJECT_ID=your_project_id
```

### Firestore Security Rules

Deploy security rules:

```bash
firebase deploy --only firestore:rules
```

### Firestore Indexes

Deploy database indexes:

```bash
firebase deploy --only firestore:indexes
```

### Local Development

```bash
# Install dependencies
npm install
cd frontend && npm install
cd ../email-service && npm install

# Start frontend (port 5173)
cd frontend
npm run dev

# Start email service (port 3001) - optional
cd email-service
npm start
```

Open browser at `http://localhost:5173`

### Production Build

```bash
# Build frontend
cd frontend
npm run build

# Preview build
npm run preview
```

### Deploy to Firebase

```bash
# Deploy everything
firebase deploy

# Deploy hosting only
firebase deploy --only hosting

# Deploy Firestore rules only
firebase deploy --only firestore:rules
```

---

## 📁 Project Structure

```
roommate-app/
├── frontend/                    # React application
│   ├── src/
│   │   ├── components/         # Reusable components
│   │   │   ├── sections/       # Page sections
│   │   │   ├── sondaggi/       # Poll/survey components
│   │   │   ├── collapsible/    # Collapsible UI
│   │   │   └── skeletons/      # Loading skeletons
│   │   ├── pages/              # Application pages
│   │   ├── services/           # Firebase & API services
│   │   ├── hooks/              # Custom React hooks
│   │   ├── i18n/               # Internationalization
│   │   ├── config/             # Configuration files
│   │   └── types/              # TypeScript types
│   ├── public/                 # Static assets & PWA
│   └── dist/                   # Production build
├── email-service/              # Node.js microservice
│   ├── server.js              # Express server
│   └── check-manutenzioni-status.js
├── documento_progetto/         # Technical documentation
├── firestore.rules            # Firestore security rules
├── firestore.indexes.json     # Firestore indexes
├── firebase.json              # Firebase configuration
├── README.md                  # This file (English)
├── README_IT.md               # Italian README
├── LICENSE.md                 # License information
├── SECURITY.md                # Security policy (English)
└── SECURITY_IT.md             # Security policy (Italian)
```

---

## 💬 Feedback & Support

Your feedback helps make RoomMate App better! We welcome:

- 🐛 **Bug Reports**: Found something not working? Let us know!
- ✨ **Feature Requests**: Have ideas for new functionality? Share them!
- 💡 **Suggestions**: Ways to improve existing features
- 🆘 **Support Questions**: Need help using the app?

### How to Provide Feedback

1. **GitHub Issues**: [Open an issue](https://github.com/AndreaBonn/RoomMatesByBonn/issues)
2. **Email**: andreabonacci95@protonmail.com

For detailed guidelines on reporting bugs, requesting features, and getting support, see our [Feedback Guide](./FEEDBACK.md).

---

## 🔒 Security

Security is a top priority. Please review our [Security Policy](./SECURITY.md) for:
- Supported versions
- Reporting vulnerabilities
- Security best practices
- Data protection measures

**[🇮🇹 Politica di Sicurezza in Italiano](./SECURITY_IT.md)**

---

## 📄 License

This project documentation is provided for informational purposes. The source code is private and proprietary.

**Personal Use**: You are free to use the deployed application for personal, non-commercial purposes.

**Source Code**: The source code is not publicly available. For licensing inquiries or access requests, please contact the author.

See [LICENSE.md](./LICENSE.md) for more details.

---

## 👨‍💻 Author

**Andrea Bonacci**

- GitHub: [@AndreaBonn](https://github.com/AndreaBonn)
- Email: andreabonacci95@protonmail.com

---

## 🙏 Acknowledgments

- **Firebase** for the robust backend infrastructure
- **React Team** for the excellent framework
- **Tailwind CSS** for the beautiful design system
- **Lucide** for the modern icon set
- **Recharts** for the charting library
- **All AI providers** for making intelligent features possible
- **Open source community** for the amazing tools and libraries

---

## 📊 Project Status

**Status**: ✅ Active Development

**Version**: 1.0.0

**Last Updated**: December 2024

---

## 🌟 Star History

If you find this project useful, please consider giving it a star! ⭐

---

**[🇮🇹 Torna alla versione Italiana](./README_IT.md)** | **[🔒 Security Policy](./SECURITY.md)** | **[💬 Feedback](./FEEDBACK.md)** | **[📄 License](./LICENSE.md)**
