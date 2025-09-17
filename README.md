# go.travel — AI-Powered Travel Companion

A modern travel planning website with Google Maps integration and AI-powered itinerary generation.

## Features
- **Interactive Google Maps** with Places autocomplete
- **AI-Generated Itineraries** using OpenAI GPT-4
- **Smart destination search** with real-time suggestions
- **Safety features** including emergency contacts and location sharing
- **Mobile-responsive design** with modern UI

## Quick Start

1. **Clone or download** this repository
2. **Get API Keys:**
   - **Google Maps**: [Google Cloud Console](https://console.cloud.google.com/) → Enable Maps JavaScript API & Places API
   - **OpenAI**: [OpenAI Platform](https://platform.openai.com/api-keys) → Create new API key
3. **For local testing**: Replace `'your-openai-api-key-here'` in `index.html` line 830 with your actual OpenAI key
4. **Open** `index.html` in your browser

## API Keys Setup

### Google Maps API
- Already configured in `index.html` with a development key
- **For production**: Replace with your own key and restrict it in Google Cloud Console:
  - Application restrictions → HTTP referrers:
    - `https://your-domain.com/*`
    - `http://localhost/*` (for local testing)
  - API restrictions → enable only:
    - Maps JavaScript API, Places API, Geocoding API

### OpenAI API
- **For development**: Replace placeholder in `index.html` with your actual key
- **For production**: Use environment variables or serverless functions
- Uses GPT-4o-mini model for cost-effective AI generation

### Security Best Practices
- Never commit API keys to version control
- Use `.env.local` for local development (already in `.gitignore`)
- For production: implement serverless proxy or use environment variables
- Rotate keys if accidentally exposed

## How to Use
1. Open `index.html` in a web browser
2. Type a destination (autocomplete suggestions will appear)
3. Fill out the travel form with your preferences
4. Click "Generate My Perfect Itinerary" for AI-powered recommendations
5. Use map controls to find nearby attractions, restaurants, and hospitals

## File Structure
```
gotravel/
├── index.html          # Main application file
├── gotravel.png        # Logo image
├── favicon/            # Favicon files
│   ├── favicon.ico
│   ├── favicon.svg
│   ├── apple-touch-icon.png
│   └── ...
└── README.md           # This file
```

## Security Note
The OpenAI API key is currently embedded in the client-side code for development purposes. For production deployment, consider implementing a backend proxy to keep the API key secure.
