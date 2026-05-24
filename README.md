# 🏭 Warehouse Geo‑Mapping Platform (WGMP)
<img width="1536" height="1024" alt="Copilot_20260524_084433" src="https://github.com/user-attachments/assets/5f695d87-9282-476b-a6df-a618feae8cfd" />

A modern, interactive web-based warehouse visualization and inventory management system. This single-page HTML application provides real-time visualization of warehouse storage locations, merchant density analysis, and consolidation management with an intuitive interface for efficient warehouse operations.

## ✨ Features

### 📦 **Storage Map**
- **Hall & Aisle Overview** - Visualize your entire warehouse layout organized by halls and aisles
- **Shelf & Slot Grid** - Detailed view of shelves, levels, and storage columns with real-time occupancy data
- **Heat Map Visualization** - Color-coded occupancy indicator showing box density across locations
- **Interactive Details** - Click any storage location to view detailed inventory information including:
  - Box identifiers and merchant information
  - SKU, description, and quantity details
  - Pickable status and tracking codes
  - Batch numbers and expiry dates
- **Search & Navigation** - Quickly find inventory by:
  - SKU number
  - Merchant name
  - Box ID (with auto-jump to location)
- **Zone Grouping** - Automatic organization of aisles into logical zones (000-099, 100-199, etc.)

### 🔥 **Merchant Density Heatmap**
- **Merchant Distribution** - Analyze merchant concentration across warehouse locations
- **Color-Coded Intensity** - Visual representation of merchant stock levels
- **Per-Merchant Filtering** - Focus on specific merchant inventory distribution
- **Aisle Details** - Break-down of which merchants occupy each aisle and their box counts
- **Comparative Statistics** - View merchant stats including:
  - Total boxes per merchant
  - Aisles occupied
  - Density percentage by location

### 📊 **Consolidation Management**
- **Floor Plan View** - Schematic representation of warehouse layout
- **Merchant Analysis Cards** - Comprehensive metrics for each merchant including:
  - Box counts and location distribution
  - Stock concentration analysis
  - Aisle occupancy breakdown
- **Aisle Purity Analysis** - Understand merchant segregation and identify consolidation opportunities
- **Summary Statistics** - Aggregate warehouse metrics at a glance

## 🎨 Design Features

- **Dark/Light Theme** - Toggle between dark and light modes for comfortable viewing in any environment
- **Responsive Layout** - Optimized for various screen sizes with flexible sidebar navigation
- **Intuitive Navigation** - Breadcrumb navigation for easy location tracking
- **Real-time Tooltips** - Hover over elements for detailed information
- **Accessibility** - Keyboard shortcuts and screen-reader friendly interface
- **Professional Styling** - Modern UI built with CSS variables for easy customization

## 📥 Data Management

### CSV Upload
Upload your warehouse inventory data in CSV format with the following column structure:

| Column | Field | Description |
|--------|-------|-------------|
| A | storage_location | Storage location code (e.g., H1-F1-01-A-001) |
| B | storage_boxes | Box ID/identifier |
| C | merchants | Merchant/vendor name |
| D | skus | SKU number |
| E | sku_description | Product description |
| F | pickable_type | Pickability status (pickable, non_pickable, bulk_pickable) |
| G | tracking_code | Tracking/reference code |
| H | expiry_date | Product expiry date |
| I | quantity | Quantity of units in box |
| J | storage_box_type | Box type/dimensions (optional) |

**Features:**
- Drag & drop file upload or click to browse
- Progress indication during upload
- Error handling with detailed feedback
- Support for up to 184,159+ storage slots
- Real-time data validation

## 🗂️ Application Structure

```
warehouse-visualization-model/
└── index.html          # Complete single-page application
    ├── CSS Styles      # Responsive design with dark/light theme
    ├── HTML Structure  # Semantic markup for all views
    └── JavaScript      # Core logic and interactivity
```

## 🚀 Getting Started

### Quick Start
1. Open `index.html` in a modern web browser
2. Click **"↑ Upload CSV"** in the bottom of the sidebar
3. Upload your warehouse inventory CSV file
4. Navigate between views using the sidebar menu:
   - **🗺 Storage Map** - Explore warehouse layout
   - **🔥 Density Heatmap** - Analyze merchant distribution
   - **📦 Consolidation** - Review consolidation opportunities

