# Native App Maker

A web application that converts any website into a native desktop app by generating AppImage files. Built with React, TypeScript, Vite, and Tauri.

## Features

- **First-Time User Experience**: Welcoming landing page for new visitors
- **URL Input Interface**: Simple form to enter website URLs
- **AppImage Generation**: Converts websites into downloadable AppImage files
- **Responsive Design**: Modern UI built with Tailwind CSS
- **Cross-Platform**: Frontend ready for desktop deployment via Tauri

## Tech Stack

- **Frontend**: React 19, TypeScript, Vite
- **Styling**: Tailwind CSS v4
- **Build Tool**: Vite
- **Desktop App**: Tauri (Rust backend)
- **Linting**: ESLint with TypeScript support

## Project Structure

```
native-app-maker/
├── src/
│   ├── components/
│   │   └── UrlInput.tsx          # Reusable URL input component
│   ├── pages/
│   │   ├── Landing.tsx           # Welcome page for first-time users
│   │   └── Wrapper.tsx           # Main app interface with URL input and download
│   ├── App.tsx                   # Main app component with routing logic
│   ├── main.tsx                  # React app entry point
│   └── index.css                 # Global styles with Tailwind imports
├── src-tauri/                    # Tauri backend (Rust)
│   ├── src/
│   │   └── main.rs
│   ├── tauri.conf.json
│   └── icons/
├── public/                       # Static assets
├── package.json                  # Node.js dependencies
├── vite.config.ts                # Vite configuration
├── tailwind.config.js            # Tailwind CSS configuration
├── postcss.config.cjs            # PostCSS configuration for Tailwind
├── tsconfig.json                 # TypeScript configuration
└── README.md
```

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- Rust (for Tauri development)

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd native-app-maker
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Open [http://localhost:5173](http://localhost:5173) in your browser

### Building for Production

```bash
npm run build
```

### Running Tauri App

```bash
npm run tauri dev
```

## Usage

1. **First Visit**: Users see a welcoming landing page with app features
2. **Get Started**: Click the button to access the main interface
3. **Enter URL**: Input the website URL you want to convert
4. **Generate App**: Click "Generate App" to create the AppImage
5. **Download**: Download the generated AppImage file

## Development

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint
- `npm run tauri dev` - Run Tauri development app
- `npm run tauri build` - Build Tauri app

### Key Components

- **App.tsx**: Manages app state and conditional rendering
- **Landing.tsx**: First-time user welcome page
- **Wrapper.tsx**: Main functionality with URL input and file generation
- **UrlInput.tsx**: Controlled input component for URLs

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests and linting
5. Submit a pull request
