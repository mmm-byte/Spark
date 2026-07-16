# Spark Repair Estimator

## 1. Most interesting design/UX decision

I made the walkthrough flow card-based and swipe-driven instead of using a long form. That matches how the app is used in the field: an agent is standing in an empty house, moving room to room, and needs to make quick decisions without fighting the UI. The card layout keeps the current section visible, makes progress obvious, and keeps the interaction model simple on a phone.

## 2. What is fragile or broken

The biggest technical tradeoff is that the app is still a single-file demo built around browser storage and CDN-loaded libraries. That makes it easy to open and submit, but it also means large photo sets can run into browser storage limits and the app depends on the libraries being cached correctly for offline use. OCR is also helpful but not guaranteed, so serial number parsing should be treated as best effort rather than a hard dependency.

## 3. Creative addition

I added a few extras beyond the brief, but the one I think is most useful is the serial-number helper for equipment photos. Agents already take photos of HVAC units and water heaters, so trying to extract a serial number from those images saves time later and makes the walkthrough more actionable. I also added supporting tools like the compare view and contractor list so the app feels like something a real team could grow into.

## 4. What I would ship next with two more days

With more time, I would move photo storage out of `localStorage` into IndexedDB, harden the offline cache so it does not depend on remote CDN availability, and clean up the export flow so it can attach richer project metadata to the workbook. I would also spend more time on validation and edge cases for custom line items and room management.

## AI tools used

I used AI to help speed up implementation and cleanup, especially for layout polishing, code review, and repetitive wiring. I still reviewed the result manually and kept the final behavior centered on the contest brief rather than the tool output.
