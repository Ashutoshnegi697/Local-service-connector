# Local Service Connector — DSA-Based Booking System

A terminal-based local service booking simulation built in **C++**. The project demonstrates how data structures can be used to manage users, service providers, search results and booking requests.

**Team:** Decode  
**Project GitHub:** https://github.com/Ashutoshnegi697/Local-service-connector  
**Project status:** 100% complete — all four modules integrated.

---

## Project Abstract

People often find local workers such as electricians and plumbers through personal contacts, phone calls or messaging groups. Comparing providers by area, rating and past work can be difficult when this information is scattered.

Local Service Connector is a C++ console application that simulates local service booking for selected areas of Dehradun. A user signs in, searches for a service in an area, views providers sorted by rating and work count, books a provider and tracks the booking. Providers can accept or reject incoming requests.

The main aim is to apply Data Structures to a practical booking problem.

## Project Approach and Architecture

The application uses a menu-driven console interface. It has three logical parts:

- **Menu layer:** accepts user input and displays options.
- **Logic layer:** performs sign-in, provider search, booking and request operations.
- **Data layer:** stores users, providers and bookings in linked lists, queues and stacks.

All data remains in memory while the program runs. The application does not use a database, network connection, OTP system or graphical interface.

Provider search works in two passes: first it counts matching providers, then it creates a pointer array of exactly that size. The results are sorted by rating and work count.

A booking is added to the provider's circular queue (capacity 5). If that queue is full, the request is placed in a waiting queue. On completion, the booking is added to the user's and provider's history stacks.

**Languages and tools:** C++, Git and GitHub.

## Data Structures Used

| Project part | Data structure | Purpose |
|---|---|---|
| Users | Singly linked list | Supports sign-ups with quick front insertion |
| Providers | Singly linked list | Stores providers and supports traversal during search |
| Provider requests | Circular queue (size 5) | Reuses freed slots and serves requests in order |
| Extra requests | Waiting queue (size 5) | Holds requests when the provider queue is full |
| Cancelling from the middle | Temporary queue | Moves other requests while skipping the cancelled request |
| User and provider history | Stacks (size 5) | Keeps the latest booking on top; a temporary stack removes the oldest |
| Search results | Dynamic pointer array | Allocates the exact number of matches before sorting |

## Booking Flow

1. **Sign in and choose:** The user signs in and selects a service and area from the menus.
2. **Search:** A two-pass search builds the provider array, which is sorted by rating and work count.
3. **Book:** The user selects a provider and a booking is created with status `Pending`.
4. **Queue:** The booking enters the provider's circular queue, or the waiting queue if the circular queue is full.
5. **Accept or reject:** The provider accepts or rejects the request. Its status is updated; after the work, it becomes `Completed`.
6. **Finish:** The booking is pushed onto the user and provider history stacks, the provider's work count increases, and the user can submit a rating. The average is calculated as rating sum divided by rating count.

## Memory Handling

A booking is referenced by the user stack, provider queue and provider stack. Each booking has one owner and is deleted in only one place; queues and stacks store pointers to it. This ownership approach avoids dangling pointers and double deletion. A final memory clean-up check was completed after integration.

## Module Mapping and Contributions

Select a team member's name to open their individual contribution file. Each file includes their GitHub ID and profile link.

| Module | Responsibility | Team member |
|---|---|---|
| Module 1 | User class, user linked list, sign-up, sign-in and password recovery | [Devyansh Bariswal](team/members/member-1-devyansh-bariswal.md) |
| Module 2 | Provider class, provider linked list, service and area menus, and search | [Rakshita Pant](team/members/member-2-rakshita-pant.md) |
| Module 3 | Booking queue, waiting queue and temporary queues | [Devyansh Bhardwaj](team/members/member-3-devyansh-bhardwaj.md) |
| Module 4 | Main menu, Booking class, history stacks, status changes and rating | [Ashutosh Negi — Team Lead](team/members/member-4-ashutosh-negi.md) |

All members collectively completed function interfaces between modules, weekly code merging, full integration, testing, memory clean-up checks and documentation.

## Challenges and Roadblocks

1. **Unique IDs with front insertion:** Separate counters for each list ensure IDs are not reused.
2. **Circular queue full or empty:** A count variable distinguishes full and empty states when front and rear positions coincide.
3. **Shared booking pointers:** Each booking has one owner and is deleted in one place, avoiding dangling pointers and double deletion.
4. **Input problems:** Small validated input functions handle the interaction between `cin` and `getline`.
5. **Password recovery without OTP:** The details supplied at sign-up are checked before a password reset is allowed.

## Project Outcome

The completed deliverable is a runnable C++ terminal application that provides:

- Separate user and provider sign-up and sign-in, with password recovery.
- Provider search by service and area, sorted by rating and work count.
- Booking requests managed through circular and waiting queues (size 5).
- Accept, reject and cancel request operations.
- Recent booking history using stacks.
- Provider work count and average rating calculation.
- Source code and project documentation in this repository.

## Testing and Validation

| Test area | Status | Validation |
|---|---|---|
| Sign-up, sign-in and password recovery | Pass | Correct and incorrect credentials handled; IDs unique; menu inputs validated |
| Provider search and sorting | Pass | Exact service and area matches; sorted by rating and work count |
| Circular and waiting queues | Pass | Full and empty cases work; extra requests enter the waiting queue |
| Cancellation | Pass | Middle request can be removed while preserving the order of others |
| History stacks | Pass | Latest booking stays on top; oldest is removed when size 5 is exceeded |
| Booking status and rating | Pass | Pending, accepted, completed and cancelled statuses work; rating uses sum / count |
| Memory clean-up check | Pass | Each booking is deleted in one place; no dangling pointers |

## Completion Status

**100% complete.** All eight milestones are done, from shared classes through the final memory clean-up check. The waiting queue, history stacks, status changes, cancellation and rating were integrated and tested with the earlier modules.

---

*B.Tech CSE project — Team Decode.*
