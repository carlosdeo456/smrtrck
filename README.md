# SmartTrack - Intercity Parcel Tracking System

A comprehensive IoT-based parcel tracking solution for intercity transportation with real-time monitoring of location, temperature, humidity, and RFID scanning.

## Features

- 🌍 **Real-time GPS Tracking** - Live parcel location on interactive map
- 🌡️ **Environmental Monitoring** - Temperature & humidity tracking with alerts
- 📍 **RFID Integration** - Automated checkpoint scanning
- 🚨 **Smart Alerts** - Anomaly detection & notifications
- 📊 **Analytics Dashboard** - Shipment insights & reporting
- 👨‍💼 **Multi-user System** - Admin, Drivers, Customers
- 📱 **Responsive Design** - Works on desktop & mobile

## Tech Stack

**Frontend:**
- React.js
- Leaflet/Mapbox (mapping)
- Socket.io-client (real-time updates)
- Tailwind CSS

**Backend:**
- Node.js + Express.js
- PostgreSQL
- Socket.io (WebSocket)
- JWT Authentication
- MQTT/REST for IoT devices

**Infrastructure:**
- Local development with Node.js
- PostgreSQL database
- AWS/GCP/Azure ready for production

## Project Structure

```
smartrack/
├── backend/              # Express.js API server
│   ├── src/
│   │   ├── models/      # Database models
│   │   ├── routes/      # API endpoints
│   │   ├── controllers/ # Business logic
│   │   ├── middleware/  # Auth, validation
│   │   ├── services/    # Core services
│   │   └── utils/       # Helper functions
│   ├── config/          # Configuration files
│   ├── .env.example
│   └── package.json
│
├── frontend/            # React.js dashboard
│   ├── src/
│   │   ├── components/  # React components
│   │   ├── pages/       # Page views
│   │   ├── services/    # API calls
│   │   ├── hooks/       # Custom hooks
│   │   ├── context/     # Context API
│   │   ├── styles/      # Tailwind CSS
│   │   └── App.js
│   ├── public/
│   └── package.json
│
├── iot-device/          # IoT device code (Arduino/Raspberry Pi)
│   ├── gps_tracker.ino
│   ├── sensor_reader.py
│   └── rfid_scanner.py
│
├── database/
│   └── schema.sql       # PostgreSQL schema
│
├── scripts/
│   └── setup.js         # First-time setup helper
│
├── package.json         # Root dev scripts (npm run dev)
├── .gitignore
└── docs/               # Documentation
```

## Installation & Setup

### Prerequisites
- Node.js 16+
- PostgreSQL 12+
- npm

### Quick Start (recommended)

```bash
npm install              # Install root dev tools
npm run setup            # Install deps + create .env files
# Edit backend/.env with your PostgreSQL connection
npm run migrate          # Apply database schema
npm run dev              # Start backend + frontend together
```

Open http://localhost:3000 (frontend) and http://localhost:5000 (API).

### Manual Setup

```bash
# Backend
cd backend
npm install
cp .env.example .env
npm run migrate
npm run dev

# Frontend (separate terminal)
cd frontend
npm install
npm start
```

## Environment Variables

See `.env.example` files in backend and frontend directories.

## API Documentation

See `docs/API.md` for detailed endpoint documentation.

## Database Schema

See `database/schema.sql` for complete database structure.

## IoT Device Integration

See `iot-device/README.md` for sensor and RFID setup instructions.

## Contributing

1. Create feature branch: `git checkout -b feature/your-feature`
2. Commit changes: `git commit -m "Add feature"`
3. Push: `git push origin feature/your-feature`
4. Create Pull Request

## License

MIT License - See LICENSE file

## Support

For issues and questions, please open an issue in the repository.
