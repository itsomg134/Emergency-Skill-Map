# Emergency Skill Map

A real-time emergency response web application that connects people in need with nearby skilled helpers including doctors, plumbers, electricians, blood donors, and first-aid trained individuals.

![Emergency Skill Map Banner](https://via.placeholder.com/1200x400/667eea/ffffff?text=Emergency+Skill+Map)

## Table of Contents
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)
- [Team](#team)

##  Features

### For Users in Need
- ** Real-time Location Detection** - Automatically detects user's location
- ** Interactive Map** - Visual representation of nearby helpers
- ** Filter by Skill** - Find specific types of helpers (doctors, plumbers, etc.)
- ** One-Click Emergency Calling** - Direct call to helpers
- ** Emergency Button** - Quick access to nearest available helper

### For Helpers
- ** Easy Registration** - Simple form to register as a helper
- ** Skill Selection** - Choose from 5 different skill categories
- ** Location Sharing** - Share your location to help others nearby
- ** Availability Toggle** - Mark yourself as available/unavailable
- ** Mobile Responsive** - Works perfectly on all devices

### Helper Categories
| Icon | Skill | Description |
|------|-------|-------------|
|  | Doctor | Medical professionals |
|  | Plumber | Plumbing emergencies |
|  | Electrician | Electrical issues |
|  | Blood Donor | Emergency blood donors |
|  | First-aid | First-aid trained individuals |

##  Tech Stack

### Frontend
- **React 18** - UI library
- **React Router DOM 6** - Navigation and routing
- **Leaflet** - Interactive maps (Free, no API key required)
- **Axios** - HTTP client for API requests
- **CSS3** - Styling with modern features

### Backend
- **JSON Server** - Mock REST API for development
- **RESTful Architecture** - Standard API endpoints

### Development Tools
- **Create React App** - Project bootstrapping
- **npm** - Package management
- **Git** - Version control

##  Project Structure

```
emergency-skill-map/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   │   ├── Navbar.js
│   │   ├── Home.js
│   │   ├── Register.js
│   │   └── Map.js
│   ├── App.js
│   ├── index.js
│   └── index.css
├── db.json
├── package.json
└── README.md
```

##  Installation

### Prerequisites
- Node.js (v14 or higher)
- npm (v6 or higher)
- Git

### Step-by-Step Setup

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/emergency-skill-map.git
cd emergency-skill-map
```

2. **Install dependencies**
```bash
npm install
```

3. **Install additional packages**
```bash
npm install axios react-router-dom leaflet react-leaflet
```

4. **Start JSON Server (Backend)**
```bash
# Install json-server globally
npm install -g json-server

# Start the server
json-server --watch db.json --port 5000
```

5. **Start React Development Server**
```bash
# In a new terminal
npm start
```

6. **Open your browser**
```
http://localhost:3000
```

## 📱 Usage

### Finding Help
1. Open the application
2. Allow location access when prompted
3. Click "Find Help" or navigate to Map page
4. View nearby helpers on the map
5. Click on a helper marker to see details
6. Press "Call Now" for immediate assistance

### Registering as a Helper
1. Click "Register as Helper"
2. Fill in your details:
   - Full Name
   - Mobile Number
   - Skill (select from dropdown)
   - Address
   - Availability status
3. Submit the form
4. Start helping people in your area!

### Helper Markers on Map
-  **Green** - Doctor
-  **Blue** - Plumber
-  **Yellow** - Electrician
-  **Red** - Blood Donor
-  **Gray** - First-aid Trained

## 🔌 API Endpoints

### GET /helpers
Fetch all registered helpers
```json
GET http://localhost:5000/helpers
```

### GET /helpers/:id
Fetch a specific helper
```json
GET http://localhost:5000/helpers/1
```

### POST /helpers
Register a new helper
```json
POST http://localhost:5000/helpers
{
  "name": "John Doe",
  "mobile": "9876543210",
  "skill": "doctor",
  "location": {
    "lat": 28.6139,
    "lng": 77.2090
  },
  "address": "New Delhi",
  "available": true
}
```

### PUT /helpers/:id
Update helper information
```json
PUT http://localhost:5000/helpers/1
{
  "available": false
}
```

### DELETE /helpers/:id
Remove a helper
```json
DELETE http://localhost:5000/helpers/1
```

##  Screenshots

### Home Page
![Home Page](https://via.placeholder.com/800x400/667eea/ffffff?text=Home+Page)

### Registration Form
![Registration](https://via.placeholder.com/800x400/28a745/ffffff?text=Registration+Form)

### Interactive Map
![Map View](https://via.placeholder.com/800x400/dc3545/ffffff?text=Interactive+Map)

### Helper Popup
![Helper Details](https://via.placeholder.com/800x400/ffc107/000000?text=Helper+Details)

## Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Guidelines
- Write clear commit messages
- Update documentation as needed
- Test your changes thoroughly
- Follow the existing code style

##  License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

##  Team

- **Developer** - [Your Name](https://github.com/yourusername)
- **UI/UX Designer** - [Designer Name](https://github.com/designer)

##  Acknowledgments

- Leaflet.js for the amazing mapping library
- React team for the fantastic framework
- OpenStreetMap contributors
- All the helpers who make this platform valuable

## 📞 Support

For support, email support@emergencyskillmap.com or create an issue in the GitHub repository.

