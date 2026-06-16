## 🪲 BR001: Internal video streaming room fails to load on click

| Field | Details |
| :--- | :--- |
| **ID** | 001 |
| **Title** | Clicking "Розпочати заняття" triggers an endless loading spinner and fails to open internal online meeting room |
| **Preconditions** | Tutor is logged in, and a lesson slot is active right now. |
| **Steps** | 1. Open the active meeting dashboard.<br>2. Click the **"Розпочати заняття"** button. |
| **Postconditions** | The tutor and students cannot connect to the internal lesson room, completely blocking the learning process. |
| **Expected Result** | The system should launch the web-RTC/video stream UI and connect to the media server instantly. |
| **Actual Result** | The video room frame remains blank with an endless loading spinner. |
| **Severity / Priority** | 🔴 **Critical / High** |
| **Status** | 🔓 **OPEN (Unresolved)** |
| **Environment** | Google Chrome (v125.0), Localhost Web Environment |

---

## 🪲 BR002: Broken layout and missing buttons on mobile screens

| Field | Details |
| :--- | :--- |
| **ID** | 002 |
| **Title** | Core elements overlap and action buttons disappear when layout is compressed to mobile viewport resolution |
| **Preconditions** | User opens any dashboard page (Student or Tutor view). |
| **Steps** | 1. Change browser window resolution to 375x812 (Mobile View via DevTools).<br>2. Try to access the "Book Lesson" button. |
| **Postconditions** | Mobile users are unable to use the application because key control buttons are physically hidden or clipped. |
| **Expected Result** | The page grid shifts to a single-column block system, and buttons scale down proportionally to fit the screen. |
| **Actual Result** | The sidebar collides with the main block content. The "Book Lesson" button is pushed outside the screen boundary line (hidden behind the right edge), making it unclickable. |
| **Severity / Priority** | 🔴 **High / High** |
| **Status** | 🔓 **OPEN (Unresolved)** |
| **Environment** | Mobile Safari (iOS 17.5) & Chrome Mobile Emulator |

---

## 🪲 BR003:  Negative Price Accepted for Group Meeting (Boundary Case)

| Field | Details |
| :--- | :--- |
| **ID** | 003 |
| **Title** | Boundary value "-0.01" bypasses price validation and is accepted as valid meeting price |
| **Preconditions** | 1. Tutor is logged in.2. Group meeting creation form is open. |
| **Steps** | 1. Fill in all required meeting fields (date, time, topic).2. Enter "-0.01" in the Price field.3. Submit the form. |
| **Postconditions** | The user is billed an incorrect amount at checkout, leading to either financial loss or a broken payment flow. |
| **Expected Result** | TSystem rejects the value and returns validation error: "Price must be a positive number." |
| **Actual Result** | Form submits successfully. Meeting is created with price "-0.01 UAH" stored in the database. |
| **Severity / Priority** | 🟡 **Medium / Medium** |
| **Status** | 🔓 **OPEN (Unresolved)** |
| **Environment** | Google Chrome v125.0, Localhost |
