# go.travel — AI-Powered Travel Companion

A modern travel planning website with Google Maps integration and AI-powered itinerary generation.

## Features
- **Interactive Google Maps** with Places autocomplete
- **AI-Generated Itineraries** using OpenAI GPT-4
- **Smart destination search** with real-time suggestions
- **Safety features** including emergency contacts and location sharing
- **Mobile-responsive design** with modern UI

## API Keys Setup

### Google Maps API
- Already configured in `index.html`
- Restrict the key in Google Cloud Console for security:
  - Application restrictions → HTTP referrers:
    - `https://gotravel-cac.github.io/*`
    - `http://localhost/*` (for local testing)
  - API restrictions → enable only:
    - Maps JavaScript API, Places API, Geocoding API

### OpenAI API
- **For development**: Replace `'your-openai-api-key-here'` in `index.html` with your actual key
- **For production**: Use environment variables or serverless functions
- Copy `.env.example` to `.env.local` and add your key
- Uses GPT-4o-mini model for cost-effective AI generation

### Security Note
- Never commit API keys to version control
- The `.gitignore` file is configured to protect environment files
- For production deployment, use serverless functions or environment variables

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
