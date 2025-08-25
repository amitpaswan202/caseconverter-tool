# Text Case Converter Web Application

## Overview

This is a Flask-based web application that serves as a clone of ConvertCase.net - an online text transformation tool. The application provides various case conversion functionalities, text manipulation tools, and encoding/decoding capabilities through a clean, user-friendly interface with dark/light mode support. Tools are organized in tabs for easy navigation, with enhanced copy functionality for better user experience.

## Recent Changes

**August 6, 2025**
- Reverted to original tab-based navigation layout per user request
- Enhanced copy functionality with visual feedback (button changes to "Copied!" temporarily)
- Maintained improved copy button behavior while keeping the original interface structure

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Single Page Application (SPA)**: Uses vanilla JavaScript with Bootstrap for responsive UI components
- **Component-based Structure**: Organized with HTML templates, CSS styling, and JavaScript functionality separated into distinct files
- **Theme System**: Implements a toggle-able dark/light mode with CSS custom properties for consistent theming
- **Real-time Processing**: Client-side text transformation without requiring server round-trips for better user experience

### Backend Architecture
- **Flask Web Framework**: Lightweight Python web framework serving as the application foundation
- **Template Rendering**: Uses Jinja2 templating engine for dynamic HTML generation
- **Static File Serving**: Handles CSS, JavaScript, and other static assets through Flask's built-in static file handling
- **Session Management**: Implements session support with configurable secret key from environment variables

### Data Storage Solutions
- **Client-side Storage**: Uses localStorage for persisting user preferences (theme selection)
- **No Database Required**: All text transformations are performed client-side, eliminating the need for persistent data storage
- **Stateless Design**: Server maintains no user state, making the application highly scalable

### Authentication and Authorization
- **No Authentication Required**: Open access application with no user accounts or login requirements
- **Public Access Model**: All functionality available without restrictions or user management

## External Dependencies

### Frontend Libraries
- **Bootstrap 5.3.0**: CSS framework for responsive design and UI components
- **Font Awesome 6.4.0**: Icon library for visual elements and user interface enhancement
- **CDN Delivery**: External libraries served via CDN for improved performance and reduced bundle size

### Backend Dependencies
- **Flask**: Python web framework for request handling and template rendering
- **Python Standard Library**: Uses os module for environment variable access

### Development Tools
- **Environment Variables**: Uses SESSION_SECRET for configuring Flask session management
- **Debug Mode**: Configurable debug mode for development environments

### Browser APIs
- **localStorage**: For persisting user theme preferences
- **DOM Manipulation**: Native JavaScript for real-time text processing and UI updates
- **Clipboard API**: For copy-to-clipboard functionality (implied from UI structure)