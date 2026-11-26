# CleanTrack: Barangay Waste Collection Tracker

## Project overview
CleanTrack is a small, single-page web app for recording missed garbage collection in a community. A resident enters an area, the date of the missed collection, and a short description. The app saves and displays reports in the same browser using `localStorage`.

**Project scope:** This is a local recordkeeping prototype. It does not send reports to barangay officials, synchronize between devices, or provide a shared community database.

## Project pitch
CleanTrack gives residents a simple way to keep an organized record of missed garbage collection. Instead of relying on memory or scattered notes, users can save and review collection concerns in one browser page.

## Community problem
Some households experience missed or delayed garbage collection. Residents might not keep a consistent record of when and where collection was missed. A small digital log offers a practical way to record these events.

This project is a proposed student prototype. The existence and frequency of missed pickups in a specific barangay should be confirmed through a short community interview or observation before making local claims.

## Target users
- Residents who want to record missed garbage collection.
- Student developers demonstrating a localStorage-based community web app.

## Main feature
Create, view, and delete missed-collection reports. Each report contains:
- Street or area
- Date of missed collection
- Short description

## FR-01: Missed Collection Report Record

| Field | Requirement |
|---|---|
| Requirement ID | FR-01 |
| Requirement title | Save a missed garbage collection report |
| Description | The app shall let a resident enter an area, a date, and a description, then save the report in browser localStorage. |
| Purpose | Provide a simple local record of missed garbage collection concerns. |
| Target users | Residents using the same browser and device where the report was saved. |
| Functional requirements | FR-01.1 Validate all required fields. FR-01.2 Require an area name of at least 3 characters. FR-01.3 Require a description of at least 5 characters. FR-01.4 Save valid reports in localStorage. FR-01.5 Display saved reports after page load and refresh. FR-01.6 Allow a user to delete a saved report. FR-01.7 Show success or error feedback. |
| Non-functional requirements | NFR-01: Use one HTML page with embedded CSS and JavaScript. NFR-02: Work in a modern browser with localStorage enabled. NFR-03: Adapt to desktop and mobile screens. NFR-04: Use readable labels and keyboard-accessible controls. NFR-05: Do not transmit report data to a server. |
| Expected outcome | Users save and review missed-collection reports in their own browser. |
| Acceptance criteria | A valid report appears in the list. Empty or too-short entries are rejected with a message. Saved entries remain after refresh in the same browser. Deleting an entry removes it from the list and storage. The layout remains usable on narrow screens. |

## System architecture
The app uses a simple client-side structure:

1. HTML provides the form and report list.
2. CSS styles the page and adapts the layout for smaller screens.
3. JavaScript validates form input, updates the report list, and handles deletion.
4. `localStorage` stores a JSON array under the key `cleantrack_reports_v1`.

No backend, external API, database server, or framework is used.

## Technologies
- HTML5
- CSS3
- Vanilla JavaScript
- Browser localStorage
- Git and GitHub for version control and hosting the project source

## Installation and running
1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Add a report using the form.

No package installation or build command is required. For a local development server, run `python -m http.server 8000` in the project folder and visit `http://localhost:8000`.

## How to use
1. Enter the street or area.
2. Select the date when collection was missed.
3. Describe the concern in at least five characters.
4. Select **Save report**.
5. Review the report under **Saved reports**.
6. Select **Delete** to remove a report.

## Screenshots
Add screenshots of the running app here before submission. Suggested files:
- `screenshots/desktop.png`
- `screenshots/mobile.png`

## Instructor demonstration steps 1–14
The activity screenshot supplied for this project lists the overall deliverables, but it does not include the instructor's demonstration steps 1–14. Those steps were not provided with the materials available for this task. Do not treat this project guide as a replacement for the instructor's exact sequence. Add the original steps here and follow them in order once the instructor's demo handout or screenshots are available.

## Limitations
- Data stays in the current browser profile on the current device.
- Clearing browser site data removes saved reports.
- Reports are not sent to barangay officials.
- There is no login, shared database, or multi-user synchronization.

## License
For classroom use. Add a license if your instructor requires one.
