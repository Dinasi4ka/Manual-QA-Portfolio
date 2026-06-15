## 📋 001: User Profile Custom Data Update

| Field | Details |
| :--- | :--- |
| **ID** | 001 |
| **Title** | Verify successful update of custom profile fields (`about` and `google_drive_link`) via REST API |
| **Preconditions** | User is successfully authenticated in the system, and a valid active session or JWT token is provided. |
| **Steps** | 1. Send a `PATCH` request to the user profile update endpoint (e.g., `/api/v1/users/profile/`).<br>2. Include the following JSON payload.<br>3. Analyze the HTTP response status code and response body. |
| **Expected Result** | 1. Server returns HTTP status code `200 OK`.<br>2. Database record for the user updates successfully.<br>3. Response body JSON contains the modified values for both `about` and `google_drive_link` fields. |

---

## 📋 002: Internal Online Meeting Launch Failure

| Field | Details |
| :--- | :--- |
| **ID** | 002 |
| **Title** | Verify the ability of a Tutor to launch and conduct an internal video-trow meeting inside the platform |
| **Preconditions** | 1. Tutor is successfully authorized on the platform.<br>2. A group or individual meeting is scheduled for the current time slot. |
| **Steps** | 1. Navigate to the "My Schedule" page.<br>2. Click on the active meeting card.<br>3. Click the **"Розпочати заняття (Start Lesson)"** button to launch the built-in video player/room interface. |
| **Expected Result** | 1. The platform initializes the internal video/audio room without redirects.<br>2. Camera and microphone permissions are requested by the browser.<br>3. The Tutor successfully enters the live session space, and a unique stream link is activated for students. |

---

## 📋 003: Mobile Responsive Layout Validation (UI/UX)

| Field | Details |
| :--- | :--- |
| **ID** | 003 |
| **Title** | Verify web platform layout responsiveness and elements visibility on mobile screen resolutions |
| **Preconditions** | User opens the platform landing/login page using a desktop browser (e.g., Google Chrome). |
| **Steps** | 1. Right-click anywhere on the page and select **Inspect (Дослідити)** to open Chrome DevTools.<br>2. Click the **Toggle Device Toolbar** icon (or press `Ctrl+Shift+M`).<br>3. Set the device viewport dimension to a smartphone view (e.g., iPhone 14 or Samsung Galaxy S22 - screen width ~390px).<br>4. Attempt to interact with the main navigation menu and dashboard elements. |
| **Expected Result** | 1. The desktop sidebar navigation collapses into a responsive "hamburger" mobile menu button.<br>2. All text elements, math formulas, and buttons adapt smoothly to the screen width without overlapping.<br>3. No horizontal scrolling is required to read content or press action items. |
