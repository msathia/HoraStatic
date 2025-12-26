# 🕉️ Hora Calculator - Static Edition

A **100% client-side** Vedic Planetary Hours (Hora) calculator that runs entirely in your browser. No backend required!

## 🌟 Features

- **Pure JavaScript** - All hora calculations done locally in browser
- **No API Calls** - Works offline after initial load
- **Multiple Locations** - 17+ cities worldwide (US, India, UK, Singapore, Australia)
- **Accurate Calculations** - Uses astronomical formulas for sunrise/sunset
- **Beautiful UI** - Modern, responsive design with dark theme
- **Real-time Updates** - Auto-refreshes every minute
- **Jupiter Hora Highlights** - Easily find the most auspicious times

## 🚀 Live Demo

Visit: **https://msathia.github.io/HoraStatic/**

## 🏠 Host It Yourself

### Option 1: GitHub Pages (Free)

1. Fork this repository
2. Go to Settings → Pages
3. Select "main" branch and save
4. Your site will be live at `https://yourusername.github.io/HoraStatic/`

### Option 2: Any Static Hosting

Just upload `index.html` to:
- Netlify
- Vercel
- Cloudflare Pages
- Any web server

## 📖 How Hora Works

The Vedic hora system divides each day into 24 planetary hours:
- **12 Day Horas** - From sunrise to sunset
- **12 Night Horas** - From sunset to next sunrise

Each hora is ruled by one of the seven classical planets:
- ☀️ Sun, 🌙 Moon, ♂️ Mars, ☿ Mercury, ♃ Jupiter, ♀️ Venus, ♄ Saturn

### Planet Qualities

| Planet | Emoji | Nature | Recommendation |
|--------|-------|--------|----------------|
| Jupiter | ♃ | Fruitful | ✅ Most Auspicious |
| Venus | ♀️ | Beneficial | ✅ Good |
| Mercury | ☿ | Quick | ✅ Good |
| Moon | 🌙 | Gentle | ✅ Good |
| Sun | ☀️ | Vigorous | 🔸 Neutral |
| Mars | ♂️ | Aggressive | ⚠️ Avoid |
| Saturn | ♄ | Sluggish | ⚠️ Avoid |

## 🔧 Technical Details

### Sunrise/Sunset Calculation

Uses the standard astronomical formula based on:
- Geographic latitude and longitude
- Day of year
- Solar declination angle

The calculation is an approximation (typically within a few minutes of actual times).

### Hora Sequence

The first hora of each day is ruled by the day's lord:
- Sunday → Sun
- Monday → Moon
- Tuesday → Mars
- Wednesday → Mercury
- Thursday → Jupiter
- Friday → Venus
- Saturday → Saturn

Subsequent horas follow the Chaldean order: Saturn → Jupiter → Mars → Sun → Venus → Mercury → Moon (repeat)

## 📍 Supported Locations

### USA
- Austin, TX
- Houston, TX
- Dallas, TX
- San Antonio, TX
- New York, NY
- Los Angeles, CA
- Chicago, IL
- San Francisco, CA

### India
- Chennai
- Mumbai
- Bangalore
- Delhi
- Hyderabad
- Kolkata

### Other
- London, UK
- Singapore
- Sydney, Australia

## 🤝 Contributing

Want to add more cities? Edit the `LOCATIONS` object in `index.html`:

```javascript
new_city: { 
    name: "City Name, Country", 
    lat: 12.3456,      // Latitude
    lng: -78.9012,     // Longitude
    tz: "Timezone/Name" // IANA timezone
}
```

## 📜 License

MIT License - Use freely!

## 🙏 Credits

Inspired by [Drik Panchang](https://www.drikpanchang.com/) for the hora reference data.

---

**Note**: This is a static calculator using astronomical formulas. For religious/spiritual purposes, consult your local pandit or the original Drik Panchang website for exact times based on precise location-specific calculations.

