# Wikimedia Events Browser 🗓️

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3.0-7952b3.svg)](https://getbootstrap.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-f7df1e.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26.svg)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6.svg)](https://developer.mozilla.org/en-US/docs/Web/CSS)

A modern, responsive web application for browsing and discovering Wikimedia community events. Built with cutting-edge web technologies and designed for optimal user experience across all devices.

## ✨ Features

### 🎯 Core Functionality
- **Real-time Event Fetching**: Automatically retrieves events from Wikipedia's special events page
- **Advanced Filtering**: Filter events by country, type, participation options, and search terms
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Live Data**: Events are fetched directly from Wikipedia API with automatic updates

### 🔍 Search & Filter Capabilities
- **Text Search**: Search through event titles and descriptions
- **Geographic Filtering**: Filter by country/location
- **Event Type Categorization**: Conference, Workshop, Meetup, Hackathon, Training, etc.
- **Participation Options**: Online, In-person, Hybrid events
- **Dynamic Filter Updates**: Real-time filtering with live result counts

### 🎨 Modern UI/UX
- **Professional Design**: Clean, modern interface with gradient accents
- **Interactive Elements**: Hover effects, smooth transitions, and animations
- **Accessibility**: WCAG compliant with proper focus states and screen reader support
- **Mobile-First**: Responsive design optimized for touch devices

### 🛡️ Security & Performance
- **Content Security Policy**: Robust CSP implementation
- **Input Sanitization**: XSS protection with proper HTML escaping
- **URL Validation**: Secure external link handling
- **Caching System**: Intelligent caching for improved performance
- **Error Handling**: Graceful error handling with user-friendly messages

## 🚀 Technology Stack

### Frontend
- **HTML5**: Semantic markup with modern standards
- **CSS3**: Custom properties, Grid/Flexbox layouts, advanced animations
- **JavaScript ES6+**: Modern JavaScript with classes, async/await, and modules
- **Bootstrap 5.3.0**: Responsive framework for consistent UI components

### APIs & Data
- **Wikipedia API**: Integration with `sw.wikipedia.org` for event data
- **RESTful Design**: Clean API consumption with proper error handling
- **Data Parsing**: Intelligent parsing of Wikipedia event markup

### Development Tools
- **Modern CSS**: CSS Grid, Flexbox, Custom Properties, Animations
- **ES6+ Features**: Classes, Arrow functions, Template literals, Destructuring
- **Responsive Design**: Mobile-first approach with progressive enhancement

## 📱 Responsive Design

The application is built with a **mobile-first approach** ensuring optimal experience across all devices:

- **Desktop**: Full-featured interface with multi-column layouts
- **Tablet**: Optimized touch interface with adaptive layouts
- **Mobile**: Streamlined mobile experience with touch-friendly controls
- **Cross-browser**: Compatible with all modern browsers

## 🎯 Use Cases

### For Wikimedia Community Members
- Discover upcoming community events and conferences
- Find workshops and training opportunities
- Connect with organizers and participants
- Stay updated on community activities

### For Event Organizers
- Showcase events to the Wikimedia community
- Reach potential participants globally
- Coordinate with other community events

### For Developers & Researchers
- Study Wikimedia community engagement patterns
- Analyze event distribution and participation trends
- Integrate with other Wikimedia tools and platforms

## 🔧 Installation & Setup

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- No server-side requirements (client-side only)

### Quick Start
1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/wikimedia-events-browser.git
   cd wikimedia-events-browser
   ```

2. **Open in browser**
   ```bash
   # Using Python (if available)
   python -m http.server 8000
   
   # Using Node.js (if available)
   npx serve .
   
   # Or simply open index.html in your browser
   ```

3. **Access the application**
   - Navigate to `http://localhost:8000` (if using server)
   - Or open `index.html` directly in your browser

### Development Setup
```bash
# Install development dependencies (if needed)
npm install

# Run development server
npm run dev

# Build for production
npm run build
```

## 📁 Project Structure

```
wikimedia-events-main/
├── index.html          # Main HTML structure and layout
├── script.js           # Core application logic and API integration
├── style.css           # Professional styling and responsive design
├── README.md           # Project documentation
├── .gitignore          # Git ignore patterns
└── style.css.backup    # Backup of original styling
```

### File Descriptions

- **`index.html`** (196 lines): Semantic HTML structure with Bootstrap integration
- **`script.js`** (528 lines): Main application logic, API calls, and event handling
- **`style.css`** (655 lines): Modern CSS with responsive design and animations
- **Total**: 1,379 lines of production-ready code

## 🌐 API Integration

### Wikipedia Events API
The application integrates with Wikipedia's special events page through their public API:

```javascript
// Example API endpoint
const apiUrl = "https://sw.wikipedia.org/w/api.php" +
  "?action=parse&format=json&formatversion=2" +
  "&prop=text&contentmodel=wikitext" +
  "&text={{Special:AllEvents}}&origin=*";
```

### Data Processing
- **Event Parsing**: Intelligent extraction of event details from Wikipedia markup
- **Data Normalization**: Consistent formatting of dates, locations, and metadata
- **Caching**: Smart caching system for improved performance
- **Error Handling**: Graceful fallbacks for API failures

## 🎨 Design System

### Color Palette
- **Primary**: Modern blue (#2563eb) with gradient variations
- **Secondary**: Neutral grays for text and borders
- **Accent**: Warm orange (#f59e0b) for highlights
- **Success**: Green (#10b981) for positive states
- **Warning**: Orange (#f59e0b) for alerts
- **Danger**: Red (#ef4444) for errors

### Typography
- **Font Family**: Inter (with system font fallbacks)
- **Font Weights**: 400 (regular), 500 (medium), 600 (semibold), 700 (bold), 800 (extrabold)
- **Responsive Scaling**: Adaptive font sizes for different screen sizes

### Components
- **Cards**: Elevated event cards with hover effects
- **Buttons**: Gradient buttons with smooth transitions
- **Forms**: Modern form controls with focus states
- **Badges**: Color-coded participation and type indicators

## 📱 Mobile Optimization

### Touch-Friendly Design
- **Minimum Touch Targets**: 44px minimum for interactive elements
- **Gesture Support**: Optimized for touch interactions
- **Responsive Layouts**: Adaptive grid systems for different screen sizes

### Performance
- **Optimized Animations**: Hardware-accelerated CSS transitions
- **Efficient Rendering**: Minimal DOM manipulation
- **Smart Caching**: Intelligent data caching strategies

## 🔒 Security Features

### Content Security Policy
```html
<meta http-equiv="Content-Security-Policy" 
      content="default-src 'self'; 
               connect-src 'self' https://sw.wikipedia.org;
               img-src 'self' https: data:;
               style-src 'self' 'unsafe-inline' https://cdn.jsdelivr.net;
               script-src 'self' https://cdn.jsdelivr.net;
               font-src 'self' https://cdn.jsdelivr.net data:;">
```

### Security Measures
- **XSS Protection**: Input sanitization and HTML escaping
- **URL Validation**: Secure external link handling
- **CSP Implementation**: Strict content security policy
- **Data Validation**: Client-side and server-side validation

## 🚀 Performance Features

### Optimization Strategies
- **Lazy Loading**: Efficient data loading and rendering
- **Smart Caching**: Intelligent cache invalidation
- **Minimal Dependencies**: Lightweight external dependencies
- **Efficient DOM**: Optimized DOM manipulation

### Loading States
- **Skeleton Loading**: Visual feedback during data fetching
- **Progressive Enhancement**: Graceful degradation for slower connections
- **Error Boundaries**: Robust error handling and recovery

## 🧪 Testing & Quality

### Code Quality
- **ES6+ Standards**: Modern JavaScript best practices
- **Semantic HTML**: Accessible and SEO-friendly markup
- **CSS Best Practices**: Modern CSS with proper vendor prefixes
- **Error Handling**: Comprehensive error handling and logging

### Browser Compatibility
- **Modern Browsers**: Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- **Progressive Enhancement**: Core functionality works in older browsers
- **Mobile Browsers**: Optimized for iOS Safari and Chrome Mobile

## 🤝 Contributing

We welcome contributions from the Wikimedia community! Here's how you can help:

### Development
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Areas for Contribution
- **UI/UX Improvements**: Design enhancements and user experience
- **Feature Development**: New functionality and capabilities
- **Performance Optimization**: Speed and efficiency improvements
- **Documentation**: Better documentation and examples
- **Testing**: Bug reports and testing assistance

### Code Standards
- **JavaScript**: ES6+ with modern best practices
- **CSS**: Modern CSS with proper organization
- **HTML**: Semantic markup with accessibility in mind
- **Git**: Clear commit messages and proper branching

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Wikimedia Foundation**: For providing the events data and API
- **Bootstrap Team**: For the excellent responsive framework
- **Font Awesome**: For the comprehensive icon library
- **Open Source Community**: For inspiration and best practices

## 📞 Support & Contact

### Getting Help
- **Issues**: Report bugs and request features via GitHub Issues
- **Discussions**: Join community discussions in GitHub Discussions
- **Documentation**: Check this README and inline code comments

### Community
- **Wikimedia**: [wikimedia.org](https://wikimedia.org)
- **GitHub**: [github.com/yourusername/wikimedia-events-browser](https://github.com/yourusername/wikimedia-events-browser)
- **Contributors**: See the [Contributors](https://github.com/yourusername/wikimedia-events-browser/graphs/contributors) page

---

**Built with ❤️ for the Wikimedia Community**

*This application helps connect Wikimedia community members with events, workshops, and opportunities to collaborate and learn together.*
