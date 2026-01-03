# 100 Day Challenge Tracker

A simple, elegant web app for tracking daily progress on any challenge—reading, exercise, skincare, or anything else you want to build into a habit.

**Live:** [dalepike.github.io/100-day-challenge](https://dalepike.github.io/100-day-challenge)

## Features

- **Universal challenges** - Name your own challenge (reading, exercise, meditation, etc.)
- **Variable duration** - Set any number of days (default 100)
- **Daily check-in** - Quick, focused view for marking today complete
- **Full progress view** - See all days organized by month
- **Date tracking** - Each day shows its calendar date based on your start date
- **Export to PNG** - Share your progress as an image
- **Offline-capable** - Works without internet after first load
- **Privacy-first** - All data stays in your browser (localStorage)

## How to Use

1. Visit the site and enter your name, challenge name, number of days, and start date
2. Each day, open the app and tap the circle to mark the day complete
3. View your full progress anytime to see your journey
4. Export and share your progress image with friends and family

## Privacy

Your data never leaves your device. Everything is stored locally in your browser using localStorage. There are no accounts, no servers, no tracking.

## Development

This is a single HTML file with embedded CSS and JavaScript. No build tools required.

To run locally:
```bash
# Just open the file in a browser
open index.html

# Or use a simple server
python -m http.server 8000
```

## License

MIT
