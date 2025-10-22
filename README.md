# Requirement Analysis in Software Development.
**Introduction**
The purpose of this repository is to write in full detial about Requirement analysis in software development

**Requirement Analysis in Software Development**

Requirement Analysis is a crucial phase in the Software Development Life Cycle (SDLC) that focuses on identifying, gathering, and analyzing the needs and expectations of users, clients, and stakeholders. It serves as the foundation upon which the entire software project is built, ensuring that the development team fully understands what the system should do and how it should perform under different conditions.

During requirement analysis, software engineers, business analysts, and stakeholders collaborate to define both functional requirements (what the system should do) and non-functional requirements (how the system should behave, such as performance, security, and usability). This process involves multiple techniques such as interviews, questionnaires, observation, document analysis, and prototyping to extract accurate information about the users’ needs.

**Key Activities in Requirement Analysis**

**Requirement Gathering:** Collecting information from users, customers, and other stakeholders about what the system should achieve.

**Requirement Elicitation:** Using techniques like brainstorming, use case analysis, and workshops to uncover hidden or implicit requirements.

**Requirement Documentation:** Clearly recording all requirements in a structured format such as a Software Requirement Specification (SRS) document.

**Requirement Validation:** Ensuring that the documented requirements are complete, consistent, feasible, and aligned with business objectives.

**Requirement Management:** Tracking changes to requirements throughout the project lifecycle and maintaining clarity as the project evolves.

**Importance of Requirement Analysis in SDLC**

**Establishes a Clear Understanding:** It ensures that developers and stakeholders share a common understanding of the project’s goals, reducing confusion and miscommunication.

**Prevents Scope Creep:** By defining requirements early, the team can avoid unnecessary changes and manage client expectations effectively.

**Improves Project Planning:** Accurate requirements help in better estimation of time, cost, and resources, contributing to realistic project planning.

**Enhances Product Quality:** When requirements are well-defined and validated, the resulting software is more likely to meet user needs and perform reliably.

**Three key reasons why Requirement Analysis is critical in the Software Development Life Cycle (SDLC):**

1. Ensures Clear Understanding Between Stakeholders and Developers

Requirement Analysis bridges the communication gap between clients, users, and the development team. It ensures that everyone involved shares the same understanding of what the software should achieve. By defining goals, functions, and constraints early, the team minimizes confusion and misinterpretation, which are common causes of project failure.

2. Reduces Costly Errors and Rework

Identifying and fixing requirement-related issues during the early stages is far less expensive than discovering them later in development or after deployment. Proper analysis helps detect inconsistencies, missing details, or unrealistic expectations before coding begins—saving time, cost, and effort that would otherwise be spent on rework.

3. Provides a Solid Foundation for Design and Development

A well-conducted requirement analysis produces a clear Software Requirement Specification (SRS) document, which serves as a blueprint for system design, coding, and testing. It ensures that every subsequent SDLC phase is guided by accurate, well-defined requirements, leading to a more organized and predictable development process.
**Reduces Development Cost and Time:** Detecting and correcting requirement errors early is far less expensive than fixing them during or after development.

**Ensures User Satisfaction:** A thorough understanding of user needs leads to the creation of software that solves real problems and adds value.

