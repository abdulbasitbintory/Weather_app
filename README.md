# 🌤️ Weather App  
*A modern, responsive weather application built with HTML, CSS, and JavaScript*

## 📌 Overview  
This project is a fully responsive weather application that fetches real-time weather data using a third-party API (e.g., OpenWeatherMap). It features a sleek, gradient-themed UI with animated interactions, dynamic DOM updates, and mobile-first design principles. Users can search for cities, view temperature, humidity, wind speed, and weather icons, and receive error handling for invalid inputs.

---

## 🧩 Key Features  

### 🌐 Core Functionality  
- **Real-Time Weather Data**: Fetches current weather conditions (temperature, humidity, wind speed, etc.) for any city.  
- **Search Autocomplete**: Instant city suggestions as the user types (requires API integration).  
- **Dynamic UI Updates**: Temperature units (°C/°F) toggle, weather icon changes based on conditions (sun, rain, clouds, etc.).  

### 🎨 UI/UX Enhancements  
- **Responsive Design**: Optimized for screens from 320px (mobile) to 1440px (desktop).  
- **Animated Interactions**: Hover effects on buttons, smooth transitions between states.  
- **Error Handling**: Displays user-friendly error messages for invalid inputs or failed API calls.  

### ⚙️ Technical Highlights  
- **Mobile-First Approach**: Built with flexible layouts using Flexbox and CSS Grid.  
- **Modular JavaScript**: Clean separation of concerns (DOM manipulation, API logic, event handling).  
- **Progressive Enhancement**: Graceful degradation for older browsers.  

---

## 🛠️ Tech Stack  
| Technology | Purpose |  
|----------|---------|  
| **HTML5** | Semantic structure, forms, and accessibility |  
| **CSS3** | Responsive layout, animations, and gradient themes |  
| **JavaScript (ES6+)** | Dynamic DOM updates, API integration, event handling |  
| **Weather API** | Example: [OpenWeatherMap](https://openweathermap.org/api) (API key required) |  
| **Git/GitHub** | Version control and collaboration |  

---

## 📁 Project Structure  
```
weather-app/
├── index.html          # Main HTML structure  
├── style.css           # Responsive styles and animations  
├── script.js           # JavaScript logic (API calls, DOM updates)  
├── assets/             # Images, icons, and fonts  
│   └── icons/          # Weather condition icons  
├── README.md           # This documentation  
└── LICENSE             # MIT License  
```

---

## 🚀 Installation & Setup  

### Prerequisites  
- A modern web browser (Chrome, Firefox, Safari, Edge)  
- Basic knowledge of HTML/CSS/JavaScript  
- [Optional] Node.js/npm for local development server  

### Steps  
1. **Clone the Repository**  
```bash
git clone https://github.com/abdulbasitbintory/Weather_app.git
cd Weather_app
```

2. **Install Dependencies**  
If using a local server (e.g., for hot-reloading):  
```bash
npm install -g http-server  # Install HTTP server globally
http-server                 # Start the server
```

3. **API Integration**  
- Sign up for a free API like [OpenWeatherMap](https://openweathermap.org/api).  
- Replace the placeholder API key in `script.js`:  
```javascript
const API_KEY = 'YOUR_OPENWEATHERMAP_API_KEY'; // Replace this
```

4. **Run the App**  
Open `index.html` in your browser or visit `http://localhost:8080` if using a local server.

---

## 🧪 Usage Guide  

### 🔍 Search for a City  
1. Enter a city name (e.g., "London") in the search bar.  
2. Press **Enter** or click the search icon.  
3. The app displays:  
   - Current temperature (°C/°F toggle)  
   - Weather description (e.g., "Clear sky")  
   - Humidity percentage  
   - Wind speed  

### ❌ Error Handling  
- If the city is invalid or the API fails:  
  - An error message appears ("City not found").  
  - The input field resets for retry.  

---

## 🧠 How It Works  

### 1. **HTML Structure**  
- `index.html` contains:  
  - A search form (`input` + `button`)  
  - A `.weather` div to display results  
  - Error message container  

### 2. **CSS Styling**  
- Responsive design using media queries (see `style.css`).  
- Gradient background: `linear-gradient(135deg, #00feba, #5b548a)`.  
- Mobile-first approach with breakpoints at `480px` and `350px`.  

### 3. **JavaScript Logic**  
- **Event Listeners**:  
  ```javascript
  document.querySelector('.search button').addEventListener('click', () => {
    const city = document.querySelector('.search input').value;
    getWeather(city);
  });
  ```
- **API Call**:  
  ```javascript
  async function getWeather(city) {
    try {
      const response = await fetch(`https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${API_KEY}&units=metric`);
      const data = await response.json();
      showWeather(data);
    } catch (error) {
      showError();
    }
  }
  ```

---

## 🌍 Browser Compatibility  
- ✅ Chrome (latest)  
- ✅ Firefox (latest)  
- ✅ Safari (iOS 12+)  
- ✅ Edge (Chromium-based)  

---

## 📈 Future Enhancements  
- [ ] Add a 5-day weather forecast  
- [ ] Geolocation support (auto-detect user location)  
- [ ] Dark/light mode toggle  
- [ ] Unit tests with Jest  
- [ ] PWA (Progressive Web App) support  

---

## 💡 Contributing  
Contributions are welcome! Follow these steps:  
1. Fork the repository  
2. Create a feature branch (`git checkout -b feature-name`)  
3. Commit your changes (`git commit -m 'Add feature'`)  
4. Push to the branch (`git push origin feature-name`)  
5. Submit a pull request  

---

## 📄 License  
This project is licensed under the [MIT License](LICENSE).  

---

## 📬 Contact  
Abdul Basit Bin Tariq  
📧 Email: abdulbasit@example.com  
🌐 GitHub: [github.com/abdulbasitbintory](https://github.com/abdulbasitbintory)  

---

## 🙌 Acknowledgments  
- [OpenWeatherMap API](https://openweathermap.org/api)  
- [W3C HTML/CSS Validation Tools](https://validator.w3.org/)  
- [Google Fonts (Poppins)](https://fonts.google.com/specimen/Poppins)  


