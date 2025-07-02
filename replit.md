# Portfolio Web Application

## Overview

This is a full-stack portfolio web application built for Shahzaib, an AI Engineer and Full Stack Developer from IBA Karachi. The application showcases professional work, services, and provides a contact form for potential clients. It's built using modern web technologies with a React frontend and Express backend, designed to be deployed on Replit with PostgreSQL database support.

## System Architecture

The application follows a monorepo structure with clear separation between client and server code:

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for lightweight client-side routing
- **UI Framework**: Shadcn/ui components with Radix UI primitives
- **Styling**: Tailwind CSS with custom portfolio theme
- **State Management**: TanStack React Query for server state
- **Form Handling**: React Hook Form with Zod validation
- **Build Tool**: Vite for fast development and optimized builds

### Backend Architecture
- **Runtime**: Node.js with TypeScript
- **Framework**: Express.js with REST API endpoints
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Schema Validation**: Zod for runtime type checking
- **Development**: Hot reloading with tsx

## Key Components

### Client Structure
- **Pages**: Single portfolio page with sections (hero, about, services, projects, contact)
- **Components**: Reusable UI components built on Shadcn/ui
- **Forms**: Contact form with validation and API integration
- **Navigation**: Smooth scrolling navigation with mobile responsiveness

### Server Structure
- **Routes**: RESTful API endpoints for contact form submissions
- **Storage**: Abstract storage interface with memory implementation (ready for database)
- **Middleware**: Request logging, error handling, and JSON parsing
- **Validation**: Server-side validation using shared Zod schemas

### Database Schema
- **Users Table**: Basic user authentication structure
- **Contact Messages Table**: Stores form submissions with timestamps
- **Shared Types**: TypeScript types generated from Drizzle schemas

## Data Flow

1. **Client-side**: User interacts with portfolio sections and contact form
2. **Form Submission**: React Hook Form validates data using Zod schemas
3. **API Request**: TanStack Query sends POST request to `/api/contact`
4. **Server Processing**: Express validates and stores contact messages
5. **Response**: Success/error feedback displayed via toast notifications
6. **Storage**: Currently uses in-memory storage, configured for PostgreSQL

## External Dependencies

### UI and Styling
- **Radix UI**: Accessible component primitives
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Icon library
- **React Icons**: Additional icon sets

### Form and Validation
- **React Hook Form**: Performance-focused form library
- **Zod**: TypeScript-first schema validation
- **Hookform Resolvers**: Zod integration for React Hook Form

### Data Management
- **TanStack React Query**: Server state management
- **Drizzle ORM**: Type-safe database toolkit
- **Neon Database**: Serverless PostgreSQL provider

### Development Tools
- **Vite**: Build tool and dev server
- **TypeScript**: Type safety and better DX
- **ESBuild**: Fast JavaScript bundler for production

## Deployment Strategy

### Development Environment
- **Platform**: Replit with Node.js 20 runtime
- **Database**: PostgreSQL 16 module
- **Port Configuration**: Server runs on port 5000, mapped to external port 80
- **Hot Reloading**: Automatic restart on file changes

### Production Build
- **Frontend**: Vite builds optimized static assets to `dist/public`
- **Backend**: ESBuild bundles server code to `dist/index.js`
- **Database**: Drizzle manages schema migrations and connections
- **Environment**: Production mode with optimized settings

### Build Process
1. `npm run build` - Builds both client and server
2. Client assets compiled to `dist/public`
3. Server code bundled with external dependencies
4. Database schema pushed via `npm run db:push`

## Changelog

Changelog:
- June 26, 2025. Initial setup
- June 26, 2025. Updated contact email to aslamshazaib@gmail.com
- June 26, 2025. Updated contact phone to +92 307 0081159
- June 26, 2025. Updated education details: BS Accounting & Finance at IBA Karachi, O & A Levels from The City School

## User Preferences

Preferred communication style: Simple, everyday language.