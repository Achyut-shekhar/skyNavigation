# ✈️ Sky Navigation - Airport Distance Calculator & Route Planner

A modern, interactive web application built with React and Vite that visualizes worldwide airports on an interactive Leaflet map. Calculate distances between airports, visualize air traffic, check weather conditions, find shortest routes, and identify dangerous no-fly zones across the globe.

## 🚀 Features

### Core Functionality
- 🌍 **Interactive Leaflet Map** - Smooth zoom, pan, and explore functionality with worldwide airport coverage
- 📍 **Global Airport Database** - Access to thousands of airports worldwide using the OpenFlights dataset
- 📏 **Distance Calculator** - Calculate great-circle distance between any two airports with estimated flight time
- 🛤️ **Shortest Route Finder** - Find optimal flight paths between airports using advanced pathfinding algorithms
- ✈️ **Real-time Air Traffic** - Visualize live air traffic data on the map
- 🌤️ **Weather Information** - Check weather conditions along your flight route
- ⚠️ **Danger Zones Visualization** - Identifies and highlights restricted airspaces including:
  - Bermuda Triangle
  - Dragon's Triangle
  - North Korea No-Fly Zone
  - Other restricted zones with real geo-coordinates

### User Interface
- 🎨 **Modern React UI** - Built with React 19 and styled with Tailwind CSS
- 🔄 **Smooth Animations** - Enhanced user experience with Framer Motion animations
- 📱 **Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- 🧭 **Intuitive Navigation** - Easy-to-use interface with clear section navigation

## 🛠️ Tech Stack

### Frontend Framework
- **React 19** - Latest React with improved performance
- **Vite 6** - Next-generation frontend tooling for fast development
- **JavaScript (ES6+)** - Modern JavaScript features

### UI & Styling
- **Tailwind CSS 4** - Utility-first CSS framework
- **Framer Motion** - Production-ready animation library
- **React Icons & Lucide React** - Beautiful icon libraries
- **FontAwesome** - Additional icon support

### Mapping & Data
- **Leaflet.js 1.9.4** - Leading open-source JavaScript library for interactive maps
- **Axios** - Promise-based HTTP client for API requests
- **PapaParse** - Fast CSV parser for airport data

### Development Tools
- **ESLint** - Code linting and quality checks
- **PostCSS & Autoprefixer** - CSS processing and vendor prefixing

## 📋 Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Node.js** (version 18.x or higher recommended)
- **npm** (comes with Node.js) or **yarn** or **pnpm**

To check if Node.js and npm are installed, run:
```bash
node --version
npm --version
```

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Achyut-shekhar/skyNavigation.git
cd skyNavigation
```

### 2. Navigate to Project Directory

```bash
cd skynavigation
```

### 3. Install Dependencies

Using npm:
```bash
npm install
```

Or using yarn:
```bash
yarn install
```

Or using pnpm:
```bash
pnpm install
```

This will install all required dependencies listed in `package.json`, including React, Vite, Leaflet, Tailwind CSS, and other libraries.

## 🏃 Running the Application

### Development Mode

Start the development server with hot module replacement (HMR):

```bash
npm run dev
```

The application will be available at `http://localhost:5173` (default Vite port). The page will automatically reload when you make changes to the code.

### Build for Production

Create an optimized production build:

```bash
npm run build
```

This command will:
- Bundle and minify all JavaScript and CSS files
- Optimize assets and images
- Generate static files in the `dist/` directory

### Preview Production Build

Preview the production build locally before deployment:

```bash
npm run preview
```

This serves the production build from the `dist/` folder, typically at `http://localhost:4173`.

### Linting

Run ESLint to check code quality and catch potential errors:

```bash
npm run lint
```

## 📂 Project Structure

