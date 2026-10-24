# Typing Academy — Front-end prototype v1

This is the first runnable implementation of the agreed Typing Academy plan. It is a static website designed to work on GitHub Pages without a build step.

## Run it

- Open `index.html` in a modern desktop browser, or
- Upload `index.html` to the root of a GitHub Pages repository.

## Included in this prototype

- Dashboard, course map (15 levels / 90 primary lessons), practice, tests, progress, and settings views.
- Beginner lessons with no countdown timer (Levels 1–7); timed practice from Level 8 onward.
- Basic live typing feedback, on-screen color-coded keyboard, finger-name guide in English and Bengali, word/letter speech settings, and error tone.
- Results summary, local session history, CSV export, and progress stored in this browser.
- A mandatory 40-second Advanced Track notice before Level 11, with the Continue button disabled until the countdown finishes.
- Responsive layout for desktop and smaller screens.

## Important prototype limitations

- **Authentication is not implemented yet.** Login, Google sign-in, account creation, and password reset need a configured authentication provider.
- **Cloud sync is not implemented yet.** Progress is currently stored in this browser using localStorage and does not sync between devices.
- Lesson texts, scoring, mastery thresholds, adaptive weak-key drills, certification logic, and the hand illustrations are prototype-level and require the next implementation pass.
- Browser speech quality varies by device/browser. The prototype uses the built-in Web Speech API where available.
- A production scoring engine must compare the final submitted text with the target and separately track corrected errors and final-text errors. The current metrics are preliminary.
- The 40-second notice is a UI-level guard, not a security boundary; production logic should also enforce course prerequisites and notice acceptance in the app state.

## Next implementation phase

1. Confirm target GitHub repository and deploy this prototype.
2. Configure authentication and cloud database (Firebase is the proposed option).
3. Implement robust scoring, lesson mastery thresholds, unlock rules, and persistent advanced-notice acceptance.
4. Expand each of the 90 lessons with carefully sequenced content and tests.
5. Replace the simplified hand emoji with a flat illustrated hand guide whose finger colors match keyboard keys exactly.
