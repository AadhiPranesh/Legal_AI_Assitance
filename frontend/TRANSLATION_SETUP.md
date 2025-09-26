# Google Translate API Setup Guide

## Step 1: Get Google Cloud API Key

1. **Go to Google Cloud Console**: https://console.cloud.google.com/
2. **Create or Select Project**: 
   - Click on project dropdown at the top
   - Create new project or select existing one
3. **Enable Cloud Translation API**:
   - Go to "APIs & Services" > "Library"
   - Search for "Cloud Translation API"
   - Click on it and press "Enable"
4. **Create API Key**:
   - Go to "APIs & Services" > "Credentials"
   - Click "Create Credentials" > "API Key"
   - Copy the generated API key

## Step 2: Add API Key to Your Project

1. **Open `.env` file** in your project root
2. **Replace `YOUR_API_KEY_HERE`** with your actual API key:
   ```
   REACT_APP_GOOGLE_TRANSLATE_API_KEY=your_actual_api_key_here
   ```

## Step 3: Restart Your Development Server

```bash
npm start
```

## Features of the New Translation System

✅ **Google Translate API**: Uses official Google Cloud Translation API  
✅ **Fallback System**: Falls back to MyMemory API if Google API fails  
✅ **Text Preservation**: Stores original text to restore when switching back to English  
✅ **Batch Translation**: Translates in batches for better performance  
✅ **Loading Indicator**: Shows translation progress  
✅ **Language Persistence**: Remembers selected language in localStorage  
✅ **Smart Element Selection**: Only translates text content, not code or symbols  

## Supported Languages

- English (🇺🇸)
- Hindi (🇮🇳)
- Bengali (🇧🇩)
- Telugu (🇮🇳)
- Tamil (🇮🇳)
- Gujarati (🇮🇳)
- Marathi (🇮🇳)
- Kannada (🇮🇳)
- Malayalam (🇮🇳)
- Punjabi (🇮🇳)
- Odia (🇮🇳)
- Urdu (🇵🇰)

## Cost Information

- **Google Translate API**: $20 per 1 million characters
- **MyMemory API**: Free tier with 10,000 words/day limit
- **Recommendation**: Start with MyMemory API for testing, upgrade to Google API for production

## Alternative: Use Only Free MyMemory API

If you prefer not to use Google API, you can modify the `translateText` function to use only MyMemory API by removing the Google API part and keeping only the fallback code.
