# Chat Widget Extensions Demo
This repository contains a demonstration of various chat widget extensions for Voiceflow. The extensions include functionality for video playback, timers, forms, maps, file uploads, date selection, confetti effects, and feedback collection.

## Video
https://youtu.be/xY0vNkzFzAI

## Overview
The demo showcases how to extend the capabilities of a chat widget by integrating custom UI elements and interactions. These extensions are designed to be used with the Voiceflow chat widget, which can be embedded into any webpage.

## Extensions
The extensions.js file contains the following extensions:

**VideoExtension**: Embeds a video player into the chat.
**TimerExtension**: Creates a countdown timer.
**FormExtension**: Generates a form for user input.
**MapExtension**: Displays a Google Map.
**FileUploadExtension**: Allows users to upload a file.
**KBUploadExtension**: Upload a doc to a knowledge base.
**DateExtension**: Provides a date and time picker.
**ConfettiExtension**: Triggers a confetti animation.
**FeedbackExtension**: Collects user feedback with thumbs up/down.

Each extension defines how it matches certain chat interactions and how it should render or trigger effects within the chat interface.

## Usage
To use these extensions, you need to include the **extensions.js** file (or **your own file/URL**) in your project and import the extensions into your HTML file where the Voiceflow chat widget is initialized.

The **index.html** file is an example of how to set up the chat widget with the provided extensions. It includes a confetti-canvas for the confetti effect and initializes the Voiceflow chat widget with the extensions.

## Initialization
The chat widget is initialized with the following configuration:
```javascript
window.voiceflow.chat.load({
  verify: { projectID: 'your project id' },
  url: 'https://general-runtime.voiceflow.com',
  versionID: 'development', // or 'production'
  user: {
    name: 'Demo User',
  },
  render: {
    mode: 'overlay',
  },
  autostart: false,
  allowDangerousHTML: true,
  assistant: {
    extensions: [
      VideoExtension,
      TimerExtension,
      FormExtension,
      MapExtension,
      FileUploadExtension,
      KBUploadExtension,
      DateExtension,
      ConfettiExtension,
      FeedbackExtension,
    ],
  },
});
```

## Development
This example page is intended for development purposes only. To integrate the chat widget and extensions into your own project, you'll need to customize the code to fit your specific requirements and ensure that it aligns with your application's architecture and design.

### Dependencies
The Voiceflow project to test with this demo is available in this repo.

The demo uses the canvas-confetti library to create the confetti effect. Make sure to include it in your project if you intend to use the ConfettiExtension.
``` html
<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>
```

### Note
Remember to replace the projectID and versionID. Additionally, ensure that you have the necessary permissions and API keys for services like Google Maps if you're using the MapExtension.

