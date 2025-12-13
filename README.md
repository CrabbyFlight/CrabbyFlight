# CrabbyFlight

CrabbyFlight is a web-based flight overlay editor and display system for streamers, virtual pilots, and aviation enthusiasts. It allows users to create live, professional-quality flight information overlays for OBS and other streaming software. The system is built using HTML, CSS, and JavaScript, with Firebase providing authentication and real-time data synchronization. All user data is stored securely under each user’s own account.

Notable features added recently include unified frame controls (border color/width/radius) that apply across the overlay, a webcam mask generator that downloads rounded PNG masks matching your webcam size, a SimBrief importer with robust UTC parsing, and a light/dark theme toggle in the editor.

Website: [https://www.crabbyflight.co.uk](https://www.crabbyflight.co.uk)  
Source: [https://github.com/CrabbyFlight/CrabbyFlight](https://github.com/CrabbyFlight/CrabbyFlight)

---

## Overview

CrabbyFlight enables users to sign in, enter their flight details, and instantly generate live overlays that can be added to OBS as browser sources. The data is stored securely in Firebase and updates in real time, so any changes made in the editor are immediately reflected in the overlays.

### Modes

Each overlay mode is accessed through the URL hash:

| Mode | Description |
|------|--------------|
| `#editor` | Main interface for entering and editing flight information. |
| `#info` | Compact overlay showing flight details such as route and aircraft. |
| `#departures` | Realistic departures board with one live row showing the user’s flight. |
| `#frame` | Full 1080p frame with an embedded webcam window and live flight data. |

Example overlay URLs:
  
https://www.crabbyflight.co.uk/#info:<yourUID>  
https://www.crabbyflight.co.uk/#departures:<yourUID>  
https://www.crabbyflight.co.uk/#frame:<yourUID>  


Each URL can be used directly as a browser source in OBS or any compatible streaming application.

---

## SimBrief integration

CrabbyFlight supports importing flight plans from SimBrief. Enter your SimBrief PilotID (or username) and click "Import from SimBrief" in the editor to fetch and parse the SimBrief XML. Imported fields include origin/destination, flight number, aircraft & registration (airframe), cruise altitude, ETE, and scheduled UTC departure/arrival times. The importer has improved UTC parsing to handle epochs, offsets, and common SimBrief formats.

---

## Technical Summary

- Frontend: HTML, CSS, JavaScript  
- Backend: Firebase Authentication and Firebase Realtime Database  
- Hosting: GitHub Pages / crabbyflight.co.uk  
- SimBrief XML API  
- Architecture: Fully client-side (no dedicated backend server)

Additional features:
- Unified frame controls (color, thickness/width, corner radius) apply to frame, info box, and webcam.
- Download rounded webcam masks matching webcam resolution and corner radius for use in OBS.
- Light/dark editor theme toggle, stored in Firebase and localStorage to reduce visual flashing on load.
- Mask generation limits large images to 2048px on the longest dimension to keep downloads reasonable.

---

## Security and Privacy

CrabbyFlight is designed with privacy and security in mind.

- Each user’s data is stored in Firebase under their unique UID.  
- Only the account owner can edit their data; overlays are read-only for others.  
- Firebase security rules restrict write access to authenticated users only.  
- The application does not use analytics, cookies, or third-party tracking.  
- Only your email address and overlay configuration data are stored.

---

## Usage Policy

CrabbyFlight is free to use for personal and non-commercial purposes. Users are encouraged to use the platform to enhance their streams, videos, or flight simulation events.

However, the source code, design, and branding are protected. Redistribution, cloning, rebranding, or rehosting of CrabbyFlight in any form without written permission from the owner is not allowed. This includes using the codebase to create derivative versions or publishing modified instances under a different name or domain.

If you are interested in collaboration, integration, or contributing improvements, please contact the project owner first.

---

## License

Copyright © 2025 CrabbyFlight.  
All rights reserved.

This software is provided for transparency and educational reference only.  
It may be used freely by end users but may not be redistributed, modified, or rehosted without permission.

---

## Contact

e-mail: [info@ridgwaygroup.net](info@ridgwaygroup.net)  
Website: [https://www.crabbyflight.co.uk](https://www.crabbyflight.co.uk)  
GitHub: [https://github.com/CrabbyFlight](https://github.com/CrabbyFlight)  
Creator: njridgway
