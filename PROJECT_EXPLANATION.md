# FreeShow Project Explanation

## Overview

**FreeShow** is a free and open-source presentation software designed to display text, lyrics, and multimedia content on large screens. Originally created for churches and venues to show song lyrics, scripture, and presentations, it has evolved into a comprehensive presentation tool used worldwide.

## Project Purpose & Mission

- **Primary Goal**: Provide an easy-to-use, affordable presentation solution for everyone from small churches to large venues
- **Problem Solved**: Addresses the need for affordable presentation software, as existing solutions were either expensive or complex
- **Target Users**: Churches, venues, event organizers, educators, and anyone needing to display content on large screens
- **Open Source Philosophy**: Maintained by ChurchApps organization with community contributions

## Key Features

### Core Presentation Features
- **Slide Shows**: Create and display text-based presentations with custom layouts
- **Scripture Display**: Bible verse presentation with reference handling
- **Media Support**: Video, audio, and image display capabilities
- **Live Streaming**: NDI (Network Device Interface) support for broadcast integration
- **Stage Display**: Separate display for performers/speakers with different content

### Advanced Features
- **Remote Control**: Control presentations remotely via web interface
- **Multi-Output Support**: Display different content on multiple screens simultaneously
- **Real-time Effects**: Visual effects and transitions for presentations
- **Audio Integration**: Audio playback with effects and mixing capabilities
- **Metronome**: Built-in metronome for musical performances
- **Timer System**: Countdown timers and event scheduling
- **Cloud Integration**: Google Drive integration and cloud synchronization

### Professional Features
- **Overlay System**: Add graphics and overlays to presentations
- **Camera Integration**: Live camera feeds and switching
- **Recording**: Built-in recording capabilities for presentations
- **Import/Export**: Support for PowerPoint, PDF, and other formats
- **Template System**: Custom templates and layouts

## Technical Architecture

### Technology Stack
- **Frontend Framework**: Svelte 3 with TypeScript
- **Desktop Framework**: Electron (cross-platform desktop application)
- **Build System**: Vite (fast build tool)
- **Backend**: Node.js with Express servers
- **Database**: SQLite for local data storage
- **Styling**: SCSS/CSS with custom styling system

### Project Structure
```
FreeShow/
├── src/
│   ├── frontend/          # Svelte-based UI components
│   │   ├── components/    # Reusable UI components
│   │   │   ├── show/      # Presentation management
│   │   │   ├── output/    # Display output handling
│   │   │   ├── drawer/    # Side panel components
│   │   │   ├── media/     # Media handling
│   │   │   └── ...
│   │   ├── stores.ts      # Svelte stores for state management
│   │   └── main.ts        # Application entry point
│   ├── electron/          # Electron main process
│   │   ├── IPC/           # Inter-process communication
│   │   ├── output/        # Output window management
│   │   ├── audio/         # Audio processing
│   │   └── index.ts       # Electron entry point
│   ├── server/            # Server components for remote features
│   └── types/             # TypeScript type definitions
├── config/                # Configuration files
│   ├── building/          # Build configuration
│   ├── testing/           # Test configuration
│   └── typescript/        # TypeScript configuration
└── public/                # Static assets
```

### Key Components

#### Frontend (Svelte)
- **Show Components**: Handle presentation creation and editing
- **Output Components**: Manage display output and effects
- **Drawer Components**: Side panels for media, scripture, timers, etc.
- **Input Components**: Form controls and interactive elements

#### Backend (Electron)
- **Main Process**: Application lifecycle and window management
- **Output Helper**: Multi-screen output management
- **IPC System**: Communication between processes
- **Data Storage**: Configuration and project data handling

#### Server Components
- **Remote Control**: Web-based remote control interface
- **Cloud Integration**: Google Drive and other cloud services
- **NDI Support**: Professional broadcast integration

## Development & Building

### Prerequisites
- Node.js (latest LTS version)
- Python 3.12+ with setuptools
- Platform-specific build tools:
  - Windows: Visual Studio with C++ development tools
  - Linux: libfontconfig1-dev

### Development Commands
```bash
npm install          # Install dependencies
npm start           # Start development server
npm run build       # Build for production
npm run release     # Create distribution packages
npm test            # Run tests (Playwright, format, Svelte check)
npm run lint        # Run linters
```

### Build System
- **Development**: Vite dev server with hot reload
- **Production**: Optimized builds for multiple platforms
- **Distribution**: Electron Builder for creating installers
- **Testing**: Playwright for end-to-end testing

## License & Support

- **License**: GNU General Public License v3.0 (GPL-3.0)
- **Funding**: Supported by user donations through ChurchApps
- **Community**: Facebook group for users, GitHub for development
- **Support**: GitHub Issues for bug reports and feature requests

## Use Cases

### Churches & Religious Organizations
- Display song lyrics during worship services
- Show scripture verses and passages
- Create announcements and service information
- Multi-screen setups for different audiences

### Events & Venues
- Conference presentations
- Concert lyric displays
- Educational content presentation
- Live event overlays and graphics

### Broadcasting & Streaming
- NDI integration for professional broadcasts
- Live streaming overlays
- Multi-camera switching
- Remote presentation control

## Notable Dependencies

- **Electron**: Desktop application framework
- **Svelte**: Reactive UI framework
- **Socket.io**: Real-time communication
- **Express**: Web server for remote features
- **SQLite**: Local database
- **Various Media Libraries**: For audio/video processing
- **NDI SDK**: Professional broadcast integration

## Community & Contribution

FreeShow is actively maintained by the ChurchApps organization with contributions from developers worldwide. The project welcomes:
- Bug reports and feature requests
- Code contributions
- Translation help (via Transifex)
- Documentation improvements
- Community support

The project's success relies on community support and donations, making it truly free and accessible to organizations of all sizes.