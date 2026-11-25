DHANVI JYOTHISHALAYA - INITIAL MOBILE WEB APP

WHAT IS INCLUDED
- Telugu / English interface
- Panchangam form: date, place, latitude, longitude
- Approximate tithi, paksha, nakshatra, Moon sign using Astronomy Engine + simplified Lahiri ayanamsa
- Sunrise, sunset, moonrise and moonset via Astronomy Engine rise/set calculations
- Birth details form and an initial Rasi chart prototype with planetary longitudes
- Gemini AI question box through a Netlify Function
- PWA manifest, icon, service worker for installable mobile shortcut
- Netlify configuration

IMPORTANT ACCURACY NOTICE
This is an INITIAL WORKING PROTOTYPE, not a fully validated professional Panchangam or horoscope engine.
- Tithi/nakshatra and planetary positions are computed from Astronomy Engine plus a simplified Lahiri ayanamsa approximation.
- Traditional Telugu lunar month, tithi start/end times, yoga, karana, panchanga rules, Rahu/Ketu, Navamsa, Vimshottari dasha/bhukti, retrograde flags and compatibility are NOT fully implemented.
- Ascendant and house layout are prototype calculations. Validate all chart outputs against a trusted Vedic ephemeris/panchanga before relying on them for rituals or decisions.
- Astronomy Engine is loaded from jsDelivr CDN, so internet is required for calculations. Library reference: https://github.com/cosinekitty/astronomy

DEPLOY TO NETLIFY
1. Extract this ZIP.
2. In Netlify, choose Add new site > Deploy manually and upload the extracted folder contents (index.html must be at the publish root). Or push the extracted files to GitHub and connect the repository.
3. Open Site configuration / Environment variables and add:
   Key: GEMINI_API_KEY
   Value: your Google AI Studio Gemini API key
4. Redeploy after adding the environment variable. Never paste the API key into index.html or share it publicly.
5. Ensure Site access / Visitor access is Public if you want other people to open it without authentication.
6. Open the published HTTPS URL on a phone, then browser menu > Install app / Add to Home Screen.

GEMINI API
- The AI question feature uses model gemini-3.8-flash via Netlify Function.
- API usage is subject to Google's current model availability, free-tier limits and pricing.
- The API key remains on the Netlify server environment; it is not exposed in browser code.

PLACE COORDINATES
- Hyderabad default: latitude 17.385, longitude 78.4867.
- You can use the location button or enter coordinates manually.

FILES
- index.html
- manifest.json
- sw.js
- icon.svg
- netlify.toml
- netlify/functions/ask.mjs
