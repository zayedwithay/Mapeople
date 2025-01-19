# Mapbox Project for Internship

This project demonstrates the integration of **Mapbox** with React for building an interactive map application. It includes key features such as displaying markers and fetching location data dynamically. Below is a breakdown of what was implemented.
PREVIEW:

## Features Implemented

### 1. **Map Integration**
- Used **Mapbox GL JS** for rendering the map.
- Integrated the `react-map-gl` library for seamless integration with React.
- Configured the map to display using the **Light** style from Mapbox (`mapbox://styles/mapbox/light-v10`).

### 2. **Dynamic Marker Display**
- Fetched data dynamically from the `/pins` endpoint using **Axios**.
- Placed markers on the map using the longitude and latitude values from the fetched data.
- Used the `@mui/icons-material` library for custom marker icons (e.g., the **Room** icon).

### 3. **State Management**
- Utilized React's `useState` for managing map viewport and marker data.
- Initialized the map's viewport with latitude, longitude, and zoom.

### 4. **API Integration**
- Made an API call to `/pins` to fetch marker data.
- Ensured error handling with fallback mechanisms in case of invalid or empty API responses.
- Logged API responses for debugging purposes.

### 5. **Responsive and Full-Screen Map**
- Styled the map to take up the full width and height of the viewport (`100vw` x `100vh`).

## Requirements Fulfilled
- **Mapbox Token Configuration**:
  - Used `VITE_MAPBOX_TOKEN` from a `.env` file for secure integration of the Mapbox API key.
- **Dynamic Data Rendering**:
  - Fetched and displayed pins dynamically using an API call.
- **Custom Markers**:
  - Used the `Room` icon to represent locations on the map.
- **Zoom Sensitivity**:
  - Marker sizes scale dynamically with the zoom level (`fontSize: viewport.zoom * 8`).
- **Error Handling**:
  - Gracefully handled errors during API calls by providing fallback states.

## Project Structure
```
/src
  |-- App.jsx         # Main React component for the app
  |-- App.css         # Styling for the application
  |-- .env            # Environment variables for API keys
```

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-url.git
   ```
2. Navigate to the project folder:
   ```bash
   cd mapbox-project
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Create a `.env` file in the root directory and add your Mapbox token:
   ```env
   VITE_MAPBOX_TOKEN=your_mapbox_access_token
   ```
5. Start the development server:
   ```bash
   npm run dev
   ```
6. Open the app in your browser:
   ```
http://localhost:5173
```

## API Endpoint
- **Endpoint**: `/pins`
- **Expected Response Format**:
  ```json
  [
    { "lat": 19.076, "long": 72.8777 },
    { "lat": 28.7041, "long": 77.1025 }
  ]
  ```

## Libraries Used
- [React Map GL](https://visgl.github.io/react-map-gl/)
- [Mapbox GL JS](https://docs.mapbox.com/mapbox-gl-js/overview/)
- [Axios](https://axios-http.com/)
- [MUI Icons](https://mui.com/material-ui/material-icons/)

## Future Improvements
- Add popups to display more details about each marker.
- Include filtering options for pins based on categories.
- Implement marker clustering for better visualization.

---
This project demonstrates my ability to work with modern web technologies, integrate APIs, and build responsive user interfaces as required for the internship. Let me know if additional features or improvements are needed!