# Key Activities in Requirement Analysis.
* Requirement Gathering: Requirement Gathering is the first and one of the most important steps in the Requirement Analysis phase of the Software Development Life Cycle (SDLC). It involves the systematic process of collecting information from clients, users, and other stakeholders to understand what the software system should achieve.
* Requirement Elicitation: Requirement Elicitation is the process of discovering, extracting, and clarifying the needs, expectations, and constraints of stakeholders for a software project. It goes beyond simply collecting information — it involves actively engaging with stakeholders to uncover both explicit and hidden requirements that may not be immediately obvious.
* Requirement Documentation: Requirement Documentation is the process of recording, organizing, and maintaining all the information gathered during requirement analysis and elicitation in a clear, structured, and accessible form. It serves as the official reference point for the entire software development team, ensuring that everyone involved — from developers and testers to project managers and clients — shares the same understanding of what the system must accomplish.
* Requirement Analysis and Modeling: Requirement Analysis and Modeling is a crucial phase of the Software Development Life Cycle (SDLC) that focuses on deeply understanding, refining, and visually representing the system requirements gathered from stakeholders. It involves studying the collected information to ensure that it is complete, consistent, feasible, and clearly understood, and then converting it into structured models that describe how the system will function and interact with users or other systems.
* Requirement Validation: Requirement Validation is the process of ensuring that the requirements gathered and documented during the analysis phase are correct, complete, consistent, feasible, and aligned with stakeholder needs. It helps confirm that the software being planned will meet user expectations and fulfill business objectives before moving into the design and development stages of the Software Development Life Cycle (SDLC).

  **Types of Requirements**

  * Functional Requirements
  * Non-Functional Requirements
  
**Functional Requirements**
Hotel Listing & Management

The system shall provide a “Hotel Manager Portal” that allows hotel owners/managers to create, update and delete hotel listings (rooms, rates, photos, availability).
(Matches the “Hotel Management Service” in the case study) 
Medium

The system shall sync listing updates so that changes in the manager portal reflect in the customer-search listing in near real-time.

Search and Availability

The system shall allow customers to search for hotels by criteria such as location, date range (check-in/check-out), number of guests, room type.

The system shall only present available rooms/units (not already booked) for the specified date range.

The system shall allow customers to view detailed information for a hotel (room types, price, amenities, cancellation policy).

Booking Creation & Payment

The system shall allow authenticated users (or guest users, if allowed) to book a specific room/slot for a chosen date range.

On booking, the system shall initiate a payment transaction via a third-party payment service, and upon successful payment, confirm the booking and generate a unique booking reference/ID.

The system shall send a booking confirmation to the user (email, SMS, or in-app).

The system shall update the availability status of the room to “booked” for the selected date range.

Modification / Cancellation

The system shall allow users to cancel or modify their booking (subject to policy) and the system must update availability accordingly.

The system shall handle refunds (or partial refunds) if the user cancels according to policy.

View Booking History / Status

The system shall allow users to view their current and past bookings, including status (confirmed, cancelled, completed) and details.

The system shall allow hotel managers to view bookings made for their hotel(s), including status and guest information.

Notifications

The system shall send notifications to users and hotel managers when certain events occur: e.g., booking confirmed, booking cancelled/modification, special offers, availability changes.
(The article mentions using a messaging queue for notifications) 
Medium

Reporting & Analytics

The system shall generate reports (for hotel managers/admins) on metrics such as number of bookings per period, occupancy rate, cancellation rate, revenue, etc.

The system shall support analytics of historical booking data for business insight (as referenced via Hadoop/BigData in the case study)

**Non-Functional Requirements**
These describe how the system must perform or operate.
Performance / Responsiveness

The system shall respond to typical search requests (location + date range) within 2 seconds under standard load.

The system shall support 2000+ concurrent users during peak hours without performance degradation (depending on scale). This aligns with high traffic booking scenarios as in the article. 
Medium

The system shall use caching (e.g., Redis) for frequent queries to reduce database load and improve response time (mentioned in the architecture) 
Medium

Scalability

The system architecture must allow horizontal scaling (adding more servers or services) for both search and booking components to handle growth.

The system shall support caching, replication and distributed design (as the architecture uses master-slave DB, caching, message queue) 
Medium

Reliability / Availability

The system shall be available 99.9% of the time, except for scheduled maintenance.

The system shall gracefully handle failures in one zone, with failover to backups (e.g., database replicas, queue systems) so that bookings are not lost.

Security

The system shall encrypt sensitive user data (passwords, payment info) and use HTTPS for all user-facing communications.

The system shall implement role-based access control: Hotel managers only access their own listings; administrators have broader access; customers access only their data.

The system shall ensure transaction integrity for bookings and payments (no double booking, atomic booking + payment).

