# Yogya — Local Service Connector

<p align="center">
  <strong>Connecting neighbourhoods with trusted local services and community skill-sharing.</strong>
</p>

Yogya is a web application prototype that brings customers and local service providers together. It also includes a community learning feature where people can share skills, discover trainers, and request learning sessions.

---

## Overview

Finding a reliable nearby professional can take time. Yogya aims to make that process simpler by providing one place to explore services, send booking requests, follow job progress, and connect with people who teach useful skills.

**Project type:** Academic / web application prototype  
**Current frontend:** HTML, CSS and vanilla JavaScript  
**Repository:** Local Service Connector

## Features

### Local services
- Browse service categories and sample service areas.
- Explore provider information, fees and ratings.
- Send booking requests and track their status.
- Providers can accept or reject requests.
- Job completion uses a customer job-code confirmation.
- Record demo payment status and submit service ratings.

### Community skill-sharing
- Browse trainer listings by skill and category.
- Filter by level and teaching mode.
- Publish a skill listing.
- Send, accept or decline learning-session requests.

### User experience
- Customer and provider account flows.
- Responsive layout for different screen sizes.
- Light and dark themes.
- In-app demo notification inbox and status feedback.

## Service categories

Plumber · Carpenter · Electrician · Geyser Repair · AC Repair · Painter · Cleaner · Appliance Repair · Vegetable Vendor

## Technology

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and forms |
| CSS3 | Responsive layout, components and themes |
| JavaScript | Frontend interactions and prototype logic |
| JSON | Frontend configuration |
| C++ | Backend / team module source files in the repository |
| Browser localStorage | Local prototype data persistence |

## Project structure

```text
Local-service-connector/
├── frontend/
│   ├── index.html       # Main page
│   ├── styles.css       # Application styles
│   ├── app.js           # Frontend logic
│   └── config.json      # Frontend configuration
│
└── backend/
    ├── program-source/  # Main C++ program
    ├── team-modules/    # Individual team member modules
    └── reference/       # Reference and example code
```

## Run the frontend

1. Clone or download this repository.
2. Open the project folder in Visual Studio Code.
3. Open `frontend/index.html` in a browser.

For local development, you can use the **Live Server** extension in VS Code and select **Open with Live Server** on `frontend/index.html`.

> The current frontend is a browser-side prototype. Its demo data is stored in localStorage, so it stays in that browser rather than being shared between users or devices.

## Demo notes and limitations

Some flows are demonstrations rather than live integrations:

- OTP and SMS notifications are simulated in the interface.
- The payment flow does not process real UPI or card payments.
- Authentication is currently frontend-side and is not suitable for production accounts.
- The current frontend does not yet communicate with a deployed backend API or production database.
- Sample providers, areas and accounts are demonstration data.

Do not use real passwords or payment details in the prototype.

## Contributors

This project is developed by the following team members. Select a member to open their individual contribution/profile file; each file includes their GitHub ID and profile link.

| Member | Contribution | GitHub |
|---|---|---|
| [Member 1 — Ashutosh Negi](team/members/member-1-ashutosh-negi.md) | Group Lead | [@Ashutoshnegi697](https://github.com/Ashutoshnegi697) |
| [Member 2 — Ayush Bhardwaj](team/members/member-2-ayush-bhardwaj.md) | Backend Development | [@ayushbhardwaj123b](https://github.com/ayushbhardwaj123b) |
| [Member 3 — Rakshita Pant](team/members/member-3-rakshita-pant.md) | Provider Profile Module | [@Rakshita-wq](https://github.com/Rakshita-wq) |
| [Member 4 — Devyansh Bariswal](team/members/member-4-devyansh-bariswal.md) | Backend Code Contribution | [@vansh1928](https://github.com/vansh1928) |

## Future improvements

- Connect the frontend to a secure backend API.
- Add persistent database storage for accounts, providers and bookings.
- Implement server-side authentication and role-based access control.
- Integrate verified SMS/OTP and payment services.
- Add provider verification, search filters and automated tests.

## Project goal

Yogya aims to make local services easier to discover and book while creating opportunities for people to share and learn skills within their communities.

---

*Built as a collaborative academic project.*
