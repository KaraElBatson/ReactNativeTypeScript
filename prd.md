# Exam Prep Game for Turkish LGS/YKS – Product Requirements Document (PRD)

### TL;DR

A mobile-first, gamified study app that helps Turkish students prepare for LGS and YKS through adaptive practice, realistic mock exams, and engaging rewards. It blends a calibrated question bank with daily missions, streaks, and clear analytics for students, parents, and teachers. Ideal for middle and high school learners seeking efficient exam prep, plus guardians and educators who want visibility and guidance.

---

## Goals

### Business Goals

* Achieve 50,000 monthly active users (MAU) within six months of launch.

* Convert 5–8% of free users to paid subscriptions by month six.

* Partner with 50 schools or dershane (prep centers) within the first year.

* Reach an average 7-day retention of 35% for new cohorts by month three.

* Maintain customer support CSAT ≥ 4.5/5 and first response time < 12 hours.

### User Goals

* Improve subject mastery via adaptive practice and spaced repetition.

* Simulate exam conditions to build speed and confidence under time pressure.

* Understand strengths and gaps via actionable analytics and topic-level insights.

* Maintain motivation with gamification (streaks, quests, badges) and short sessions.

* Enable parents/teachers to monitor progress and support targeted practice.

### Non-Goals

* Live tutoring or 1:1 teacher-video conferencing at launch.

* Full curriculum replacement; the app complements textbooks/classes.

* Broad international exam coverage; focus is exclusively on LGS/YKS in Turkish market for v1.

---

## User Stories

* LGS Student (Age 12–14)

  * As a student, I want daily 10–15 minute missions, so that I can study consistently without burnout.

  * As a student, I want hints and detailed solutions in Turkish, so that I can learn from mistakes.

  * As a student, I want a streak and badges, so that I stay motivated to practice every day.

  * As a student, I want timed mini-tests, so that I can learn pacing for exam day.

  * As a student, I want to filter questions by unit/topic, so that I can prepare for school quizzes too.

* YKS Student (Age 16–19)

  * As a student, I want diagnostic tests, so that I can get a personalized study plan for TYT/AYT.

  * As a student, I want full-length mock exams, so that I can simulate the real exam experience.

  * As a student, I want performance by topic/net score, so that I choose where to focus next.

  * As a student, I want offline practice, so that I can study during commutes.

  * As a student, I want to set a target score or university, so that I can track progress toward my goal.

* Parent/Guardian

  * As a parent, I want weekly email/app summaries, so that I can see consistent progress.

  * As a parent, I want usage limits and focus mode, so that my child studies without distractions.

  * As a parent, I want a simple subscription plan, so that I can unlock premium without confusion.

* Teacher/Guidance Counselor

  * As a teacher, I want to assign topic-based practice to a class, so that I can reinforce lessons.

  * As a teacher, I want to see student analytics, so that I can provide targeted support.

  * As a teacher, I want to curate question sets, so that I match current curriculum pacing.

* Content Editor/Admin

  * As an admin, I want to create and tag questions by exam, topic, difficulty, and skill, so that the adaptive engine can work effectively.

  * As an admin, I want to approve content workflows, so that quality stays high.

---

## Functional Requirements

* Onboarding & Profiles (Priority: P0) -- Account Creation: Email, phone, or SSO (Apple/Google), with parental consent for minors. -- Exam Selection: Choose LGS or YKS (TYT/AYT/YDT), grade, target score/school. -- Diagnostic Path: Optional quick diagnostic to seed difficulty and study plan.

* Practice & Study Modes (Priority: P0) -- Quick Practice: Short sessions (5–15 questions) by topic and difficulty. -- Adaptive Path: Personalized queue using performance, time-on-task, and confidence. -- Spaced Repetition: Auto resurfacing of weak topics at optimal intervals. -- Explanations & Hints: Step-by-step solutions with tips and common traps.

* Mock Exams & Timing (Priority: P0) -- Exam Simulation: Full-length TYT/AYT/LGS mocks with official-like timing and structure. -- Section Pacing: Per-section timer, pause restrictions, and summary at the end. -- Results & Breakdown: Topic-level performance, time per question, accuracy, and trends.

