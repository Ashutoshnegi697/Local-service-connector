# Local-service-connector
he platform provides a simple and user-friendly interface where customers can discover service providers, compare available options, request services, and connect directly with professionals. It also allows skilled individuals to register as service providers or trainers and offer their services to customers.YOGYA
LOCAL SERVICE CONNECTOR
Project Documentation

Connecting neighbourhoods with trusted local services
and community skill-sharing

DOCUMENT DETAILS	DESCRIPTION
Project name	Yogya – Local Service Connector
Project type	Web application / academic project prototype
Primary users	Customers, local service providers, trainers and learners
Current frontend	Single-page HTML, CSS and JavaScript prototype
Current data storage	Browser localStorage (prototype/demo data)
Document version	1.0

 
1. Executive Summary
Yogya is a local service connector designed to help people discover and request everyday services from nearby professionals. Customers can find a service provider, submit a booking request, follow its status, complete payment recording and rate the service. Providers can manage incoming requests and accepted jobs. The application also includes a community learning feature: users and providers can list skills they teach, discover trainers and request learning sessions.
The supplied frontend is a working browser-side prototype. It demonstrates the main user journeys with sample accounts and seeded records. Its current implementation stores application data in the browser's localStorage; SMS, OTP and payment experiences are simulated in the interface and are not connected to live external services.
2. Problem Statement
Finding a suitable local professional can require searching multiple sources, contacting providers individually and repeatedly checking availability. Customers may also find it difficult to track whether a request has been accepted or completed. At the same time, people with useful skills may not have a simple local platform through which they can offer lessons.
Yogya addresses these needs through one interface for local service discovery, booking management and community skill-sharing.
3. Objectives
•	Provide a simple way to discover local service providers by service category and area.
•	Allow customers to create and track service booking requests.
•	Allow providers to accept or reject requests and close completed jobs.
•	Show booking progress and communicate status changes through an in-app demo SMS inbox.
•	Support payment-status recording and customer ratings in the prototype.
•	Allow users and providers to publish skills, discover trainers and request sessions.
•	Provide separate navigation and capabilities for customer and provider roles.
•	Create a foundation that can later be connected to a secure backend and database.
4. Scope and User Roles
4.1 Customer
•	Register or sign in as a customer.
•	Browse available services and providers by area.
•	Create a booking request and view active or completed bookings.
•	Cancel eligible bookings, view job progress and access the job code when issued.
•	Record payment and rate a completed service.
•	Find trainers, request learning sessions and manage their own skill listings.
4.2 Service Provider
•	Register or sign in as a service provider.
•	View incoming booking requests.
•	Accept or reject pending requests.
•	View accepted jobs and close a job after validating the customer's job code.
•	Review completed work and provider-side activity.
•	Publish a skill they can teach and respond to learning-session requests.
4.3 Trainer and Learner
The trainer feature is available to both customer and provider accounts. A member can publish a skill listing or search for another member's listing. Listings include the skill name, category, level, teaching mode, area, fee and a short description. Learners can send a message with a session request; the listing owner can accept or decline it.
5. Main Functional Modules
Module	Description / Demonstrated functions
Authentication	Customer/provider role selection, sign-in, registration, password sign-in, OTP-style demo flow and password reset interface.
Service discovery	Service categories, area selection, provider cards, service fee and provider rating display.
Booking management	Create booking, waiting queue, accept/reject, cancellation rules, active and completed booking views.
Job completion	Provider enters the four-digit job code supplied to the customer before closing an accepted job.
Payment interface	UPI-style form and cash-after-service option; payment result is simulated in the prototype.
Ratings	Customer can rate completed work; provider's displayed rating is recalculated from recorded ratings.
SMS inbox	In-app demonstration inbox shows booking, acceptance, completion, payment and session notifications.
Skill sharing	Find trainers, filter listings, publish a skill, request sessions and manage incoming/outgoing requests.
Profile and preferences	Account profile and security-related interface elements.
Theme and feedback	Light/dark theme switch, status badges, confirmation prompts and toast notifications.

6. Service Categories and Sample Areas
The frontend includes these service categories:
•	Plumber
•	Carpenter
•	Electrician
•	Geyser Repair
•	AC Repair
•	Painter
•	Cleaner
•	Appliance Repair
•	Vegetable Vendor
The sample area list in the prototype includes Rishikesh, Raipur, Dehradun, Clement Town and Prem Nagar.
The skill-sharing categories include Coding & Tech, Dance, Music, Art & Craft, Languages, Sports & Fitness, Academics, Cooking, Business & Finance and Other. Skill levels include Beginners, Intermediate, Advanced and All levels.
7. Key Workflows
7.1 Customer booking workflow
1.	Customer signs in and opens the service booking section.
2.	Customer chooses a service and an area.
3.	The interface displays matching providers and their fee/rating information.
4.	Customer submits a booking request. The booking is created with WAITING status.
5.	The provider receives a demo notification and can accept or reject the request.
6.	If accepted, a four-digit job code is generated and shown to the customer.
7.	After the service is finished, the provider enters the job code to close the job.
8.	The customer can then record payment and submit a rating.
7.2 Provider workflow
9.	Provider signs in and opens the request queue.
10.	Provider reviews customer and booking details.
11.	Provider accepts or rejects a pending request.
12.	Accepted jobs appear in the provider's accepted-jobs section.
13.	After service completion, provider validates the job code and closes the job.
7.3 Skill-sharing workflow
14.	A member opens Trainers and chooses Find a trainer to browse and filter listings.
15.	The learner opens a listing and sends a short message describing their learning needs.
16.	The trainer reviews the request and accepts or declines it.
17.	The learner sees the request status and can continue with the session/payment demonstration where available.
18.	A member can choose Teach a skill to create or manage their own listing.
8. Booking Statuses and Business Rules
Status / rule	Meaning
WAITING	Booking has been submitted and is waiting for the provider's response.
ACCEPTED	Provider has accepted the booking; a job code is issued.
REJECTED	Provider cannot take the request.
CANCELLED	Eligible booking has been cancelled.
COMPLETED	Provider has validated the job code and closed the job.
Queue limit	The prototype limits a customer's active bookings and a provider's waiting/accepted workload to five, according to the relevant checks.
Completion validation	An accepted job cannot be closed unless the entered code matches the generated job code.