### No Installation Required
- Pure HTML/CSS/JavaScript application
- Runs entirely in the browser
- No backend server or dependencies needed
- Data processed client-side for privacy

## 🎮 User Guide

### Storage Map Navigation
1. Select a Hall from the hall tabs in the sidebar
2. Click an Aisle to view its shelf layout
3. Click any storage slot to see detailed inventory
4. Use the search box to find items by SKU, merchant, or box ID
5. Click the "Find Storage Box" feature to jump to a specific box location

### Density Heatmap
1. Select a Hall and merchant from the filters
2. Color intensity represents merchant stock concentration
3. Hover over aisles to see merchant breakdown
4. Click an aisle to see detailed merchant distribution

### Consolidation View
1. Choose between Floor Plan or Merchant Analysis views
2. Review merchant statistics and aisle purity metrics
3. Analyze consolidation opportunities based on merchant distribution
4. Identify zones with mixed vs. pure merchant storage

### Keyboard Shortcuts
- **Enter** in Box Search - Jump to box location
- **Click breadcrumb** - Navigate back to hall overview
- **Theme Toggle** - Switch between dark/light modes

## 📊 Data Statistics

The application displays real-time inventory metrics:
- **Total Boxes** - Number of storage boxes in warehouse
- **Total Units** - Quantity of items across all boxes
- **Total Aisles** - Number of active aisles
- **Merchants** - Number of unique merchants

## 🎨 Customization

### Theme Customization
Modify CSS variables in the `:root` and `[data-theme="dark"]` sections:

```css
:root {
  --bg: #f0f2f7;           /* Background color */
  --accent: #0077cc;       /* Primary accent color */
  --accent2: #e85d04;      /* Secondary accent color */
  /* ... more variables */
}
```

### Color Palette
- Professional blue/orange accent colors
- Green for available/good status
- Red for critical/error states
- Yellow for warnings
- Purple for bulk items

## 🔒 Privacy & Security

- **Client-Side Processing** - All data processing happens in your browser
- **No Data Transmission** - Inventory data stays on your device
- **No External Dependencies** - No API calls or third-party services
- **Local Storage Ready** - Can be extended with local browser storage

## 💻 Browser Compatibility

- Chrome/Chromium 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 📋 Technical Details

### File Size
- Compact single-file deployment (~145 KB)
- Optimized for fast loading and responsiveness

### Performance
- Efficient DOM manipulation
- Optimized rendering for large datasets
- Smooth animations and transitions
- Zero layout shift

### Font Stack
- **Syne** - Display font for headings (800 weight)
- **JetBrains Mono** - Monospace font for data and labels

## 🔄 Workflow Examples

### Example 1: Find a Product
1. Type SKU in the "Search" box (sidebar)
2. Matching locations highlight in aisle overview
3. Click an aisle to view shelf details
4. Click the slot to see full inventory details

### Example 2: Analyze Merchant Distribution
1. Go to "Density Heatmap" tab
2. Select a merchant from the left panel
3. Review color-coded aisle distribution
4. Click aisles to see merchant box counts

### Example 3: Consolidation Planning
1. Go to "Consolidation" tab
2. Click "Merchant Analysis" view
3. Review merchant concentration scores
4. Check "Aisle Purity" metrics for consolidation opportunities

## 🛠️ Features for Operations Teams

- **Real-time Visibility** - Always know where inventory is stored
- **Quick Lookups** - Find boxes in seconds using multiple search criteria
- **Density Analysis** - Optimize storage allocation based on merchant distribution
- **Pick Planning** - Identify consolidation opportunities to reduce pick time
- **Inventory Validation** - Verify storage location data accuracy

## 📝 Future Enhancement Ideas

- Export/Print warehouse reports
- Historical tracking and analytics
- Multi-location support
- Integration with warehouse management systems
- Mobile app version
- Advanced filtering and custom views
- Barcode scanning integration
- Real-time inventory sync

## 📄 License

This project is provided as-is for warehouse management purposes.

## 👤 Author

Created by **prabathSoft**

---

**Need Help?** This application is self-contained in a single HTML file. Simply open it in your browser and start uploading your warehouse data!
