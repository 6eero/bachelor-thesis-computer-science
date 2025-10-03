# CRM Project Management System

A modern, cloud-native Customer Relationship Management system built with Next.js for managing and monitoring company projects throughout their lifecycle.

## Overview

This CRM system was developed as a thesis project at the University of Udine's Department of Mathematical, Computer and Physical Sciences. It provides a centralized dashboard for tracking ongoing projects, archiving completed work, and planning future initiatives.

## Key Features

- **Project Management**: Complete CRUD operations for project lifecycle management
- **Role-Based Access Control**: Differentiated permissions for Admins and Project Managers
- **User Management**: Invite-only system with secure authentication
- **Project Tracking**: Monitor project status, timelines, and assigned personnel
- **Cloud-Native Architecture**: Built on AWS infrastructure for scalability and reliability

## Tech Stack

### Frontend
- **Next.js 14**: React framework with server-side rendering and static generation
- **React 18**: Component-based UI library with hooks
- **TypeScript**: Static typing for enhanced code quality
- **Tailwind CSS**: Utility-first CSS framework
- **Next UI**: Pre-built UI component library
- **Formik**: Form management and validation

### Backend & Infrastructure
- **AWS Amplify**: Continuous deployment and hosting
- **AWS Cognito**: User authentication and authorization
- **AWS DynamoDB**: NoSQL database for project data
- **Amazon Web Services**: Complete cloud infrastructure

## Architecture

The application follows a modern web architecture pattern:

- **Server-Side Rendering (SSR)**: Dynamic pages rendered on-demand
- **Static Site Generation (SSG)**: Pre-rendered pages for optimal performance
- **API Routes**: Next.js API endpoints for database operations
- **Context-Based State Management**: Global state using React Context

## Project Structure

```
├── app/                    # Next.js app directory
│   ├── projects/          # Project management pages
│   ├── users/             # User management (Admin only)
│   └── performances/      # Analytics and reporting
├── api/                   # API endpoint definitions
│   └── Project/           # Project CRUD operations
├── components/            # Reusable React components
└── Context/              # Global state management
```

## User Roles

### Admin
- Full access to all system features
- Create and manage user accounts
- View and modify all projects
- Access user management section
- Assign projects to Project Managers

### Project Manager
- View assigned projects only
- Create, update, and delete assigned projects
- Limited dashboard access
- No user management privileges

## Key Functionalities

### Authentication Flow
1. Admin creates user account via AWS Cognito
2. New user receives email with temporary password
3. First login requires password change
4. Subsequent logins use permanent credentials

### Project Management
- **Create**: Define project code, name, dates, status, and assignments
- **Read**: View all projects (Admin) or assigned projects (PM)
- **Update**: Modify project details with form validation
- **Delete**: Remove projects with confirmation modal

### Project States
- Not Started
- In Progress
- Completed

## Development Approach

The project was developed using Agile methodologies:

- **Iterative Development**: Short cycles with continuous feedback
- **Pair Programming**: Collaborative coding sessions
- **Extreme Programming (XP)**: Focus on code quality and refactoring
- **Continuous Integration**: Automated deployment via AWS Amplify

## Testing

Testing focused on acceptance testing with end users:

- **Black Box Testing**: Functional verification without code inspection
- **CRUD Operations**: Comprehensive testing of all database operations
- **Role-Based Access**: Verification of permission systems
- **User Experience**: Real-world scenario testing with stakeholders

## Future Enhancements

- **Advanced State Management**: Migration to Context + Reducer pattern
- **Data Analytics**: Comprehensive performance reports and metrics
- **Security Testing**: Penetration testing and vulnerability assessments
- **Accessibility**: WCAG 2.1 compliance and keyboard navigation
- **User Management UI**: In-app user administration without Cognito dashboard

## Performance

The system demonstrates:
- Fast response times for CRUD operations
- Efficient server-side rendering
- Optimized client-side hydration
- Scalable cloud infrastructure

## License

This work is shared under the Creative Commons 4.0 License Attribution-NonCommercial-ShareAlike.

## Author

**Alessandro Gerotto**  
University of Udine  
Academic Year 2023-2024

**Academic Supervisor**: Prof. Vincenzo Riccio  
**Company Tutor**: Yannick Ponte  
**Company**: Archeido

## Acknowledgments

Special thanks to Archeido for providing the opportunity to develop this system, and to the team members who contributed through pair programming sessions and feedback throughout the development process.