9. Frontend Technology and Design
Technology	Use in supplied frontend
HTML5	Page structure, forms, navigation and content containers.
CSS3	Responsive layout, cards, tabs, status labels, modal sheets, theme variables and visual styling.
JavaScript (vanilla)	Application state, rendering, form handling, booking logic, trainer requests and interactions.
Browser localStorage	Persists the prototype's application data between page reloads on the same browser.
Google Fonts	Bricolage Grotesque, DM Sans and Noto Sans Devanagari font families.

The frontend is implemented as a single-page interface. It renders different sections based on the current account role and selected tab. It uses a responsive layout and supports both light and dark themes.
10. Data Model Overview
Data entity	Important fields represented in the prototype
User	id, name, phone, email, password, area and account-related fields.
Provider	id, name, phone, email, password, service, area, fee, rating totals and work count.
Booking	booking number, customer ID, provider ID, service, area, status, created time, amount, job code, rating and payment record.
Trainer listing	listing ID, owner role/ID, skill, category, level, mode, area, fee, bio and creation time.
Learning session	session ID, listing ID, skill, trainer, learner, message, status, amount and payment record.
SMS message	message ID, recipient phone, message text, timestamp and read state.

These are logical JavaScript data structures in the current prototype. They are not yet database tables or a production backend schema.
11. Current Prototype Limitations
•	Data is stored in localStorage on one browser. It is not shared between different devices or users.
•	Sample accounts and seeded records are included for demonstration.
•	The OTP flow and SMS inbox are simulated; no real SMS is sent.
•	The payment interface is a demonstration; no real UPI transaction or payment gateway is connected.
•	Authentication is frontend-only in this version. Passwords and sessions are not protected by a server-side authentication system.
•	There is no live backend API or production database connection in the supplied HTML file.
•	Provider listings and sample areas are demonstration data, not a verified live directory.
•	Production deployment would require security, privacy, validation, reliability and operational safeguards.
12. Recommended Future Enhancements
•	Build a backend using Node.js and Express or another suitable server framework.
•	Connect a relational database such as PostgreSQL for users, providers, bookings, ratings, trainer listings and sessions.
•	Implement server-side password hashing, authentication tokens/sessions and role-based authorization.
•	Integrate a legitimate SMS/OTP provider for phone verification and notifications.
•	Integrate a compliant payment gateway for real online payments; never treat a frontend success screen as proof of payment.
•	Add provider onboarding, identity/business verification and a process for reporting inaccurate listings.
•	Add search by distance, availability and service filters.
•	Add admin tools, audit logs, privacy controls, rate limits and secure image uploads.
•	Add automated tests for booking state transitions, code validation, payment status and authorization.
13. Suggested Backend Architecture
A future full-stack version can be organized into the following layers:
Layer	Responsibilities
Frontend	User interface, forms, navigation, validation feedback and API calls.
REST API	Authentication, users, providers, service discovery, bookings, ratings, trainers and sessions.
Business logic	Booking state transitions, queue limits, job-code validation, payment reconciliation and permissions.
Database	Persistent relational storage for accounts, provider profiles, bookings, payments, ratings and skill listings.
External services	SMS/OTP and payment gateway integrations, added only after secure server-side implementation.

Suggested API groups:
•	POST /api/auth/register and POST /api/auth/login
•	GET /api/services and GET /api/providers
•	POST /api/bookings, GET /api/bookings, PATCH /api/bookings/:id
•	POST /api/bookings/:id/complete
•	POST /api/bookings/:id/ratings
•	GET /api/trainers, POST /api/trainers, PATCH /api/trainers/:id
•	POST /api/sessions and PATCH /api/sessions/:id
14. Testing Checklist
•	Customer and provider demo sign-in work with the supplied sample accounts.
•	Customer can select a service and area and submit a booking.
•	Provider can accept and reject waiting requests.
•	Accepted booking displays a job code to the customer.
•	Incorrect job code is rejected; correct code closes the job.
•	Eligible bookings can be cancelled.
•	Completed booking appears in the completed section.
•	Customer can record a rating and the provider rating updates.
•	Demo SMS messages appear in the inbox and read state updates.
•	Users can find trainers, publish a skill and request a session.
•	Trainer can accept or decline a session request.
•	Theme switching and responsive layout remain usable.
15. Conclusion
Yogya combines local service discovery and booking management with a community skill-sharing feature. The supplied frontend demonstrates the main customer, provider, trainer and learner journeys, including request tracking, job-code validation, ratings and simulated notifications. It is a useful prototype foundation for an academic project. To become a real multi-user service, the next major step is to replace browser-only demo state with a secure backend, persistent database and verified external integrations.
Appendix A – Demo Account Information
The interface includes sample account shortcuts for demonstration. The frontend indicates the shared sample password as demo123 and exposes Customer ID 1 and Provider ID 100. These credentials are for local prototype testing only and must not be reused in a deployed application.

— End of Document 