Maintainability & Extensibility

The system shall be built in a modular fashion (microservices) so that each service (search, booking, hotel management, notification) can be maintained separately. (As described in the article) 
Medium

The system shall have clearly documented APIs for future extension (e.g., adding new payment methods or loyalty modules).

Usability

The user interface shall be responsive and support web, mobile web, and optionally native mobile platforms.

The system shall provide an intuitive search/booking flow with minimal steps.

Data Consistency / Integrity

The system shall guarantee that once a booking is confirmed, the availability of that room for that period is locked and not displayed as available to others.

The system shall use event queues and replication mechanisms (master-slave DBs, message queues) to ensure consistency of data across services. 


**Use Case Diagrams**

A Use Case Diagram is a visual representation used in software engineering to describe how users (actors) interact with a system.
It is part of the Unified Modeling Language (UML) and helps illustrate functional requirements — showing what the system should do from the user’s point of view.

**Benefits of Use Case Diagrams**

Clarifies System Scope:
It visually defines what is inside the system’s functionality and what’s not.

Enhances Communication:
Helps developers, designers, and stakeholders share a common understanding of system goals and user interactions.

Captures Functional Requirements Early:
Makes it easier to identify what features need to be developed and which actors use them.

Supports Testing and Validation:
Test cases can be derived directly from use cases to ensure each functionality is covered.

Simplifies Complex Systems:
Breaks down large systems (like a booking platform) into manageable interactions.

<img width="1536" height="1024" alt="alx-booking-uc png" src="https://github.com/user-attachments/assets/ea82f0db-b754-47fe-a6fc-55a686ae0162" />


**Acceptance Criteria**
Acceptance Criteria (AC) are the predefined conditions or statements that a software product or feature must meet for it to be accepted by the stakeholders, client, or end user. They are usually written in clear, testable terms and serve as a benchmark to determine whether a requirement has been successfully implemented.

Why Acceptance Criteria Are Important

* Clarifies Expectations:
Acceptance criteria ensure that both developers and stakeholders have a shared understanding of what a feature is supposed to achieve. This reduces ambiguity and miscommunication.

* Defines the "Done" State:
It clearly specifies when a feature can be considered complete, preventing scope creep or unfinished features being marked as done.

* Guides Development and Testing:
Acceptance criteria act as the foundation for test cases. QA teams can design test scenarios directly from the AC to verify that the system works as intended.

* Improves User Satisfaction:
By ensuring that all requirements are measurable and validated against user needs, acceptance criteria increase the likelihood of delivering a product that meets user expectations.

* Facilitates Agile Collaboration:
In Agile development, ACs help developers, product owners, and testers align on goals during sprint planning and backlog refinement sessions.

**Example: Acceptance Criteria for the "Checkout Feature" in a Booking Management**

Feature: Checkout (Completing a booking payment and confirming reservation)

User Story:

As a customer, I want to complete my booking and make a secure payment so that I can confirm my reservation and receive a receipt.

**Acceptance Criteria:**

✅ Payment Integration:

The system must allow users to choose a payment method (credit/debit card, PayPal, or mobile payment).

Payment processing should be handled securely through an integrated payment gateway (e.g., Stripe, Paystack).

✅ Validation and Error Handling:

The system must validate all payment inputs (card number, expiry date, CVV).

If payment fails, an error message must be displayed, and the user should have the option to retry.

✅ Booking Confirmation:

Upon successful payment, the system must generate a unique booking reference number.

A confirmation message and summary of the booking must be displayed to the user.

✅ Email/SMS Notification:

The system must send an email and/or SMS to the customer confirming the booking details and payment receipt.

✅ Availability Update:

The booked room must be automatically marked as unavailable for the selected date range in the system.

✅ Security and Compliance:

All transactions must occur over HTTPS.

Sensitive information (like card details) must not be stored in the system.

The system must comply with PCI DSS standards.

✅ System Logging:

The system must log all checkout transactions (successful or failed) for auditing purposes.
