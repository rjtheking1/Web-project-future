# SecureShield - Enterprise Cybersecurity Solutions

## Overview

SecureShield is a modern cybersecurity services company website built as a single-page application. The platform showcases enterprise-grade security services including penetration testing, vulnerability assessment, threat intelligence, and incident response. The site features a dark-themed, professional design inspired by industry leaders like CrowdStrike and Palo Alto Networks, with a comprehensive service catalog, pricing plans, team profiles, case studies, educational resources, and a demo booking system.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Framework & Build System**
- React 18 with TypeScript for type-safe component development
- Vite as the build tool and development server for fast HMR and optimized production builds
- Wouter for client-side routing (lightweight alternative to React Router)
- Single-page application (SPA) architecture with component-based design

**UI Component System**
- Shadcn UI component library (New York style variant) built on Radix UI primitives
- Tailwind CSS for utility-first styling with custom design tokens
- Dark mode as the primary theme with sophisticated navy-charcoal color scheme
- Custom color palette emphasizing cyber blue accents, purple secondary actions, and security-focused green/red indicators
- Responsive design with mobile-first approach

**State Management & Data Fetching**
- TanStack Query (React Query) for server state management and caching
- Custom query client configuration with API request helpers
- Form state managed with React Hook Form and Zod validation

**Design System**
- Typography: Inter/Outfit for headings, Inter/DM Sans for body text, JetBrains Mono for code
- Consistent spacing primitives using Tailwind's 4-unit scale
- Elevation system with hover and active states for interactive elements
- Professional cybersecurity aesthetic with trust indicators and clear visual hierarchy

### Backend Architecture

**Server Framework**
- Express.js as the web server framework
- Node.js runtime with ESM module support
- TypeScript for type safety across the full stack

**API Design**
- RESTful API endpoints under `/api` prefix
- JSON request/response format
- Centralized error handling middleware
- Request logging with duration tracking for API calls

**Storage Layer**
- In-memory storage implementation (MemStorage) for development
- Interface-based storage design (IStorage) allowing easy swap to persistent databases
- UUID-based record identification
- Support for user management and demo booking entities

**Development Tooling**
- Vite middleware integration for HMR in development
- Custom logging system with timestamped console output
- Runtime error overlay for improved developer experience
- Replit-specific plugins for cartographer and dev banner

### Database Schema

**Drizzle ORM Configuration**
- PostgreSQL as the target database (via @neondatabase/serverless)
- Schema-first approach with Drizzle Kit for migrations
- Type-safe database operations with drizzle-orm

**Data Models**
- **Users Table**: ID (UUID), username (unique), password - for future authentication
- **Demo Bookings Table**: ID (UUID), name, email, company (optional), service, preferred date/time, message, created timestamp
- Zod schemas for runtime validation (insertUserSchema, insertDemoBookingSchema)
- TypeScript types generated from schema definitions

**Storage Strategy**
- Current: In-memory storage for rapid development and testing
- Future: PostgreSQL with Drizzle ORM (connection string via DATABASE_URL environment variable)
- Migration path: `db:push` script to sync schema changes

### Build & Deployment

**Build Process**
- Client: Vite builds React app to `dist/public`
- Server: esbuild bundles Express server to `dist/index.js` with external packages
- Production mode serves static assets from dist directory

**Environment Configuration**
- NODE_ENV-based configuration (development/production)
- Database connection via DATABASE_URL environment variable
- Type-safe environment validation

## External Dependencies

### UI & Component Libraries
- **Radix UI**: Accessible component primitives (accordion, dialog, dropdown, popover, select, tabs, toast, tooltip, etc.)
- **Shadcn UI**: Pre-built component system with customizable variants
- **Tailwind CSS**: Utility-first CSS framework with custom configuration
- **Lucide React**: Icon library for UI elements
- **React Icons**: Additional icon sets (Font Awesome alternatives)

### Data Management
- **TanStack Query v5**: Server state management and caching
- **React Hook Form**: Form state management with performance optimization
- **Zod**: Runtime type validation and schema definition
- **@hookform/resolvers**: Integration between React Hook Form and Zod

### Database & ORM
- **Drizzle ORM**: TypeScript-first ORM for PostgreSQL
- **Drizzle Kit**: Schema management and migration tools
- **Drizzle Zod**: Zod schema generation from Drizzle tables
- **@neondatabase/serverless**: Serverless PostgreSQL driver for Neon

### Development Tools
- **Vite**: Fast build tool with HMR
- **TypeScript**: Type safety across the stack
- **ESBuild**: Fast JavaScript bundler for production server build
- **Replit Plugins**: Runtime error modal, cartographer, dev banner for Replit environment

### Utilities
- **date-fns**: Date manipulation and formatting
- **clsx & tailwind-merge**: Conditional className utilities
- **cmdk**: Command palette component
- **class-variance-authority**: Type-safe variant styling
- **Embla Carousel**: Carousel/slider functionality

### Routing
- **Wouter**: Lightweight client-side routing library (alternative to React Router)

### Session Management (Configured but not active)
- **connect-pg-simple**: PostgreSQL session store for Express sessions (ready for authentication implementation)