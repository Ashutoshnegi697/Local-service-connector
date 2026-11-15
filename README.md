# Yogya — Local Service Connector

**Connecting customers with trusted local service providers and bringing communities together through skill-sharing.**

Yogya (Local Service Connector) is a web application project designed to make it easier for people to discover local service providers, request services, and connect with trainers in their community. It brings service discovery, booking requests, provider profiles, and community skill-sharing into one platform.

**Team:** Decode  
**Project type:** Local services and community skill-sharing platform

---

## About the Project

Finding a reliable electrician, plumber, carpenter, cleaner, or other local professional can be difficult when information is scattered across personal contacts and messaging groups. Yogya aims to make this process simpler by giving customers one place to explore service providers, compare available information, and send booking requests.

The platform also includes a skill-sharing section where people can discover trainers, publish skills they can teach, and request learning sessions.

## Key Features

### 1. Local Service Connection
- Browse different local service categories.
- Explore service providers and their profile information.
- View provider fees, ratings, and service areas.
- Search and filter providers based on available service information.
- Send booking requests to providers.
- Track booking request status.
- Providers can accept or reject incoming requests.
- Confirm job completion through a customer job-code flow.
- Submit ratings after a service is completed.

### 2. Community Skill-Sharing
- Discover trainers based on skills and categories.
- Filter listings by learning level and teaching mode.
- Publish a listing for a skill you can teach.
- Send requests to learn a skill.
- Trainers can accept or decline session requests.

### 3. User Experience
- Separate customer and provider experiences.
- Responsive interface for different screen sizes.
- Light and dark themes.
- Notification inbox and booking/session status feedback.

## How It Works

1. A user opens the platform and chooses the relevant customer, provider, or skill-sharing flow.
2. Customers browse service categories and explore available providers.
3. A customer sends a booking request to a selected provider.
4. The provider reviews the request and accepts or rejects it.
5. The customer can follow the request status and confirm completion through the job-code flow.
6. Users can also explore trainer listings and request community learning sessions.

## Technology Used

| Technology | Use |
|---|---|
| HTML5 | Page structure and content |
| CSS3 | Styling, responsive layouts and themes |
| JavaScript | Frontend interactions and application logic |
| JSON | Frontend configuration and sample data |
| C++ | Team module / data-structure implementation |
| Browser localStorage | Stores prototype data locally in the browser |
| Git & GitHub | Version control and team collaboration |

## Project Structure

```text
Local-service-connector/
├── frontend/
│   ├── index.html
│   ├── styles.css
│   ├── app.js
│   └── config.json
│
└── backend/
    ├── program-source/
    ├── team-modules/
    └── reference/
```

## Run the Project

1. Clone or download this repository.
2. Open the project folder in Visual Studio Code.
3. Open `frontend/index.html` in your browser.

For local development, you can use the **Live Server** extension in Visual Studio Code and open `frontend/index.html) with Live Server.

## Current Prototype Notes

- The frontend currently runs as a browser-side prototype.
- Demo data is stored in the browser using localStorage.
- Some notification and verification flows are simulated.
- The current frontend is not yet connected to a deployed production backend or database.
- Do not enter real passwords or payment details into a prototype.

## Team Contributions

This project was developed by Team Decode. Select a member's name to open their individual contribution file, which includes their GitHub ID and profile link.

| Team member | Project role / contribution | GitHub |
|---|---|---|
| [Ashutosh Negi](team/members/member-4-ashutosh-negi.md) | Team Lead; project coordination and integration | [@Ashutoshnegi697](https://github.com/Ashutoshnegi697) |
| [Devyansh Bhardwaj](team/members/member-3-devyansh-bhardwaj.md) | Booking and request-handling module | [@ayushbhardwaj123b](https://github.com/ayushbhardwaj123b) |
| [Devyansh Bariswal](team/members/member-1-devyansh-bariswal.md) | User management module | [@vansh1928](https://github.com/vansh1928) |
| [Rakshita Pant](team/members/member-2-rakshita-pant.md) | Provider profile and search module | [@Rakshita-wq](https://github.com/Rakshita-wq) |

## Future Scope

- Connect the frontend to a secure backend API.
- Add a production database for users, providers, bookings, and trainer listings.
- Implement secure server-side authentication and role-based access.
- Add verified provider profiles and improved search filters.
- Integrate reliable notification services.
- Improve booking management and add further community features.

---

*Yogya — making local services easier to discover, connect with, and book.*
