# requirement-analysis
# Requirement Analysis in Software Development


---

## Introduction

This repository contains a clear, instructor-friendly README that explains Requirement Analysis as part of the Software Development Life Cycle (SDLC). It includes definitions, the importance of requirement analysis, core activities, types of requirements (with examples for a booking management project), a use-case diagram (linked image), acceptance criteria guidance, and a short checklist for manual verification.


---

## What is Requirement Analysis?

**Requirement Analysis** is the process of collecting, refining, documenting, and validating the needs and constraints of stakeholders to produce a clear, agreed set of requirements that the development team will implement. It sits near the start of the SDLC and ensures the team builds the *right* product — not just *a* product.

Key goals of Requirement Analysis:

* Translate stakeholder needs into explicit, testable requirements.
* Remove ambiguity by defining scope and acceptance criteria.
* Provide a foundation for design, development, testing, and deployment.

---

## Why is Requirement Analysis Important?

1. **Reduces rework and cost**

   * Clear requirements prevent misunderstandings that lead to rework, saving time and budget.

2. **Defines project scope and prevents scope creep**

   * Well-documented requirements set boundaries for what will (and will not) be built.

3. **Improves product quality and stakeholder satisfaction**

   * When requirements are validated with stakeholders early, the final product aligns with user needs and expectations.

4. **Enables better planning and resource allocation**

   * Prioritized requirements let teams focus on delivering the highest value features first.

---

## Key Activities in Requirement Analysis

Below are the five key activities with short descriptions and practical tips.

* **Requirement Gathering**

  * Collect stakeholders’ needs using interviews, surveys, workshops, observation, and reviewing existing documents.
  * Tip: Record sessions (with permission) and keep notes for traceability.

* **Requirement Elicitation**

  * Use techniques like brainstorming, user story mapping, prototyping, and use-case exploration to uncover implicit requirements.
  * Tip: Prototypes and low-fidelity mockups are excellent to surface hidden assumptions.

* **Requirement Documentation**

  * Produce clear artifacts such as SRS (Software Requirements Specification), user stories, acceptance criteria, and use-case descriptions.
  * Tip: Keep documents concise and include version history.

* **Requirement Analysis & Modeling**

  * Analyze requirements for conflicts, completeness, and feasibility. Create models such as use-case diagrams, data flow diagrams, and UML to visualize behavior and structure.
  * Tip: Use diagrams to help technical and non-technical stakeholders agree on designs.

* **Requirement Validation**

  * Review and validate requirements with stakeholders through walkthroughs, reviews, and acceptance criteria checks. Ensure each requirement is testable.
  * Tip: Use the “Given/When/Then” template for acceptance criteria to link requirements directly to tests.

---

## Types of Requirements

### Functional Requirements

Functional requirements describe **what** the system should do — the features, behaviors, and interactions.

**Examples for the Booking Management Project**:

* **User Registration**: New users can register with email and password.
* **Secure Login**: Registered users can log in securely (session handling).
* **Property Search**: Users can search properties by location, price, and date availability.
* **View Property Details**: Users can view photos, description, host info, and availability calendar.
* **Make Booking**: Users can select dates, add guest info, and reserve a property.
* **Payment Processing**: Checkout accepts card payments and returns a confirmed transaction ID.
* **Booking Cancellation**: Users can cancel bookings within policy rules.
* **Admin Dashboard**: Admin can approve listings, manage users, and view reservations.

### Non-functional Requirements

Non-functional requirements describe **how** the system should behave — performance, security, reliability, scalability, and usability.

**Examples for the Booking Management Project**:

* **Performance**: Page load time < 2 seconds on standard broadband.
* **Security**: All sensitive data stored encrypted; all traffic via HTTPS.
* **Scalability**: System supports at least 2,000 concurrent users and can scale horizontally.
* **Availability**: 99.9% uptime SLA for the booking API.
* **Usability**: Mobile-responsive UI; 3-step booking flow with clear CTAs.
* **Backup & Recovery**: Daily backups with recovery point objective (RPO) of 24 hours.

---

## Use Case Diagrams

**What are Use Case Diagrams?**
Use case diagrams are UML artifacts that show actors (users or external systems) and the high-level interactions (use cases) they perform with the system. They help communicate scope and user interactions to both technical and non-technical stakeholders.

**Benefits**:

* Quickly visualizes who uses the system and for what.
* Helps identify missing requirements and user roles.
* Useful in reviews when validating requirements with stakeholders.

**Actors and Use Cases for Booking Management** (suggested):

**Actors**:

* Guest (unregistered user)
* Registered User
* Property Owner
* Admin
* Payment Gateway (external system)

**Use Cases**:

* Search Properties
* View Property Details
* Register / Login
* Make Booking
* Checkout / Process Payment
* View Bookings
* Cancel Booking
* Manage Listings (Owner)
* Approve/Reject Listings (Admin)

**Diagram (exported image)**

![Use Case Diagram](alx-booking-uc.png)

> The file `alx-booking-uc.png` is included with this repository. Open it to view the example use-case diagram exported for the booking system.

---

## Acceptance Criteria

**Why Acceptance Criteria matter**:
Acceptance criteria define the conditions a feature must meet to be accepted by stakeholders. They make requirements testable and provide a shared understanding between developers, testers, and product owners.

**Example: Checkout Feature — Acceptance Criteria**

* **Scenario:** Successful payment and reservation

  * Given the user has selected a property and provided valid payment details,
  * When the user confirms payment,
  * Then the payment should be processed successfully by the payment gateway and the booking status should become **Confirmed**;
  * And the system must send a confirmation email to the user with booking details and a transaction ID.

* **Other checks:**

  * Payment failures must display a clear error and leave the booking in a **Pending** state.
  * Payment transactions must be recorded in an audit log for traceability.
  * The checkout must complete within 10 seconds under normal load.

---

## How to use this repository (quick start)

1. **Clone the repo**

   ```bash
   git clone https://github.com/<your-username>/requirement-analysis.git
   cd requirement-analysis
   ```

2. **Open README.md** — review each section and replace placeholder information with your ALX program details and project-specific notes.

3. **View the use-case diagram** — open `alx-booking-uc.png` in any image viewer.

4. **Edit/Add artifacts** — add an SRS.md, detailed user stories, or more diagrams in the `docs/` folder.

---

## Manual Check (Submission checklist)

Before you mark this assignment as done, confirm the following:

* [ ] Repository exists on GitHub and is named `requirement-analysis`.
* [ ] `README.md` contains the required sections and clear content:

  * Title and brief introduction
  * "What is Requirement Analysis?"
  * "Why is Requirement Analysis Important?"
  * "Key Activities in Requirement Analysis"
  * "Types of Requirements" with functional and non-functional examples for the booking project
  * "Use Case Diagrams" that link to `alx-booking-uc.png`
  * "Acceptance Criteria"
* [ ] `alx-booking-uc.png` is present in the repository root and displays the diagram.
* [ ] README and diagram are readable and professional (no placeholder text left behind).

---

## Next steps and suggestions

* Add a `docs/` directory and move expanded artifacts into it (SRS.md, user-stories.md, test-cases.md).
* Create a small runnable demo (e.g., a minimal booking API or UI) and link it from the README with instructions to run locally.
* Add `LICENSE` and `CONTRIBUTING.md` if you plan to open the project for collaboration.

---

*Last updated: *(replace with the date you push this file)**
