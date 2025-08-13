# Overview

This is a full-stack AI chat application called "IntelliCore" that provides an interactive conversational interface with OpenAI's GPT-4o model via OpenRouter. The application features a modern React frontend with shadcn/ui components and an Express.js backend that handles message processing and AI interactions. Users can engage in conversations with the AI assistant through a clean, responsive chat interface that maintains conversation history per session. The application includes intelligent error handling and graceful fallbacks for API issues.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript, built using Vite for fast development and optimized builds
- **UI Library**: shadcn/ui components built on Radix UI primitives for accessible, customizable interface elements
- **Styling**: Tailwind CSS with CSS variables for theming and responsive design
- **State Management**: TanStack Query (React Query) for server state management, caching, and synchronization
- **Routing**: Wouter for lightweight client-side routing
- **Component Structure**: Modular design with reusable UI components, chat-specific components, and utility hooks

## Backend Architecture
- **Runtime**: Node.js with Express.js server framework
- **Language**: TypeScript with ES modules for type safety and modern JavaScript features
- **API Design**: RESTful endpoints for message operations (GET, POST, DELETE)
- **Development Setup**: Hot module replacement via Vite integration for seamless development experience
- **Error Handling**: Centralized error middleware with proper HTTP status codes and JSON responses

## Data Storage Solutions
- **Database**: PostgreSQL with Neon serverless database integration
- **ORM**: Drizzle ORM for type-safe database operations and schema management
- **Schema**: Users table for authentication and messages table for conversation storage
- **Fallback Storage**: In-memory storage implementation for development and testing scenarios
- **Migration Management**: Drizzle Kit for database schema migrations and synchronization

## Authentication and Authorization
- **Session Management**: PostgreSQL-backed session storage using connect-pg-simple
- **Schema Design**: User authentication prepared with username/password fields
- **Security**: Session-based authentication with secure cookie handling

## AI Integration
- **Provider**: OpenRouter API integration providing access to OpenAI's GPT-4o model
- **Model**: openai/gpt-4o via OpenRouter for reliable access and better rate limits
- **Context Management**: Conversation history maintained per session for contextual responses
- **Message Processing**: Structured message format with role-based categorization (user/assistant)
- **Error Handling**: Intelligent fallback system with helpful user guidance for API issues
- **Validation**: Support for messages up to 8000 characters with real-time character counting

## Development and Build Process
- **Build Tool**: Vite for frontend bundling with React plugin and hot reload
- **Bundling**: esbuild for server-side code compilation and optimization
- **Type Checking**: TypeScript strict mode with comprehensive type definitions
- **Development Environment**: Integrated development server with automatic restart and error overlay

# External Dependencies

## Core Technologies
- **React Ecosystem**: React 18, React DOM, React Hook Form with Zod validation
- **UI Framework**: Radix UI components, Lucide React icons, Tailwind CSS with plugins
- **Backend Framework**: Express.js with CORS, body parsing, and static file serving

## Database and ORM
- **Database**: Neon PostgreSQL serverless database
- **ORM**: Drizzle ORM with Drizzle Kit for migrations
- **Session Store**: connect-pg-simple for PostgreSQL session management

## AI and External Services
- **AI Provider**: OpenAI API (GPT-4o model)
- **API Client**: Official OpenAI JavaScript SDK

## Development Tools
- **Build Tools**: Vite, esbuild, TypeScript compiler
- **Code Quality**: ESLint configuration, Prettier formatting
- **Replit Integration**: Custom error overlay and cartographer plugins for Replit environment