```
skyNavigation/
│
├── skynavigation/              # Main application directory
│   ├── public/                 # Public static assets
│   ├── src/                    # Source code
│   │   ├── components/         # React components
│   │   │   ├── Header.jsx      # App header/navigation
│   │   │   ├── Map.jsx         # Main Leaflet map component
│   │   │   ├── ControlPanel.jsx # Control panel for interactions
│   │   │   └── FadeTransition.jsx # Animation wrapper
│   │   ├── pages/              # Page components
│   │   │   ├── air_traffic.jsx # Air traffic visualization
│   │   │   ├── weather.jsx     # Weather information
│   │   │   ├── shortest_route.jsx # Route calculation
│   │   │   └── Contact.jsx     # Contact page
│   │   ├── data/               # Data files
│   │   │   ├── airports.csv    # Airport database
│   │   │   ├── airportsData.js # Airport data utilities
│   │   │   └── DangerZone.js   # Danger zone coordinates
│   │   ├── utils/              # Utility functions
│   │   ├── assets/             # Images, icons, etc.
│   │   ├── App.jsx             # Main App component
│   │   ├── App.css             # App styles
│   │   ├── main.jsx            # Application entry point
│   │   └── index.css           # Global styles
│   ├── index.html              # HTML entry point
│   ├── package.json            # Dependencies and scripts
│   ├── vite.config.js          # Vite configuration
│   ├── eslint.config.js        # ESLint configuration
│   └── README.md               # Project documentation
│
└── README.md                   # This file
```

## ✅ How It Works

1. **Select Airports**: Click on airport markers on the interactive map to select source and destination
2. **Calculate Distance**: The app uses the Haversine formula to calculate great-circle distance
3. **View Route**: See the flight path visualized as a line on the map
4. **Check Weather**: Get weather information along your route
5. **Find Shortest Path**: Use the route optimizer to find the most efficient path
6. **Avoid Danger Zones**: Danger zones are displayed as polygon/circle overlays to help with flight planning
7. **View Air Traffic**: See real-time air traffic data visualized on the map

## 🎯 Available Features by Section

### Distance Calculator
- Select source and destination airports
- View calculated distance in kilometers/miles
- See estimated flight time
- Visualize the route on the map

### Air Traffic
- View real-time flight data
- See aircraft positions on the map
- Track flight paths

### Weather
- Check weather conditions along routes
- View weather at specific airports
- Plan routes based on weather safety

### Shortest Route
- Calculate optimal flight paths
- Consider multiple waypoints
- Optimize for distance or time

## 🐛 Troubleshooting

### Port Already in Use

If you see an error that the port is already in use, you can:
- Stop the process using that port
- Or specify a different port:
  ```bash
  npm run dev -- --port 3000
  ```

### Dependencies Installation Issues

If you encounter issues during `npm install`:
1. Clear npm cache: `npm cache clean --force`
2. Delete `node_modules` folder and `package-lock.json`
3. Run `npm install` again

### Build Errors

If the build fails:
1. Ensure all dependencies are installed: `npm install`
2. Check for Node.js version compatibility (18.x or higher)
3. Clear the build cache: `rm -rf dist node_modules/.vite`

## 🌐 Deployment

The built application (from `npm run build`) can be deployed to various platforms:

- **GitHub Pages**: Static hosting for GitHub repositories
- **Netlify**: Drag-and-drop deployment or connect to GitHub
- **Vercel**: Optimized for frontend frameworks
- **AWS S3/CloudFront**: For enterprise deployments

Simply deploy the contents of the `dist/` folder after running the build command.

## 📈 Upcoming Features

- [ ] Filter airports by country, type, or IATA code
- [ ] Enhanced flight path optimization algorithms
- [ ] Multi-stop route planning
- [ ] Save and share routes
- [ ] User accounts and preferences
- [ ] Historical weather data
- [ ] Flight cost estimation
- [ ] Mobile app version
- [ ] Backend integration for persistent data storage

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/YourFeature`
3. Make your changes
4. Run tests and linting: `npm run lint`
5. Commit your changes: `git commit -m 'Add some feature'`
6. Push to the branch: `git push origin feature/YourFeature`
7. Submit a pull request

Please ensure your code follows the existing style and passes all linting checks.

## 📝 License

This project is open source and available under the MIT License.

## 📧 Contact

For questions, suggestions, or issues, please open an issue on GitHub or contact the maintainers.

---

**Made with ❤️ for aviation enthusiasts and developers**