* Gamification & Motivation (Priority: P1) -- Streaks & Badges: Daily practice streaks, milestone badges, and weekly quests. -- XP & Levels: Earn XP for correct answers and focused behavior; level up by subject. -- Focus Mode: Disables social interruptions, optional background sounds.

* Analytics & Insights (Priority: P0) -- Student Dashboard: Mastery by topic, accuracy, speed, and recommended next steps. -- Parent/Teacher Views: Weekly summaries, risk flags (e.g., low consistency), and assignments. -- Goal Tracking: Progress toward target score/university/high school type.

* Content Management (Priority: P0 for internal tools) -- Question Bank: Create/edit items with images, equations, and diagrams. -- Tagging: Exam > Section > Topic > Subtopic > Skill; difficulty; estimated time. -- Review Workflow: Draft, review, approve, publish; version control; flagging.

* Social & Community (Priority: P2) -- Friends-Only Leaderboards: Weekly friendly competition limited to opt-in peers. -- Study Groups: Small group challenges without chat for safety in v1.

* Payments & Monetization (Priority: P1) -- Freemium: Core practice free; mock exams, advanced analytics, and offline in premium. -- Subscriptions: Monthly/annual with family plans; localized pricing. -- Trials & Discounts: 7-day trial; school bulk codes.

* Notifications & Reminders (Priority: P1) -- Smart Reminders: Nudges based on missed streak, upcoming exam date, and weak topics. -- Parental Summaries: Weekly digest via email/push.

* Accessibility & Localization (Priority: P0) -- Turkish-first UI with English option; RTL not required. -- Dyslexia-friendly fonts, dark mode, scalable text, and color-blind safe palettes. -- Text-to-speech for explanations; keyboard for math symbols.

---

## User Experience

**Entry Point & First-Time User Experience**

* Discovery: Found via app stores, school referrals, social media, or friend invites.

* Install & Launch: Splash screen with concise value prop and Turkish-first experience.

* Onboarding:

  * Select LGS or YKS (TYT/AYT/YDT), grade, and target (score, school, department).

  * Optional diagnostic (10–20 questions) to seed adaptive baseline.

  * Consent flow: Parental consent for minors; data minimization stated clearly.

  * Tutorials: 3 screenshot cards explaining daily missions, mock exams, and analytics.

  * Personalization: Choose study days, preferred session length, and notification times.

**Core Experience**

* Step 1: Home (Today tab)

  * Shows daily mission: "10-question Math + 5-question Turkish."

  * Clear CTAs; progress bar; estimated time; quick start option.

  * Validation: If offline, notify what's cached and what's limited.

  * Success: XP gains, streak continuity, suggested next activity.

* Step 2: Practice Session

  * Multiple-choice question screen with timer (per item or per set).

  * UI: Large tap targets, subject color-coding, formula keypad for math, image zoom.

  * Error states: Poor connection → switch to offline queue; corrupted media → retry/cached fallback.

  * Options: Skip with penalty, request hint, flag question, bookmark for review.

* Step 3: Feedback & Learning

  * Immediate correct/incorrect feedback (toggleable for exam-mode).

  * Detailed solution with steps, common mistakes, and related concepts.

  * Post-item actions: "More like this," "Review topic," "Add to revision list."

* Step 4: Adaptive Next Steps

  * Algorithm injects spaced repetition of weak topics; adjusts difficulty.

  * Mastery meter updates; shows micro-goals (e.g., "Master Quadratic Equations: 2 questions left").

* Step 5: Mock Exam

  * Choose full or section-only; confirm rules (no pauses, limited backtracking based on mode).

  * Timers reflect official exam constraints; warning at 5 minutes remaining.

  * Completion screen: Score estimate, topic breakdown, time analysis, recommended plan.

* Step 6: Analytics

  * Dashboard with trend lines for accuracy and pace; heatmap by topic.

  * Recommendations: "Prioritize Geometry; add 15 min session Tue/Thu."

  * Export/share: Parent/teacher summary (with student consent).

* Step 7: Motivation & Retention

  * Earn badges; weekly quests; leaderboards (opt-in, friends only).

  * Streak freeze token for emergencies (limited to prevent abuse).

**Advanced Features & Edge Cases**

* Offline Mode: Pre-download practice sets and one mock exam; sync results later.

* Accommodations: Extended time settings for accessibility; screen reader support.

