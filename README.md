# The Wild Oasis - Cabin Booking Application

A full-stack cabin booking system built with Next.js, React, and Supabase. This project was developed as part of a comprehensive Next.js course to learn modern web development patterns and full-stack application architecture.

## Project Overview

The Wild Oasis is a luxury cabin booking platform that allows users to:

- Browse available cabins with filtering options
- View detailed cabin information and amenities
- Select dates with real-time availability checking
- Make authenticated reservations through Google OAuth
- Manage bookings and user profiles
- Handle booking modifications and cancellations

## Technology Stack

- **Frontend:** Next.js 14 (App Router), React 18, JavaScript
- **Styling:** Tailwind CSS
- **Backend:** Next.js Server Actions, Supabase
- **Authentication:** NextAuth.js with Google OAuth
- **Database:** Supabase (PostgreSQL)
- **Libraries:** react-day-picker, date-fns, Heroicons

## Key Features Implemented

### Authentication & Authorization
- Google OAuth integration with NextAuth.js
- Secure session management
- Protected routes with automatic login redirects
- User-specific data access controls

### Booking System
- Interactive date selection with conflict prevention
- Real-time price calculation based on dates and discounts
- Form validation and server-side processing
- Complete booking management (create, edit, delete)

### State Management
- React Context API for cross-component date state
- Server and client component architecture
- Form state management with loading indicators

### Database Operations
- Full CRUD operations for bookings and user profiles
- Relational data queries with joins
- Data validation and error handling
- Cache revalidation after data changes

## Architecture

### File Structure
```
app/
├── _components/          # Reusable UI components
├── _lib/                # Business logic and utilities
│   ├── actions.js       # Server actions for mutations
│   ├── auth.js          # Authentication configuration  
│   ├── data-service.js  # Database queries
│   └── supabase.js      # Database client
├── account/             # Protected user area
├── cabins/              # Cabin browsing and booking
└── page.js              # Homepage
```

### Key Patterns
- **Server Actions:** Direct form-to-server communication
- **Context API:** Shared state management across components
- **Dynamic Routing:** File-based routing with parameters
- **Authentication Flow:** OAuth integration with custom callbacks

## Getting Started

### Prerequisites
- Node.js (v18+)
- Supabase account
- Google OAuth credentials

### Installation

1. **Clone and install dependencies**
   ```bash
   git clone [repository-url]
   cd wild-oasis
   npm install
   ```

2. **Environment Setup**
   ```bash
   # Create .env.local file with:
   NEXTAUTH_URL=http://localhost:3000
   NEXTAUTH_SECRET=your-secret-key
   AUTH_GOOGLE_ID=your-google-oauth-id
   AUTH_GOOGLE_SECRET=your-google-oauth-secret
   SUPABASE_URL=your-supabase-url  
   SUPABASE_ANON_KEY=your-supabase-anon-key
   ```

3. **Database Setup**
   - Create Supabase project with guests, cabins, and bookings tables
   - Configure Row Level Security policies
   - Add sample cabin data

4. **Run Development Server**
   ```bash
   npm run dev
   ```
   Visit http://localhost:3000 to view the application.

## Learning Outcomes

This project provided hands-on experience with:

- **Modern React Patterns:** Hooks, Context API, Server/Client Components
- **Next.js Features:** App Router, Server Actions, Static Generation
- **Authentication:** OAuth flows, session management, route protection
- **Database Integration:** CRUD operations, relational queries
- **Form Handling:** Server-side processing, validation, loading states
- **Security:** Authentication checks, data isolation, input validation

## Security Features

- Authentication required for all booking operations
- Users can only access their own data
- Server-side form processing and validation
- Secure session management with HTTP-only cookies

## Project Context

This application was built as part of a structured Next.js learning curriculum, focusing on implementing modern full-stack development patterns and understanding real-world application architecture. The styling was provided as part of the course materials using Tailwind CSS and a global CSS file.

---

**Built with Next.js 14** | Learning focused on React patterns and full-stack development
