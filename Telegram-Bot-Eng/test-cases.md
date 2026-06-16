## 📋 TC001: Subscription Tariff Purchase Flow

| Field | Details |
| :--- | :--- |
| **ID** | 001 |
| **Title** | Verify successful transition to external payment gateway when purchasing a lesson package |
| **Preconditions** | 1. User is registered and authorized in the bot.<br>2. User is on the bot's Main Menu screen. |
| **Steps** | 1. Click the menu button **"Придбати заняття"**.<br>2. Select a specific lesson package from the list (e.g., "Standard: 8 Lessons").<br>3. Review the displayed package information and price.<br>4. Click the **"Оплатити"** button. |
| **Expected Result** | 1. Clicking "Придбати заняття" displays inline buttons with all available lesson packages.<br>2. Selecting a package displays a message with its full description, number of lessons, and accurate cost.<br>3. Clicking "Оплатити" generates and opens a valid external web link to the payment gateway page. |

---

## 📋 TC002: Lesson Cancellation Flow by Student

| Field | Details |
| :--- | :--- |
| **ID** | 002 |
| **Title** | Verify lesson cancellation flow, terms display, and redirect to tutor communication |
| **Preconditions** | 1. User is registered as a Student.<br>2. Student has at least one active booked lesson in their schedule. |
| **Steps** | 1. Open the bot menu and navigate to the active bookings/lessons section.<br>2. Click the **"Скасувати заняття"** button next to the booked lesson.<br>3. Review the displayed cancellation terms and instructions.<br>4. Click the **"Написати викладачу"** inline button.<br>5. Enter the required text input: date, time of the lesson, and the reason for cancellation. |
| **Expected Result** | 1. Clicking "Скасувати заняття" triggers a message detailing the cancellation policy (e.g., refund rules, 24-hour notice policy).<br>2. The **"Написати викладачу"** button generates a valid internal Telegram link/action that opens a direct chat window with the assigned tutor to send the cancellation details. |

---

## 📋 TC003: Unregistered Phone Number

| Field | Details |
| :--- | :--- |
| **ID** | 003 |
| **Title** | Verify that a user with an unregistered phone number is denied access to main functionality |
| **Preconditions** | 1. Bot is running.<br>2. Phone number is NOT present in the Google Sheets database. |
| **Steps** | 1. Send /start command to the bot.<br>2. Enter a phone number not registered in the system. |
| **Expected Result** | 1. Bot returns an error or informational message indicating the number is not recognized.<br>2. User is NOT granted access to the main menu.<br>3. Bot suggests contacting the tutor to register. |

---

## 📋 TC004: Balance Display After Package Purchase

| Field | Details |
| :--- | :--- |
| **ID** | 004 |
| **Title** | Verify that lesson balance updates correctly after a successful package purchase |
| **Preconditions** | 1. User is registered and authorized.<br>2. User's current balance is 0 lessons.<br>3. A valid payment method is available. |
| **Steps** | 1. Navigate to "Придбати заняття".<br>2. Select any available package (e.g., Standard: 8 Lessons).<br>3. Click "Оплатити" and complete the payment flow.<br>4. Return to the main menu and open "Мій баланс". |
| **Expected Result** | 1. Balance section displays the correct number of purchased lessons (e.g., 8).<br>2. Package name and expiry date (if applicable) are shown accurately.<br>3. No duplicate credits are added on page refresh. |

---

## 📋 TC005: Lesson Rescheduling Under Policy Restrictions

| Field | Details |
| :--- | :--- |
| **ID** | 005 |
| **Title** |Verify that lesson rescheduling is blocked when cancellation policy conditions are not met |
| **Preconditions** | 1. User has an active booked lesson scheduled within the next 1 hours (inside restriction window). |
| **Steps** | 1. Open "Мій розклад".<br>2. Select the upcoming lesson within the restriction window.<br>3. Attempt to click "Перенести заняття". |
| **Expected Result** | 1. System displays a policy warning message explaining the restriction (e.g., "Reschedule not allowed less than 1 hours before lesson").<br>2. "Написати викладачу" option remains available as an alternative. |
