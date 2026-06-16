## 📋 TC001: User Profile Custom Data Update

| Field | Details |
| :--- | :--- |
| **ID** | 001 |
| **Title** | Verify successful update of custom profile fields (`about` and `google_drive_link`) via REST API |
| **Preconditions** | User is successfully authenticated in the system, and a valid active session or JWT token is provided. |
| **Steps** | 1. Send a `PATCH` request to the user profile update endpoint (e.g., `/api/v1/users/profile/`).<br>2. Include the following JSON payload.<br>3. Analyze the HTTP response status code and response body. |
| **Expected Result** | 1. Server returns HTTP status code `200 OK`.<br>2. Database record for the user updates successfully.<br>3. Response body JSON contains the modified values for both `about` and `google_drive_link` fields. |

---

## 📋 TC002: Internal Online Meeting Launch Failure

| Field | Details |
| :--- | :--- |
| **ID** | 002 |
| **Title** | Verify the ability of a Tutor to launch and conduct an internal video-trow meeting inside the platform |
| **Preconditions** | 1. Tutor is successfully authorized on the platform.<br>2. A group or individual meeting is scheduled for the current time slot. |
| **Steps** | 1. Navigate to the "My Schedule" page.<br>2. Click on the active meeting card.<br>3. Click the **"Розпочати заняття (Start Lesson)"** button to launch the built-in video player/room interface. |
| **Expected Result** | 1. The platform initializes the internal video/audio room without redirects.<br>2. Camera and microphone permissions are requested by the browser.<br>3. The Tutor successfully enters the live session space, and a unique stream link is activated for students. |

---

## 📋 TC003: Mobile Responsive Layout Validation (UI/UX)

| Field | Details |
| :--- | :--- |
| **ID** | 003 |
| **Title** | Verify web platform layout responsiveness and elements visibility on mobile screen resolutions |
| **Preconditions** | User opens the platform landing/login page using a desktop browser (e.g., Google Chrome). |
| **Steps** | 1. Right-click anywhere on the page and select **Inspect (Дослідити)** to open Chrome DevTools.<br>2. Click the **Toggle Device Toolbar** icon (or press `Ctrl+Shift+M`).<br>3. Set the device viewport dimension to a smartphone view (e.g., iPhone 14 or Samsung Galaxy S22 - screen width ~390px).<br>4. Attempt to interact with the main navigation menu and dashboard elements. |
| **Expected Result** | 1. The desktop sidebar navigation collapses into a responsive "hamburger" mobile menu button.<br>2. All text elements, math formulas, and buttons adapt smoothly to the screen width without overlapping.<br>3. No horizontal scrolling is required to read content or press action items. |

---

## 📋 TC004: YouTube Video Playback in Self-Study Module

| Field | Details |
| :--- | :--- |
| **ID** | 004 |
| **Title** | Verify that YouTube-embedded videos load and play correctly within the self-study topic page |
| **Preconditions** | 1. Student is logged in.<br>2. At least one topic with an embedded YouTube video exists. |
| **Steps** | 1. Navigate to the self-study section.<br>2. Select any available math topic.<br>3. Click on a video lesson from the topic list.<br>4. Press Play on the embedded video player. |
| **Expected Result** | 1. Video player loads within the page without redirecting to YouTube.<br>2. Video begins playback within 3 seconds.<br>3. Player controls (pause, volume, fullscreen) are functional.<br>4. Page layout does not break during video playback. |

---

## 📋 TC005: Tutor Booking — Conflict Prevention

| Field | Details |
| :--- | :--- |
| **ID** | 005 |
| **Title** | Verify that a student cannot book a tutor time slot already reserved by another student |
| **Preconditions** | 1. Two student accounts exist (Student A and Student B).<br>2. Tutor has one available slot at 15:00.<br>3. Student A has already booked the 15:00 slot. |
| **Steps** | 1. Log in as Student B.<br>2. Navigate to the tutor's profile and open schedule.<br>3. Attempt to book the same 15:00 slot. |
| **Expected Result** | 1. The 15:00 slot is displayed as unavailable or greyed out.<br>2. System returns an error: "This time slot is already booked."<br>3. Student B is prompted to choose a different time.<br>4. Student A's booking remains unaffected |
