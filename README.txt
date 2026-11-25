DHANVI JYOTHISHYALAYA – SIMPLE PANCHANGAM

This simplified app asks for a date and place, then shows Telugu year (approximate), weekday, tithi, nakshatra, sunrise, sunset, moonrise, Rahu Kalam and an indicative Abhijit window.

Deployment:
1. Upload these files to the root of your existing GitHub repository, replacing the old app files.
2. Keep index.html, manifest.json, sw.js and icon.svg at repository root.
3. Commit changes. Netlify should deploy from the connected GitHub repository.
4. No Netlify Function and no GEMINI_API_KEY are required. Remove the old Netlify function folder if you want to clean up the repository; it is unused by this version.

Notes:
- Internet is required for Astronomy Engine CDN and Open-Meteo geocoding.
- Enter the place in English (e.g. Hyderabad, India).
- Sunrise/sunset/moonrise and lunar calculations use Astronomy Engine. The Telugu year is a simplified Ugadi-date approximation. Abhijit is an indicative daytime midpoint window, not a complete muhurta calculation.
- Verify important ritual timings with a trusted local Drik Panchang.
