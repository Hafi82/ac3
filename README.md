# Excellence Graphics - Account Management System

A modern, full-featured customer account management system built for Excellence Graphics with a beautiful glassmorphic UI.

## Features

✨ **Customer Management**
- Add, edit, view, and delete customers
- Automatic profile creation on save
- Customer search functionality
- Payment status tracking (Full/Partial/None)

🎨 **Modern UI/UX**
- Glassmorphic design with smooth animations
- Responsive layout for all devices
- Dark theme with vibrant gradients
- Intuitive navigation and controls

💾 **Data Persistence**
- LocalStorage integration for offline use
- Automatic data saving
- No backend required for basic functionality

## Tech Stack

- **Frontend**: React 18 + Vite
- **Styling**: Vanilla CSS with custom design system
- **Fonts**: Google Fonts (Inter, Outfit)
- **Icons**: Inline SVG icons

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd Ac3
```

2. Install dependencies:
```bash
npm install
```

3. Run the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5173`

## Building for Production

```bash
npm run build
```

The build output will be in the `dist` folder.

## Deployment

### Deploy to Netlify

1. **Push to GitHub**:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin <your-github-repo-url>
git push -u origin main
```

2. **Connect to Netlify**:
   - Go to [Netlify](https://netlify.com)
   - Click "Add new site" → "Import an existing project"
   - Connect your GitHub repository
   - Build settings:
     - Build command: `npm run build`
     - Publish directory: `dist`
   - Click "Deploy site"

### Alternative: Deploy to Vercel

1. Install Vercel CLI:
```bash
npm install -g vercel
```

2. Deploy:
```bash
vercel
```

## Project Structure

```
Ac3/
├── src/
│   ├── components/
│   │   ├── Navigation.jsx       # Top navigation bar
│   │   ├── Navigation.css
│   │   ├── CustomerList.jsx     # Customer list with filters
│   │   ├── CustomerList.css
│   │   ├── CustomerCard.jsx     # Individual customer card
│   │   ├── CustomerCard.css
│   │   ├── CustomerForm.jsx     # Add/Edit customer form
│   │   └── CustomerForm.css
│   ├── App.jsx                  # Main application component
│   ├── App.css
│   ├── main.jsx                 # React entry point
│   └── index.css                # Global styles & design system
├── index.html
├── package.json
├── vite.config.js
└── README.md
```

## Features in Detail

### Customer Management
- **Add Customer**: Click the "Add Customer" button to open a form
- **Edit Customer**: Click the edit icon on any customer card
- **View Customer**: Click the view icon to see full customer details
- **Delete Customer**: Click the delete icon (with confirmation)

### Payment Filters
- **All**: Show all customers
- **Full Payment**: Show only customers with full payment
- **Partial Payment**: Show only customers with partial payment
- **No Payment**: Show only customers with no payment

### Search
- Search customers by name or address in real-time

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

MIT License - feel free to use this project for your business needs.

## Support

For issues or questions, please create an issue in the GitHub repository.

---

**Excellence Graphics** - Account Management System v1.0
