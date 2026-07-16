# Voices Around Us

A mobile app that enables people to share and discover stories from their community. Built as a submission to UCLA ACM Hack's HOTH XII hackathon.

> More details on Devpost: https://devpost.com/software/voices-around-us?ref_content=my-projects-tab&ref_feature=my_projects

---

## About

**Voices Around Us** is a mobile application designed to foster genuine human connection by allowing users to share and explore authentic stories from their local community. The app makes it easy for people to contribute their experiences through audio and text, discover stories from others on an interactive map, and build meaningful connections around shared narratives.

## Features

- 🗺️ **Interactive Map View** - Discover stories pinned to their geographic locations
- 🎙️ **Voice & Audio Stories** - Share stories via audio recordings with transcription support
- ✦ **Explore Feed** - Browse stories from your community
- ⊕ **Easy Sharing** - Submit your own stories with text and/or audio
- ◉ **User Profile** - Manage your stories and account
- 🔐 **Authentication** - Secure user accounts via Supabase

## Tech Stack

- **Frontend**: React Native with Expo
- **Runtime**: Expo (Web, iOS, Android support)
- **Backend**: Supabase (PostgreSQL database)
- **Location Services**: React Native Maps
- **Audio**: Expo AV
- **UI Framework**: React Navigation (Bottom tabs + Stack navigation)
- **Fonts**: Google Fonts (Outfit, Lora)
- **Language**: JavaScript / React Native

### Key Dependencies

- `expo` - App framework
- `@react-navigation/*` - Navigation system
- `@supabase/supabase-js` - Backend database client
- `react-native-maps` - Map display
- `expo-av` - Audio/Video playback and recording
- `expo-location` - Geolocation
- `react-native-safe-area-context` - Safe area handling

## Installation

### Prerequisites

- Node.js and npm/yarn
- Expo CLI (`npm install -g expo-cli`)
- Supabase account and project

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/Bobydong/voices-around-us-BUILD.git
   cd voices-around-us-BUILD
   ```

2. **Install dependencies**
   ```bash
   cd VoicesAroundUs
   npm install
   # or
   yarn install
   ```

3. **Set up Supabase**
   - Create a new Supabase project at https://supabase.com
   - Run the SQL migration to set up the database schema
   - Apply the transcription migration:
     ```bash
     # Copy the contents of migration-add-transcription.sql
     # Paste into Supabase → SQL Editor → Run
     ```

4. **Configure environment variables**
   - Create a `.env` file in the `VoicesAroundUs` directory
   - Add your Supabase credentials:
     ```
     EXPO_PUBLIC_SUPABASE_URL=your_supabase_url
     EXPO_PUBLIC_SUPABASE_ANON_KEY=your_anon_key
     ```

## Running Locally

### Web
```bash
cd VoicesAroundUs
npm run web
```

### iOS
```bash
cd VoicesAroundUs
npm run ios
```

### Android
```bash
cd VoicesAroundUs
npm run android
```

### Development Server
```bash
cd VoicesAroundUs
npm start
```

Then choose your platform:
- Press `w` for web
- Press `i` for iOS
- Press `a` for Android

## Project Structure

```
VoicesAroundUs/
├── App.js                    # Main app entry point
├── src/
│   ├── navigation/          # Navigation configuration (tabs, stacks)
│   ├── screens/             # Screen components (Map, Explore, Submit, Profile)
│   ├── hooks/               # Custom hooks (useAuth)
│   ├── theme/               # Colors and font definitions
│   └── ...
├── supabase/                # Supabase configuration
└── package.json
```

## Key Screens

- **Map Screen** - View stories on an interactive map
- **Explore Screen** - Browse stories in a feed
- **Submit Screen** - Share a new story with audio/text
- **Profile Screen** - View your profile and manage your stories
- **Auth Screen** - Sign up and log in
- **Story View** - View detailed story information

## Database

The app uses Supabase PostgreSQL database with support for:
- User authentication
- Story storage (text, audio URLs, location)
- Transcription data (transcript_text, transcription_status, transcribed_at)
- Comments and interactions

See `migration-add-transcription.sql` for database schema updates.

## Acknowledgements

- Built for UCLA ACM Hack's HOTH XII hackathon
- Built by the team at Bruin Software Engineers
- Devpost: https://devpost.com/software/voices-around-us?ref_content=my-projects-tab&ref_feature=my_projects
- Thanks to everyone who provided feedback during development
