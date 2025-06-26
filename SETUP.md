# ElevenLabs Convai Widget - Setup Guide

## Quick Setup (3 Steps)

### 1. **Copy the Script**
Copy `js/convai-tools.js` to your website.

### 2. **Change One Line**
In `js/convai-tools.js`, change this line:
```javascript
const AGENT_ID = 'agent_01jymq2txxfj8r8tb2rhjg282r';
```
To your actual ElevenLabs agent ID:
```javascript
const AGENT_ID = 'your-agent-id-here';
```

### 3. **Include in Your HTML**
Add this to your HTML `<head>`:
```html
<script src="js/convai-tools.js"></script>
```

## Platform-Specific Instructions

### **Self-Hosted Sites (React, Next.js, etc.)**

#### **React/Next.js**
1. Copy `js/convai-tools.js` to your `public` folder
2. Add to your main layout or `_app.js`:
```html
<script src="/convai-tools.js"></script>
```

#### **Vanilla HTML/CSS/JS**
1. Copy `js/convai-tools.js` to your project
2. Add to your HTML `<head>`:
```html
<script src="js/convai-tools.js"></script>
```

#### **WordPress**
1. Upload `js/convai-tools.js` to your theme folder
2. Add to your theme's `header.php`:
```html
<script src="<?php echo get_template_directory_uri(); ?>/convai-tools.js"></script>
```

### **Website Builders**

#### **Framer**
1. Upload `js/convai-tools.js` to your project assets
2. Add custom code in your project settings:
```html
<script src="/convai-tools.js"></script>
```

#### **Wix**
1. Go to Settings → Custom Code
2. Add this in the `<head>` section:
```html
<script src="https://your-wixsite.com/convai-tools.js"></script>
```

#### **Squarespace**
1. Go to Settings → Advanced → Code Injection
2. Add this in the Header section:
```html
<script src="/convai-tools.js"></script>
```

#### **Webflow**
1. Go to Project Settings → Custom Code
2. Add this in the `<head>` section:
```html
<script src="/convai-tools.js"></script>
```

#### **Shopify**
1. Go to Online Store → Themes → Edit Code
2. Add to `theme.liquid` in the `<head>`:
```html
<script src="{{ 'convai-tools.js' | asset_url }}"></script>
```

## Optional Customization

You can also customize these settings in the same file:

```javascript
// Navigation: true = new tab, false = same tab
const OPEN_IN_NEW_TAB = true;

// Widget position
const WIDGET_POSITION = 'bottom-right'; // 'bottom-right', 'bottom-left', 'top-right', 'top-left'

// Base URL (only needed if auto-detection fails)
const BASE_URL = ''; // e.g., 'https://mysite.framer.app'
```

## Troubleshooting

### **Widget Not Appearing**
- Check browser console for errors
- Ensure script is loaded before closing `</body>` tag
- Verify agent ID is correct

### **Navigation Not Working**
- Check if popup blockers are enabled
- Try setting `OPEN_IN_NEW_TAB = false`
- Verify your agent has the `redirectToExternalURL` tool configured

### **Wrong Base URL**
- Set `BASE_URL` manually if auto-detection fails
- Check your site's actual URL structure

## Voice Commands

Your agent can use these commands:
- "Show me pricing" → `/pricing.html`
- "Book a demo" → `/booking.html`
- "Go home" → `/index.html`

## That's It!

The widget will automatically:
- ✅ Load the ElevenLabs script
- ✅ Create the widget in the specified position
- ✅ Handle voice navigation between pages
- ✅ Work on any platform (Framer, Wix, React, etc.)

Just make sure your ElevenLabs agent has the `redirectToExternalURL` tool configured! 