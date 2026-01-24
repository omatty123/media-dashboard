# Media Dashboard

A personal dashboard for tracking shows and movies you're watching.

## Firebase Setup (One-time, ~2 minutes)

### 1. Create Firebase Project
1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Click "Create a project"
3. Name it something like "media-dashboard"
4. Disable Google Analytics (not needed)
5. Click "Create project"

### 2. Create Realtime Database
1. In your project, click "Build" → "Realtime Database"
2. Click "Create Database"
3. Choose your region (any is fine)
4. Select "Start in **test mode**" (allows read/write)
5. Click "Enable"

### 3. Get Your Config
1. Click the gear icon → "Project settings"
2. Scroll down to "Your apps"
3. Click the web icon `</>`
4. Register app (name doesn't matter)
5. Copy the `firebaseConfig` object

### 4. Update the Dashboard
1. Edit `index.html`
2. Find the `firebaseConfig` section near line 357
3. Replace the placeholder values with your config:

```javascript
const firebaseConfig = {
    apiKey: "your-actual-api-key",
    authDomain: "your-project.firebaseapp.com",
    databaseURL: "https://your-project-default-rtdb.firebaseio.com",
    projectId: "your-project",
    storageBucket: "your-project.appspot.com",
    messagingSenderId: "123456789",
    appId: "1:123456789:web:abcdef"
};
```

5. Commit and push to GitHub

### 5. Load Initial Data (Optional)
After Firebase is connected, you can manually add your first items, or:
1. Open Firebase Console → Realtime Database
2. Click "Import JSON"
3. Upload the `data.json` file from this repo

## Done!
Your dashboard will now sync automatically across all devices.
