# CareBridge — Low-Bandwidth Telemedicine Web Application

A multi-page, responsive healthcare web-app prototype combining a modern patient portal experience with a clean clinical consultation workspace.

## Run locally
1. Extract the ZIP archive.
2. Open `index.html` in a modern browser (Chrome, Edge, Firefox, Safari).
3. No Node.js, build tools, or package installation are required.

## Application pages
- Overview dashboard
- Consultation room
- Medical records
- Messages
- Patient profile
- Settings

## Core project demonstration
- Adaptive consultation UI: video (55–100), audio (25–54), text (0–24) using the network quality slider.
- Chat/transcript remains visible through mode changes.
- Structured clinical note capture: complaint, history, temperature, blood pressure, assessment, and plan.
- Save notes in browser session storage.
- Export the visit record and conversation as JSON.
- Responsive layout with desktop sidebar and mobile navigation.
- Sample document previews, patient profile and preferences.

## Files
- `index.html` — app shell and all page views
- `styles.css` — responsive design system
- `app.js` — navigation, adaptive mode simulation, chat, notes and export

## Important limitations
This is a **front-end prototype**, not a production telemedicine platform. The bandwidth slider simulates connection quality. It does not establish a real WebRTC video/audio call, connect a real doctor, capture actual microphone/camera media, or synchronize data with a server. Patient information and records are sample/demo content; session storage is local to the browser tab/session. Do not enter real patient-identifiable or sensitive health information.

## Production implementation checklist
- Secure backend, user authentication, role-based authorization, clinician verification
- WebRTC signaling and media transport with STUN/TURN, adaptive bitrate, measured packet loss/jitter/RTT and tested fallback thresholds
- Reliable offline message queue, durable local outbox, message IDs, acknowledgements, retry and conflict resolution
- Encrypted data in transit and at rest, consent, audit trails, retention/deletion controls
- Clinician review/signature workflow and standards-based EHR integration (e.g. FHIR) after clinical and privacy review
- Emergency escalation pathway, accessibility review, clinical safety testing and jurisdiction-specific compliance
