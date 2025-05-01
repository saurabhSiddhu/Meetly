# Meetly - Modern Video Conferencing

Meetly is a lightweight, modern video conferencing application built with WebRTC, Socket.IO, and SimplePeer. It provides a clean, Google Meet-like interface with essential video conferencing features.

## Features

- 🎥 Real-time video and audio communication
- 🔄 Camera switching (front/back)
- 🎤 Mute/unmute microphone
- 📹 Enable/disable video
- 📱 Responsive design for all devices
- 🎨 Modern, clean UI inspired by Google Meet
- 🔒 Secure WebRTC connections
- 🌐 Cross-browser compatibility

## Technical Stack

- **Frontend**: HTML5, CSS3, JavaScript
- **WebRTC**: SimplePeer for peer-to-peer connections
- **Signaling**: Socket.IO for real-time communication
- **STUN/TURN**: Metered.ca for NAT traversal
- **Icons**: Material Icons
- **Fonts**: Google Sans

## Architecture

### Components

1. **Video Grid**
   - Responsive grid layout
   - Automatic sizing based on participant count
   - 16:9 aspect ratio maintenance
   - Smooth transitions and animations

2. **Control Panel**
   - Floating control bar
   - Material Design icons
   - Real-time status indicators
   - Touch-friendly interface

3. **Peer Connection**
   - WebRTC peer-to-peer connections
   - Automatic ICE candidate handling
   - Stream management and switching
   - Error handling and recovery

### Data Flow

1. **Connection Setup**
   ```
   Client -> Socket.IO Server -> Peer Discovery -> WebRTC Connection
   ```

2. **Media Stream**
   ```
   Local Device -> MediaStream -> Peer Connection -> Remote Display
   ```

3. **Control Signals**
   ```
   User Action -> State Update -> UI Feedback -> Stream Modification
   ```

## Setup and Installation

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Modern web browser with WebRTC support

### Installation

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/meetly.git
   cd meetly
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Start the server
   ```bash
   npm start
   ```

4. Open in browser
   ```
   https://localhost:3000
   ```

## Configuration

### Environment Variables

```env
PORT=3000
NODE_ENV=development
```

### STUN/TURN Servers

The application uses Metered.ca's free STUN/TURN servers. For production, consider:

1. Setting up your own TURN server
2. Using a paid TURN service
3. Implementing fallback mechanisms

## Usage

### Basic Controls

- **Mute/Unmute**: Click the microphone icon
- **Video Toggle**: Click the camera icon
- **Switch Camera**: Click the flip camera icon

### Keyboard Shortcuts

- `Ctrl/Cmd + D`: Toggle mute
- `Ctrl/Cmd + E`: Toggle video
- `Ctrl/Cmd + C`: Switch camera

## Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge (Chromium-based)

## Performance Considerations

1. **Bandwidth Management**
   - Adaptive bitrate
   - Resolution scaling
   - Network condition monitoring

2. **Resource Usage**
   - Efficient peer connection management
   - Stream cleanup on disconnect
   - Memory leak prevention

3. **Mobile Optimization**
   - Touch-friendly controls
   - Responsive layout
   - Battery efficiency

## Security

1. **Connection Security**
   - HTTPS required
   - Secure WebSocket (WSS)
   - Encrypted media streams

2. **Data Protection**
   - No data storage
   - End-to-end encryption
   - Secure signaling

## Troubleshooting

### Common Issues

1. **Camera/Microphone Access**
   - Check browser permissions
   - Verify device connections
   - Restart browser if needed

2. **Connection Issues**
   - Check network connectivity
   - Verify STUN/TURN server availability
   - Check firewall settings

3. **Performance Problems**
   - Close unnecessary tabs
   - Check system resources
   - Update browser

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

MIT License - See LICENSE file for details

## Acknowledgments

- WebRTC team
- Socket.IO community
- SimplePeer library
- Metered.ca for STUN/TURN servers

## Roadmap

- [ ] Screen sharing
- [ ] Chat functionality
- [ ] Recording capabilities
- [ ] Virtual backgrounds
- [ ] Breakout rooms
- [ ] Meeting scheduling
- [ ] User authentication
- [ ] Meeting analytics
