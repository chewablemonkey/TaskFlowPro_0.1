# Overview

WorkFlow Pro is an enterprise-level project management platform built with a modern full-stack architecture. The application provides comprehensive task management, project organization, user management, and team collaboration features designed for enterprise workflows. It supports hierarchical project structures, role-based access control, and real-time collaboration capabilities.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query (React Query) for server state management and caching
- **UI Library**: Radix UI primitives with shadcn/ui components for consistent design system
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **Build Tool**: Vite for fast development and optimized production builds

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript for type safety across the entire stack
- **API Design**: RESTful API following conventional HTTP methods and status codes
- **Authentication**: Replit Auth integration with OpenID Connect and JWT tokens
- **Session Management**: Express sessions with PostgreSQL storage using connect-pg-simple
- **Database ORM**: Drizzle ORM with type-safe database queries and migrations
- **File Structure**: Monorepo structure with shared schema definitions between client and server

## Data Storage
- **Primary Database**: PostgreSQL with Neon serverless database
- **Schema Management**: Drizzle Kit for database migrations and schema versioning
- **Connection Pool**: Neon serverless connection pooling for scalability
- **Session Storage**: PostgreSQL table for secure session persistence

## Authentication & Authorization
- **Primary Auth**: Replit Auth with OpenID Connect flow
- **Session Security**: HTTP-only cookies with secure flags and CSRF protection
- **Role-Based Access**: Four-tier role system (Admin, Manager, Employee, Guest)
- **Route Protection**: Server-side middleware for API endpoint protection
- **Client Protection**: React components with authentication checks

## Core Data Models
- **Users**: Role-based user system with profile management
- **Projects**: Hierarchical project structure with status tracking
- **Tasks**: Comprehensive task management with dependencies, priorities, and time tracking
- **Comments**: Task discussion and collaboration system
- **Project Members**: Many-to-many relationship for project team assignments

## Development Architecture
- **Type Safety**: Shared TypeScript schemas using Drizzle-Zod for validation
- **Code Organization**: Clear separation between client, server, and shared code
- **Development Tools**: Hot module replacement with Vite, TypeScript checking
- **Error Handling**: Centralized error handling with proper HTTP status codes
- **Logging**: Request/response logging with performance metrics

# External Dependencies

## Database Services
- **Neon Database**: Serverless PostgreSQL database with connection pooling
- **connect-pg-simple**: PostgreSQL session store for Express sessions

## Authentication Services  
- **Replit Auth**: Primary authentication provider with OpenID Connect
- **openid-client**: OpenID Connect client library for authentication flows
- **Passport.js**: Authentication middleware for Express

## Frontend Libraries
- **TanStack Query**: Server state management and data fetching
- **Radix UI**: Accessible UI primitives for form controls and interactive elements
- **Wouter**: Lightweight routing library for single-page application navigation
- **date-fns**: Date manipulation and formatting utilities
- **Tailwind CSS**: Utility-first CSS framework with design system variables

## Development Dependencies
- **Vite**: Build tool and development server with hot module replacement
- **Drizzle Kit**: Database schema management and migration tools  
- **TypeScript**: Type checking and compilation across the entire stack
- **ESBuild**: Fast JavaScript bundler for production builds

## UI Component System
- **shadcn/ui**: Pre-built accessible components built on Radix UI
- **Lucide React**: Icon library with consistent design language
- **Class Variance Authority**: Type-safe styling variants for components