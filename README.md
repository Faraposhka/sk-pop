# Population Change in Slovakia (1996-2025)

Interactive web map showing population changes at the municipal level in Slovakia over 30 years.

## Features

- **Time Slider**: Slide through years from 1996 to 2025 to see population changes over time
- **Multiple Display Modes**:
  - Population: View absolute population numbers for any year
  - Change from Base Year: See how population changed compared to a base year (1996, 2000, 2010, or 2020)
  - Percent Change: Visualize percentage changes from the base year
  - Change from Previous Year: See year-over-year changes
- **Interactive**: Hover over municipalities to see detailed statistics
- **Color-coded**: Intuitive color schemes showing growth (green) vs decline (red)

## Files

- `index.html` - The main web map interface
- `slovakia_population.geojson` - Geographic data with population statistics (1996-2025)
- `create_webmap.py` - Python script used to generate the GeoJSON from source data
- `INSPIRE_AU.gpkg` - Source geodata (GeoPackage format)
- `v_om7010rr_00_00_00_en20260516213658.csv` - Source demographic statistics

## How to Host on GitHub

### Option 1: GitHub Pages (Recommended)

1. **Create a new GitHub repository**:
   - Go to https://github.com/new
   - Name it something like `slovakia-population-map`
   - Make it public

2. **Upload files**:
   - Upload `index.html` and `slovakia_population.geojson` to the repository
   - You can drag and drop files or use Git commands:
   ```bash
   git init
   git add index.html slovakia_population.geojson README.md
   git commit -m "Initial commit"
   git remote add origin https://github.com/YOUR_USERNAME/slovakia-population-map.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**:
   - Go to repository Settings → Pages
   - Under "Source", select "main" branch
   - Click Save
   - Your map will be available at: `https://YOUR_USERNAME.github.io/slovakia-population-map/`

### Option 2: Direct File Access

You can also open `index.html` directly in your browser for local viewing. However, some browsers may block loading the GeoJSON file due to CORS restrictions. If this happens, use a local web server:

```bash
# Python 3
python -m http.server 8000

# Then visit http://localhost:8000
```

## Data Sources

- **Geographic Data**: INSPIRE Administrative Units (GeoPackage)
- **Population Statistics**: Statistical Office data covering years 1996-2025
- **Level**: Municipal (Obec) - 2,928 municipalities

## Technical Details

- Built with Leaflet.js for mapping
- GeoJSON format for efficient data loading
- Responsive design works on desktop and mobile
- No server-side processing required

## Population Trends

The data shows interesting patterns:
- Total population in 2000: 5,398,657
- Total population in 2025: 5,419,451
- Net change: +20,794 (+0.4%)
- Average municipality population: ~1,850

Many rural municipalities show significant population decline, while urban areas and suburbs show growth.

## License

Data visualization created for educational and analytical purposes.
