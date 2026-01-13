# Cache Configuration Guide

## Overview
This website uses browser caching to improve performance and reduce server load. Static assets (images, CSS, JavaScript) are cached for **72 hours** before expiring.

## Configuration Files

### `.htaccess`
The main configuration file that handles caching rules. This file is located in the root directory and automatically applies caching rules to all files.

## Cache Settings

### Images (72 hours)
- `.jpg`, `.jpeg`, `.png`, `.gif`, `.webp`, `.svg`, `.ico`
- Cache Duration: 72 hours (259,200 seconds)
- Cache Type: Public, Immutable

### CSS & JavaScript (72 hours)
- `.css`, `.js`
- Cache Duration: 72 hours (259,200 seconds)
- Cache Type: Public, Immutable

### Fonts (72 hours)
- `.ttf`, `.otf`, `.woff`, `.woff2`, `.eot`
- Cache Duration: 72 hours (259,200 seconds)
- Cache Type: Public, Immutable

### HTML Files (1 hour)
- `.html`, `.htm`
- Cache Duration: 1 hour (3,600 seconds)
- Cache Type: Public
- *Note: HTML files have shorter cache time to allow for content updates*

## How It Works

1. **First Visit**: Browser downloads all files from the server
2. **Subsequent Visits**: Browser uses cached files (if within 72 hours)
3. **After 72 Hours**: Browser checks for updated files and re-downloads if changed

## Testing Cache

### Check if caching is working:
1. Open browser Developer Tools (F12)
2. Go to Network tab
3. Reload the page
4. Check the "Size" column:
   - `(disk cache)` or `(memory cache)` = Cached file
   - File size in KB/MB = Downloaded from server

### Clear Cache (for testing):
- **Chrome/Edge**: Ctrl+Shift+Delete → Clear cached images and files
- **Firefox**: Ctrl+Shift+Delete → Cached Web Content
- **Safari**: Cmd+Option+E (Mac) or Ctrl+Shift+Delete (Windows)

## Server Requirements

This configuration requires Apache server with the following modules enabled:
- `mod_expires` - For Expires headers
- `mod_headers` - For Cache-Control headers
- `mod_deflate` - For compression (optional but recommended)
- `mod_rewrite` - For URL rewriting (if needed)

## Troubleshooting

### Cache not working?
1. Verify `.htaccess` file is in the root directory
2. Check if Apache modules are enabled (contact hosting provider)
3. Ensure file permissions allow Apache to read `.htaccess`
4. Check server error logs for any `.htaccess` syntax errors

### Need to update files immediately?
- Change the file name (e.g., `styles.css` → `styles-v2.css`)
- Or clear browser cache manually
- Or reduce cache time temporarily in `.htaccess`

## Notes

- **72 hours** = 259,200 seconds
- Cache headers work automatically - no code changes needed
- Images and static files are cached aggressively for better performance
- HTML files have shorter cache time to allow content updates
- Compression is enabled to reduce file sizes and improve load times
