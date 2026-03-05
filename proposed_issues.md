# Proposed GitHub Issues for New Features

Based on the comparison with the International Essay Competition, here are proposed GitHub issues for adding new features to the Mergington High School Activities API. Each issue includes a title, description, and suggested implementation notes. You can copy these to create actual GitHub issues in your repository.

## Issue 1: Add Contest/Event Structure Support
**Title:** Implement Contest/Event Structure for Activities (e.g., Monthly Competitions with Topics)

**Description:**  
Currently, activities are static. Add support for recurring or themed events like contests/competitions. This could include:
- Activity types (e.g., "contest", "club", "event")
- Recurring schedules (e.g., monthly)
- Themes/topics for each instance
- Start/end dates for sign-ups and events

**Acceptance Criteria:**
- API can create activities with types and themes
- GET /activities returns type and theme info
- In-memory data model updated to include these fields

**Estimated Effort:** Medium

## Issue 2: Add Participant Categories
**Title:** Implement Participant Categories (e.g., Junior/Senior or Age/Grade-Based Restrictions)

**Description:**  
Allow activities to have categories or restrictions based on student attributes (e.g., grade level, age). This enables targeted sign-ups, like junior/senior categories in contests.

**Acceptance Criteria:**
- Students have additional fields (e.g., age, category)
- Activities can specify allowed categories
- Sign-up endpoint validates category eligibility
- GET /activities shows category restrictions

**Estimated Effort:** Low-Medium

## Issue 3: Add Submission and Evaluation System
**Title:** Implement Submission and Evaluation System for Contests

**Description:**  
For contest-type activities, allow students to submit work (e.g., essays, files) and have them evaluated. Include:
- Submission endpoint (e.g., POST /activities/{name}/submit with file/text)
- Plagiarism checks (basic or integrated)
- Evaluation by judges (admin role)
- Status tracking (submitted, evaluated, etc.)

**Acceptance Criteria:**
- New endpoints for submissions
- Data model includes submissions and evaluations
- Basic validation for submissions

**Estimated Effort:** High

## Issue 4: Add Results and Announcements
**Title:** Implement Results Announcements and Notifications

**Description:**  
After activities (especially contests), announce results. Include:
- Winner determination logic
- Announcement system (email, in-app notifications)
- Results page or endpoint
- Integration with social media or external channels (future)

**Acceptance Criteria:**
- POST /activities/{name}/announce-results endpoint
- GET /activities/{name}/results
- Email notification simulation (or integration)

**Estimated Effort:** Medium-High

## Issue 5: Add Rewards and Incentives
**Title:** Implement Rewards System (Certificates, Prizes, Vouchers)

**Description:**  
Add rewards for participation and winning. Include:
- Certificates for all participants
- Prizes/vouchers for winners
- Sponsor-provided incentives
- Generation of certificates (PDF or text)

**Acceptance Criteria:**
- Data model includes rewards
- Endpoints to claim/issue rewards
- Basic certificate generation

**Estimated Effort:** Medium

## Issue 6: Add Sponsorship and External Support
**Title:** Implement Sponsorship Tracking for Activities

**Description:**  
Allow activities to have sponsors (e.g., corporate or NGO support). Include:
- Sponsor details (name, contributions)
- Linking sponsors to activities
- Displaying sponsor info in activity details

**Acceptance Criteria:**
- Activities include sponsor field
- GET /activities shows sponsor info
- Admin can add sponsors

**Estimated Effort:** Low

## Issue 7: Expand to Global/Online Access
**Title:** Expand API for Global/Online Participation

**Description:**  
Make the API more flexible for non-school users (e.g., global contests). Include:
- Remove school-specific assumptions
- Enhanced authentication (beyond email)
- Online submission support
- Scalability for external users

**Acceptance Criteria:**
- API works for any user (not just Mergington students)
- Authentication updates
- Documentation for external use

**Estimated Effort:** High

## Issue 8: Add FAQs and Guidelines
**Title:** Implement FAQs and Guidelines for Activities

**Description:**  
Provide help and rules for activities. Include:
- Per-activity FAQs
- Guidelines/rules
- Endpoint to retrieve them
- Admin editing

**Acceptance Criteria:**
- Activities include FAQ/guideline fields
- GET /activities/{name}/help endpoint
- Editable by admins

**Estimated Effort:** Low

## Issue 9: Add Advanced Judging and Quality Assurance
**Title:** Implement Advanced Judging System

**Description:**  
For contests, add expert judging. Include:
- Judge roles/users
- Evaluation criteria
- Unbiased scoring
- Quality checks

**Acceptance Criteria:**
- Judges can evaluate submissions
- Scoring system
- Results based on evaluations

**Estimated Effort:** High

These issues can be prioritized based on your roadmap. Start with low-effort ones like categories or sponsorships, then build towards contests.