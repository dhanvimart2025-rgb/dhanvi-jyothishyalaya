DHANVI JYOTHISHYALAYA — COMPLETE EDITION (TELUGU + ENGLISH)

Selected configuration
- Complete Panchangam and birth-chart sections
- Lahiri ayanamsa setting (the current implementation is an approximation)
- Telugu / English language toggle
- Netlify hosting and Gemini question-answer function

WHAT THIS BUILD ADDS
PANCHANGAM
- Date and location inputs with coordinates
- Weekday, paksha, tithi, nakshatra, yoga, karana, Moon sign
- Estimated Telugu lunar month and 60-year samvatsara indication
- Approximate tithi, nakshatra and yoga end-time search
- Sunrise, sunset, moonrise, moonset
- Rahu Kalam, Yamagandam and Gulika Kalam based on sunrise-to-sunset division

BIRTH CHART
- Name, date, time, place, latitude and longitude
- Ascendant, Moon sign, birth nakshatra and pada
- Nine grahas including approximate Rahu and Ketu (mean lunar node)
- South Indian Rasi chart and planetary sidereal-longitude table
- Navamsa (D9) placements
- Indicative Vimshottari Mahadasha timeline

AI QUESTION SERVICE
- Existing Netlify Function retained at /.netlify/functions/ask
- Uses GEMINI_API_KEY from Netlify environment variables
- Key must never be placed in index.html or committed to GitHub

IMPORTANT ACCURACY LIMITATIONS
This is an enhanced prototype, NOT a validated professional Jyotish/Panchanga engine.
- Astronomy Engine provides astronomical positions; Lahiri ayanamsa is currently approximated with a simple formula, not a complete Swiss Ephemeris implementation.
- Telugu lunar month and samvatsara labels are indicative estimates; regional amanta/purnimanta conventions and Ugadi boundaries can differ.
- Tithi/nakshatra/yoga boundary times are numerical estimates. Karana end-time, exact traditional observance rules, Amrita Kalam, Varjyam, Durmuhurta, Abhijit Muhurta, eclipse rules and festival nirnaya are not fully implemented.
- Rahu/Ketu are mean-node estimates. True node, planetary speed/retrograde, shadbala, bhava calculations, divisional charts beyond the basic D9 display, antardasha/pratyantardasha and validated yoga/dosha analysis are not included.
- Birth time must be entered in local Indian Standard Time (IST); coordinates must match the birthplace. Historical time-zone/DST corrections are not implemented.
- Compare output with a trusted Drik Panchanga or professional Vedic astrology software before using for rituals, marriage, muhurta or any important decision. Astrology is a traditional belief system, not a scientifically established predictive method.

DEPLOYMENT
1. Extract this ZIP.
2. Push all files and folders to your GitHub repository, preserving paths.
3. Connect the repository to Netlify. Build command can remain blank; publish directory is ".". netlify.toml configures Functions.
4. In Netlify > Project configuration > Environment variables add:
   Name: GEMINI_API_KEY
   Value: your Google AI Studio API key
   Ensure the variable is available to Functions, then redeploy.
5. Do not expose the API key in browser code or public screenshots.
6. Open the deployed HTTPS site on a phone and choose Install app / Add to Home Screen.

FILES
- index.html
- upgrade.js
- manifest.json
- sw.js
- icon.svg
- netlify.toml
- netlify/functions/ask.mjs