* Anti-Cheat for Mocks: Randomized item order; disable hints; analytics to detect improbable speed.

* Content Flags: Users can report errors; auto-route to editors; quick hotfix system.

* Low-End Devices: Lightweight image compression; optional animation reduction.

* Safety: No open chat in v1; anonymized leaderboards; strict profanity filters for usernames.

**UI/UX Highlights**

* Turkish terminology aligned with MEB curriculum; concise labels.

* Color coding by subject (e.g., Turkish=Red, Math=Blue) with color-blind safe variants.

* Consistent iconography; focus on legibility and minimal cognitive load.

* Tap areas ≥ 44px; haptic feedback on answer selection; skeleton loaders for perceived speed.

* Accessibility: Dynamic text sizes, alt text for images, keyboard navigation on web.

---

## Narrative

It's a rainy March evening in Ankara, and Ece, an eighth-grader preparing for LGS, feels overwhelmed by the breadth of topics. Her teacher just covered probability, but her last quiz showed weaknesses in Turkish grammar. Opening the app, she sees a clear plan: a 12-minute mission mixing five probability questions and five Turkish items aligned with the MEB curriculum. Each question offers subtle hints, and when she errs, step-by-step solutions highlight the exact misconception.

After completing the mission, Ece tries a short timed mini-test that mirrors LGS pacing. The timer keeps her focused, while the clean interface ensures she isn't lost in menus. Her dashboard updates instantly—probability mastery ticks up, and a recommendation suggests a spaced review three days later. She smiles as her streak hits 9 days and a new badge appears.

At week's end, her parent receives a concise summary: consistent practice, improved accuracy in probability, and a reminder that Turkish grammar still needs attention. Meanwhile, her teacher assigns a small class set on punctuation. The app seamlessly blends into Ece's school rhythm, turning anxiety into a manageable routine. By exam day, she has not only improved her score but also built confidence and pacing—delivering value to her, reassurance to her family, and measurable outcomes that help the business grow.

---

## Success Metrics

* 7-day retention ≥ 35% and 30-day retention ≥ 20% within 3 months.

* Average study minutes per DAU ≥ 18 minutes by month three.

* Premium conversion ≥ 5–8% and churn ≤ 4% monthly.

* Mock exam completion rate ≥ 25% of active users monthly.

* Content error rate ≤ 0.2% of attempts; question rating ≥ 4.5/5.

### User-Centric Metrics

* Daily mission completion rate.

* Accuracy improvement per topic over 14 and 30 days.

* Average time-on-task and session frequency per week.

* NPS/CSAT for students and parents.

### Business Metrics

* MAU/DAU growth rate and cohort retention.

* Free-to-paid conversion, ARPU, LTV/CAC ratio.

* School/partner acquisition count and activation rate.

### Technical Metrics

* App crash-free sessions ≥ 99.5%.

* P95 question load time ≤ 600 ms (online), ≤ 150 ms (offline cache).

* Uptime SLA ≥ 99.9% for core services.

* Sync error rate ≤ 0.5% of offline sessions.

### Tracking Plan

* Onboarding: exam selection, diagnostic started/completed, consent captured.

* Practice: question served/answered, correctness, hint usage, time per question.

* Sessions: mission started/completed, streak updates, XP awarded.

* Mocks: started/completed, pause events, section breakdown, score.

* Analytics: dashboard viewed, recommendation accepted/ignored.

* Monetization: paywall viewed, trial started, subscription purchase/renew/cancel.

* Notifications: sent, delivered, opened; reminder conversions.

* Errors: content flagged, sync failures, image load failures.

---

## Technical Considerations

### Technical Needs

* Client Applications: Mobile (iOS/Android) and responsive web/PWA.

* Backend Services:

  * User/Auth Service with parental consent logic.

  * Content Service for question bank, tagging, and media.

  * Practice Engine for question selection, spaced repetition, and difficulty adaptation.

  * Exam Simulation Service for timing, session state, and scoring.

  * Analytics Pipeline for events, dashboards, and recommendations.

  * Payment Service integration with secure subscription handling.

* APIs: REST/GraphQL for content, practice, analytics, and payments; webhook support for billing events.

