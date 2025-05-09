# MeetNing - Smart Appointment Scheduling Application

MeetNing is an AI-powered appointment scheduling application that helps users manage their calendars, schedule meetings efficiently, and coordinate with team members.

## Features

- **User Authentication**: Secure signup and login functionality
- **Smart Scheduling**: AI-powered scheduling assistant that suggests optimal meeting times
- **Calendar Integration**: Connect with Google Calendar, Outlook, and other providers
- **Appointment Management**: Create, view, edit, and delete appointments
- **Video Conferencing**: Automatic generation of Google Meet links
- **Time Zone Intelligence**: Automatic handling of time zone differences
- **Team Coordination**: Schedule meetings with multiple participants
- **Notifications**: Automatic reminders for upcoming appointments

## Project Structure

```
fe/ - Frontend (Next.js)
├── public/
├── src/
│   ├── app/ - Next.js app router
│   │   ├── (authenticated)/ - Protected routes
│   │   │   ├── appointments/ - Appointment management
│   │   │   ├── calendar/ - Calendar view
│   │   │   ├── dashboard/ - User dashboard
│   │   │   └── settings/ - User settings
│   │   ├── auth/ - Authentication pages
│   │   │   ├── login/ - Login page
│   │   │   └── signup/ - Signup page
│   │   ├── api/ - API routes
│   │   │   └── nylas/ - Nylas API integration
│   │   └── page.tsx - Landing page
│   ├── components/ - Reusable components
│   │   ├── ui/ - UI components
│   │   └── layout/ - Layout components
│   └── lib/ - Utility functions and services
│       ├── auth-context.tsx - Authentication context
│       └── api/ - API service files
be/ - Backend
```

## Tech Stack

- **Frontend**: Next.js 14, React, TypeScript
- **Styling**: Tailwind CSS
- **Form Handling**: React Hook Form with Zod validation
- **API Integration**: Nylas API for calendar management
- **Authentication**: JWT-based authentication
- **Icons**: Lucide React

## Getting Started

### Prerequisites

- Node.js 18+ and npm/yarn
- Nylas API credentials (for calendar integration)

### Installation

1. Clone the repository

```
git clone <repository-url>
cd MeetNing-Appointment-AI
```

2. Install dependencies

```
# Install frontend dependencies
cd fe
npm install

# Install backend dependencies
cd ../be
npm install
```

3. Set up environment variables

Create a `.env.local` file in the `fe` directory with the following variables:

```
NEXT_PUBLIC_API_URL=http://localhost:3000/api
NYLAS_CLIENT_ID=your_nylas_client_id
NYLAS_CLIENT_SECRET=your_nylas_client_secret
```

4. Start the development servers

```
# Start frontend
cd fe
npm run dev

# Start backend (in a separate terminal)
cd be
npm run dev
```

5. Open [http://localhost:3000](http://localhost:3000) to view the application

## Key Components

- **Authentication Context**: Manages user authentication state across the application
- **Smart Scheduler**: AI-powered component for suggesting optimal meeting times
- **Calendar Views**: Daily, weekly, and monthly calendar views
- **Appointment Form**: Form for creating and editing appointments
- **Settings Page**: User profile and preference management

## Integration with Nylas

MeetNing uses the Nylas API for calendar integration. This allows users to:

- Connect their Google, Outlook, or Exchange calendars
- Fetch and display events from connected calendars
- Create, modify, and delete events that sync with their calendar provider
- Check availability across multiple calendars

## Future Enhancements

- **Natural Language Processing**: Allow users to create appointments using natural language
- **Advanced Analytics**: Provide insights into meeting patterns and productivity
- **Mobile Application**: Develop native mobile apps for iOS and Android
- **Calendar Sharing**: Enable sharing calendars with team members
- **Recurring Appointments**: Support for setting up recurring meetings
