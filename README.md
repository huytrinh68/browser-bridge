# Browser Bridge

A simple web page that redirects users from in-app browsers (Messenger, Telegram, WhatsApp, etc.) to their device's default browser.

## Features

- **Auto-detect platform**: Automatically detects Android, iOS, or Desktop
- **Smart redirect**: Uses Intent URLs (Android) and URL schemes (iOS) to open external browser
- **Fallback support**: Shows manual link if auto-redirect fails
- **Loading UI**: Clean loading animation while redirecting

## Usage

### Basic Setup

1. Clone this repository
2. Edit `index.html` and change the `targetUrl` variable to your desired URL
3. Deploy to your web server

### Example

```javascript
const targetUrl = 'https://your-target-url.com';
```

### Deploy

Simply upload `index.html` to your web server and access it via your domain.

## How It Works

### Android
- Uses Intent URL with Chrome package: `intent://...#Intent;scheme=https;package=com.android.chrome;end`
- Falls back to direct URL if Chrome is not installed

### iOS
- Uses Chrome URL scheme: `googlechromes://...`
- Falls back to direct URL if Chrome is not installed

### Desktop
- Direct redirect to target URL

## Live Demo

https://cts.io.vn/open-app

## Configuration

Edit the `targetUrl` variable in `index.html`:

```javascript
const targetUrl = 'https://your-website.com';
```

## License

MIT
