# 🕉️ பஞ்சாங்கம் - Panchangam

A **100% client-side** Vedic Panchangam (Hindu Calendar) and Hora calculator that runs entirely in your browser. No backend required!

## 🌟 Features

- **Pure JavaScript** - All calculations done locally in browser
- **No API Calls** - Works offline after initial load
- **Multiple Locations** - 17+ cities worldwide (US, India, UK, Singapore, Australia)
- **Accurate Calculations** - Uses astronomical formulas with lunar/solar orbital mechanics
- **Beautiful UI** - Modern, responsive design with dark theme
- **Real-time Updates** - Auto-refreshes every minute
- **Tamil & English** - Bilingual display for all elements

### Panchangam Elements
- **Tithi** - Lunar day with end times
- **Nakshatra** - Lunar mansion with end times
- **Yoga** - Sun-Moon combination
- **Karana** - Half of Tithi
- **Vara** - Day of week
- **Tamil Date** - Solar calendar date
- **Rahu Kalam** - Inauspicious time period

### Additional Features
- **Hora Calculator** - 24 planetary hours with auspiciousness indicators
- **Lagna (Ascendant)** - Rising sign schedule throughout the day
- **Jathaga Kattam** - South Indian style birth chart with planetary positions
- **Sankalpam** - Traditional prayer invocation text
- **Jupiter Hora Highlights** - Easily find the most auspicious times

## 🚀 Live Demo

Visit: **https://msathia.github.io/Panchangam/**

## 🏠 Host It Yourself

### Option 1: GitHub Pages (Free)

1. Fork this repository
2. Go to Settings → Pages
3. Select "main" branch and save
4. Your site will be live at `https://yourusername.github.io/Panchangam/`

### Option 2: Any Static Hosting

Just upload `index.html` to:
- Netlify
- Vercel
- Cloudflare Pages
- Any web server

## 📖 How It Works

### Panchangam Calculations

The app calculates traditional Hindu calendar elements using:
- **Tithi**: Angular distance between Moon and Sun (each tithi = 12°)
- **Nakshatra**: Moon's position in the 27 lunar mansions (each = 13.33°)
- **Yoga**: Sum of Sun and Moon longitudes (27 yogas, each = 13.33°)
- **Karana**: Half of a tithi (60 karanas in a lunar month)

### Hora System

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

### Astronomical Calculations

- **Sunrise/Sunset**: Astronomy Engine `SearchRiseSet` with atmospheric refraction when available; built-in formula fallback
- **Moon Position**: Lunar theory with equation of center, evection, variation, and annual equation
- **Sun Position**: Solar theory with equation of center
- **Ayanamsa**: Lahiri ayanamsa for sidereal (Vedic) coordinates
- **Astronomy Engine**: Uses pinned [astronomy-engine](https://github.com/cosinekitty/astronomy) `2.1.19` from jsDelivr for precise ephemeris when available
- **Timezone Handling**: Converts each selected city's local date/time to UTC before ephemeris calls

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

Inspired by [Drik Panchang](https://www.drikpanchang.com/) for reference data and validation.

---

**Note**: This is a static calculator using astronomical formulas. For religious/spiritual purposes, consult your local pandit or the original Drik Panchang website for exact times based on precise location-specific calculations.
