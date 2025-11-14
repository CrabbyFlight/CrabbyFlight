# CrabbyFlight

CrabbyFlight is a web-based flight overlay editor and display system for
streamers, virtual pilots, and aviation enthusiasts. It allows users to
create live, professional-quality flight information overlays for OBS
and other streaming software. The system is built using HTML, CSS, and
JavaScript, with Firebase providing authentication and real-time data
synchronization. All user data is stored securely under each user's own
account.

Website: https://www.crabbyflight.co.uk\
Source: https://github.com/CrabbyFlight/CrabbyFlight

------------------------------------------------------------------------

## Overview

CrabbyFlight enables users to sign in, enter their flight details, and
instantly generate live overlays that can be added to OBS as browser
sources. Data is stored securely in Firebase and updates in real time,
so any changes made in the editor are immediately reflected in the
overlays.

### Modes

Each overlay mode is accessed using a URL hash:

  -----------------------------------------------------------------------
  Mode                   Description
  ---------------------- ------------------------------------------------
  `#editor`              Main interface for entering and editing flight
                         information.

  `#info`                Compact overlay with route, callsign, aircraft,
                         and essential details.

  `#departures`          Realistic departure-board style overlay showing
                         your live flight.

  `#frame`               Full 1080p frame with embedded webcam window and
                         live data.
  -----------------------------------------------------------------------

Example overlay URLs:\
https://www.crabbyflight.co.uk/#info:`<yourUID>`{=html}\
https://www.crabbyflight.co.uk/#departures:`<yourUID>`{=html}\
https://www.crabbyflight.co.uk/#frame:`<yourUID>`{=html}

Each link can be used directly as a browser source in OBS or any
compatible streaming software.

------------------------------------------------------------------------

## SimBrief Integration

CrabbyFlight now fully integrates with **SimBrief**.\
Users can enter their SimBrief PilotID and import their latest
operational flight plan directly into the editor.

CrabbyFlight retrieves XML data from the SimBrief API and automatically
fills:

-   Departure & destination airports\
-   Flight number & callsign\
-   Aircraft type\
-   Cruise altitude\
-   Scheduled departure & arrival times\
-   Estimated enroute duration\
-   Route information (when available)

Once imported, all values sync to Firebase and update every overlay mode
in real time.\
Your SimBrief credentials are never stored --- only your imported OFP
data.

------------------------------------------------------------------------

## Technical Summary

-   **Frontend:** HTML, CSS, JavaScript\
-   **Backend:** Firebase Authentication & Realtime Database\
-   **Hosting:** GitHub Pages / crabbyflight.co.uk\
-   **Integration:** SimBrief XML API\
-   **Architecture:** Fully client-side (no dedicated backend server)

------------------------------------------------------------------------

## Security and Privacy

CrabbyFlight is built with privacy in mind:

-   Each user's data is stored under their unique Firebase UID.\
-   Only the account owner can edit their data; overlays are read-only
    to others.\
-   Firebase security rules enforce authenticated write access only.\
-   No analytics, cookies, or external tracking providers are used.\
-   Stored data includes only your email and overlay configuration
    fields.

------------------------------------------------------------------------

## Usage Policy

CrabbyFlight is free for personal and non-commercial use. You may use it
freely to enhance streams, videos, or flight-simulation content.

The source code, branding, UI design, and project structure are
protected.\
Redistributing, cloning, modifying, or re-hosting CrabbyFlight without
written permission is not allowed --- including derivative or rebranded
versions.

For collaboration, integration, or contributions, please contact the
project owner.

------------------------------------------------------------------------

## License

Copyright © 2025 CrabbyFlight\
All rights reserved.

This software is provided for transparency and educational reference
only.\
It may be used freely by end users but may not be redistributed,
modified, or re-hosted without permission.

------------------------------------------------------------------------

## Contact

Email: info@ridgwaygroup.net\
Website: https://www.crabbyflight.co.uk\
GitHub: https://github.com/CrabbyFlight\
Creator: njridgway
