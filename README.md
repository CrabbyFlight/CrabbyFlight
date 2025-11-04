# CrabbyFlight

CrabbyFlight is a web-based flight overlay editor and display system for streamers, virtual pilots, and aviation enthusiasts. It allows users to create live, professional-quality flight information overlays for OBS and other streaming software. The system is built using HTML, CSS, and JavaScript, with Firebase providing authentication and real-time data synchronization. All user data is stored securely under each user’s own account.

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
| `#info` | Compact overlay showing flight details such as route, callsign, and aircraft. |
| `#departures` | Realistic departures board with one live row showing the user’s flight. |
| `#frame` | Full 1080p frame with an embedded webcam window and live flight data. |

Example overlay URLs:

https://www.crabbyflight.co.uk/#info:<yourUID>
https://www.crabbyflight.co.uk/#departures:<yourUID>
https://www.crabbyflight.co.uk/#frame:<yourUID>


Each URL can be used directly as a browser source in OBS or any compatible streaming application.

---

## SimBrief Integration (Planned)

A new SimBrief integration feature is in development. Users will be able to enter their SimBrief PilotID and click an “Import from SimBrief” button to automatically retrieve and import their latest flight plan. The system will fetch XML data from the SimBrief API, parse it in the browser, and populate the relevant CrabbyFlight fields automatically.

During initial testing, the XML data was successfully fetched and parsed directly from the browser, so this integration will continue to use that approach. The imported data will include the departure and destination airports, flight number, callsign, aircraft type, cruise altitude, scheduled times, and estimated enroute duration. Once imported, these values will be synced to Firebase and immediately reflected in all overlays.

---

## Technical Summary

- Frontend: HTML, CSS, JavaScript  
- Backend: Firebase Authentication and Firebase Realtime Database  
- Hosting: GitHub Pages / crabbyflight.co.uk  
- Planned Integration: SimBrief XML API  
- Architecture: Fully client-side (no dedicated backend server)

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
