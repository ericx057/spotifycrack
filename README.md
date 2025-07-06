# Spotify Playlist Downloader

A Python tool to download Spotify playlists as MP3 files. The program extracts playlist metadata from Spotify and downloads the audio from YouTube, then packages everything into a convenient zip file.
README written by ChatGPT

**Note: For personal use only - not for commercial purposes**

## Setup Instructions

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Get Spotify API Credentials
1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Click "Create App"
3. Fill in app name and description
4. Copy your **Client ID** and **Client Secret**

### 3. Run the Program
```bash
python main.py
```

On first run, you'll be prompted to enter your Spotify credentials. They'll be saved in a `.env` file for future use.

## How to Use

1. Run `python main.py`
2. Enter your Spotify playlist URL when prompted
   - Example: `https://open.spotify.com/playlist/37i9dQZF1DXcBWIGoYBM5M`
3. The program will:
   - Fetch all tracks from the playlist
   - Search for each track on YouTube
   - Download as MP3 (192kbps quality)
   - Create a zip file with all tracks

## Features

- Downloads entire playlists automatically
- Converts to MP3 format locally
- Creates organized zip files
- Handles special characters in filenames
- Shows download progress
- Error handling for failed downloads

## Requirements

- Python 3.7+
- Active internet connection
- Spotify Developer account (free)

## Technical Details

The program uses:
- **Spotipy** for Spotify API access
- **yt-dlp** for YouTube audio downloading
- **FFmpeg** (auto-installed by yt-dlp) for audio conversion

## Troubleshooting

1. **"Package requirements not satisfied"**: Run `pip install -r requirements.txt`
2. **"Invalid Spotify playlist URL"**: Make sure you're using a public playlist URL
3. **Download failures**: Some tracks might not be available on YouTube
4. **Audio quality**: Default is 192kbps MP3, modify `audioquality` in code if needed
