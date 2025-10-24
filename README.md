#  Astronomical Search Engine

A professional full-stack web application for searching, filtering, and analyzing **2.7+ million real stars** from the ESA Gaia mission astronomical catalog.

[Python](https://img.shields.io/badge/Python-3.11+-blue)
[Flask](https://img.shields.io/badge/Flask-2.3.3-green)
[License](https://img.shields.io/badge/License-MIT-yellow)
[Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen)


##  Features

✨ **Advanced Search Capabilities:**
- Search by star name (Sirius, Vega, Betelgeuse, etc.)
- Filter by brightness (magnitude)
- Filter by distance from Earth (light-years)
- Filter by star type (O, B, A, F, G, K, M)
- Filter by temperature (Kelvin)
- Advanced multi-filter search
- Real-time autocomplete suggestions

📊 **Data & Analytics:**
- 2.7+ million stars from Gaia DR3 catalog
- Real-time database statistics
- Interactive data tables with pagination
- Export search results to CSV
- Detailed star information modals

🎨 **User Interface:**
- Beautiful space-themed design with animated star background
- Responsive mobile-friendly layout
- Modern dark mode interface
- Smooth animations and transitions
- Professional UI/UX

⚡ **Performance:**
- Optimized SQLite database with performance indexes
- Fast search queries even with millions of stars
- Efficient data caching
- Pagination for large result sets

---

## 🛠️ Technology Stack

**Backend:**
- Python 3.11+
- Flask 2.3.3 (Web Framework)
- Flask-CORS 4.0.0 (Cross-Origin Requests)
- SQLite3 (Database)
- Pandas 2.1.1 (Data Processing)
- NumPy 1.24.3 (Numerical Computing)

**Frontend:**
- HTML5
- CSS3 (with animations)
- Vanilla JavaScript (ES6+)

**Data Sources:**
- ESA Gaia Mission DR3 Catalog (2+ million stars)
- Hipparcos Star Catalog (118k stars)
- SIMBAD Astronomical Database (star names)

## 📁 Project Structure

```
astronomical-search-engine/
│
├── web_app.py                    # Main Flask application
├── requirements.txt              
├── Procfile                      
├── runtime.txt                   
│
├── templates/
│   └── index.html               # Main web interface
│
├── static/
│   ├── style.css                # Website styling
│   └── script.js                
│
├── data/
│   ├── combined_gaia_stars.csv  # Gaia data (2 million stars)
│   ├── hipparcos-voidmain.csv   # Hipparcos catalog
│   └── simbad_stars.csv         # SIMBAD star names
│
├── ultimate_star_database.db    #SQLite database
│
└── README.md                   
```

---

## 🔍 Usage Guide

### **Searching by Star Name**
1. Enter star name in the search box (e.g., "Sirius", "Vega", "Betelgeuse")
2. Click Search or press Enter
3. View results in the table below

### **Filtering Stars**
1. Adjust brightness (magnitude) slider (1-20, lower = brighter)
2. Set maximum distance in light-years
3. Select star type (O, B, A, F, G, K, M)
4. Results update automatically

### **Viewing Star Details**
1. Click on any star name in the results table
2. View detailed information in the modal popup
3. See position, brightness, distance, spectral type, and more

### **Exporting Results**
1. Perform a search
2. Click "Export Results" button
3. Download CSV file with all search results

---

##  API Endpoints

### **Search Stars by Name**
```
POST /api/search-by-name
Body: { "name": "Sirius" }
```

### **Advanced Search**
```
POST /api/search
Body: {
  "min_magnitude": 0,
  "max_magnitude": 10,
  "max_distance": 500,
  "star_type": "G",
  "limit": 1000
}
```

### **Get Database Statistics**
```
GET /api/stats
```

### **Get Specific Star**
```
GET /api/star/<star_name>
```

---

##  Data Statistics

- **Total Stars:** 2,744,264
- **Data Source:** ESA Gaia Mission DR3
- **Database Size:** ~450 MB
- **Average Search Time:** <100ms
- **Update Frequency:** Static (can be updated with new data)


##  Educational Value

This project demonstrates:

✅ **Full-Stack Web Development**
- Backend API design with Flask
- Database optimization and indexing
- Frontend UI/UX with modern JavaScript

✅ **Data Science & Analytics**
- Large dataset handling (2.7M+ records)
- Data cleaning and standardization
- Efficient data storage and retrieval

✅ **Software Engineering**
- Professional code structure
- Database normalization
- Performance optimization
- Responsive design

✅ **Astronomy & Science**
- Real astronomical data analysis
- Understanding star properties
- Celestial coordinate systems


##  Database Operations

### **Create Database**
```bash
python create_master_database.py
```

### **Add Star Names**
```bash
python add_common_names.py
```

### **Test Database**
```bash
python test_search.py
```

---
## Troubleshooting

**Issue: Search returns no results**
- Make sure `ultimate_star_database.db` exists
- Check that web_app.py points to correct database
- Restart Flask server and refresh browser (Ctrl+Shift+R)

**Issue: Website loading slowly**
- Large dataset takes time to search
- Use more specific filters to narrow results
- Database indexes speed up searches significantly

**Issue: Port 5000 already in use**
```bash
python web_app.py --port 5001
```

## Future Enhancements

- [ ] Add 3D star map visualization
- [ ] Implement star comparison tool
- [ ] Add exoplanet data integration
- [ ] Create user accounts and save searches
- [ ] Add machine learning for star classification
- [ ] Real-time data updates from Gaia
- [ ] Mobile app version

Author

**Bobby** - Computer Science & Astronomy Enthusiast  
Astronomical Database & Search Engine

License

This project is licensed under the **MIT License** - see LICENSE file for details.

Acknowledgments

- **ESA Gaia Mission** - For providing astronomical data
- **Hipparcos Catalog** - For star position data
- **SIMBAD** - For star names and classifications
- **Flask Community** - For excellent web framework

 Support

For issues, questions, or suggestions:
- Open an Issue on GitHub
- Check existing documentation
- Review API endpoints

Show Your Support
If you found this project helpful, please:
-  Star this repository
-  Fork and contribute
-  Share with others
-  Give feedback

Live Demo: {currently in work}

GitHub: [github.com/Bobby515-code/astronomical-search-engine](https://github.com/Bobby515-code/astronomical-search-engine)