* Data Models:

  * Users (role, consent, exam profile, settings).

  * Questions (metadata: exam, section, topic, subtopic, skill, difficulty, time).

  * Sessions (practice/mocks), Attempts (answer, correctness, time, hint).

  * Progress (mastery by topic), Rewards (streak, badges, XP).

  * Organizations (schools), Classes, Assignments.

### Integration Points

* Authentication: Apple/Google sign-in; optional phone/OTP.

* Payments: Local and global processors (e.g., Iyzico/Stripe), app store subscriptions.

* Notifications: Push (APNs/FCM), email service for summaries.

* Analytics: Privacy-compliant event collection; internal dashboards.

* Media/CDN: Image and asset delivery with caching.

* Optional School Integrations: CSV roster upload; basic SSO for institutions (phase 2+).

### Data Storage & Privacy

* Data Flow: Client → API Gateway → Services → Datastore; analytics via event stream to warehouse.

* Storage: Partitioned by region; encrypted at rest and in transit; role-based access control.

* Privacy:

  * KVKK/GDPR compliance-by-design; parental consent for minors.

  * Data minimization (no unnecessary PII); clear retention policies.

  * Right to access/delete; export user data; consent logs.

* Safety:

  * Content moderation for user-generated elements (usernames, flags).

  * COPPA-like safeguards for under-13s if applicable; conservative defaults for minors.

### Scalability & Performance

* Expected Load: 10–20k DAU initially; peak during evenings and weekends; seasonal spikes before exams.

* Horizontal scaling for stateless services; CDN for assets; caching for question delivery.

* Pre-warm adaptive queues; batch recommendations off-peak; graceful degradation offline.

### Potential Challenges

* Content Quality: Maintaining high-quality, exam-aligned items at scale.

* Cheating in Mocks: Balancing integrity with usability; avoid over-restrictive measures.

* Device Fragmentation: Ensuring smooth performance on low-end Android devices.

* Payment Complexity: Handling refunds, proration, and app store policies.

* Legal/Compliance: Age verification, consent, and data subject requests at scale.

---

## Milestones & Sequencing

### Project Estimate

* Medium: 2–4 weeks for MVP; +2–3 weeks for polish/beta; continuous iteration thereafter.

### Team Size & Composition

* Small Team: 2 total people

  * Product Designer/PM (hybrid): UX, content structure, analytics plan, QA.

  * Full-Stack Engineer: Mobile app, backend services, integrations, deployment.

### Suggested Phases

**Phase 1: Discovery & Prototype (1 week)**

* Key Deliverables: PM/Designer → clickable prototype; content taxonomy; top 200 question items; event schema.

* Dependencies: Access to initial content pool; exam format validation.

**Phase 2: MVP Build (2–3 weeks)**

* Key Deliverables: Engineer → core onboarding, quick practice, adaptive baseline, explanations, basic dashboard, offline cache (practice), payments (single plan), analytics events.

* Dependencies: Payment accounts; push/email setup; CDN.

**Phase 3: Beta & Polish (1–2 weeks)**

* Key Deliverables: Engineer → mock exams, streaks/badges, parental weekly summary, performance optimizations; PM/Designer → UX refinements, accessibility pass, content QA.

* Dependencies: Beta testers (students/teachers), app store listings.

**Phase 4: Launch & Learn (1 week)**

* Key Deliverables: Public release; onboarding A/B test; pricing test; school pilot playbook; support scripts.

* Dependencies: Marketing assets; partner schools/dershane.

---

## Developments & Improvements

* AI Tutor in Turkish: Context-aware hints, mistake analysis, and step-by-step guidance.

* Image/OCR Practice: Snap a textbook question; get similar items and solutions.

* Advanced Recommendations: Multi-armed bandits for content selection; goal-conditioned pacing.

* Teacher Tools: Assignment scheduling, item authoring templates, and rubric-based grading for open-ended items (phase 2+).

* Community Features: Safe, moderated Q&A with teacher-verified answers.

* Competitive Events: Weekend challenges; national mock exam days with real-time rankings.

* Personalization Enhancements: Stress and pacing coach; micro-break suggestions; wellness nudges.

* Content Expansion: YDT language packs; deeper subtopics; video explanations.

* Institutional Integrations: School dashboards, SIS imports, and bulk licensing.

* Security & Compliance: Automated consent renewal flows; data residency options for institutions.