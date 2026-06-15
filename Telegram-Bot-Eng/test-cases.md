## 📋 001: Subscription Tariff Purchase Flow

| Field | Details |
| :--- | :--- |
| **ID** | 001 |
| **Title** | Verify successful transition to external payment gateway when purchasing a lesson package |
| **Preconditions** | 1. User is registered and authorized in the bot.<br>2. User is on the bot's Main Menu screen. |
| **Steps** | 1. Click the menu button **"Придбати заняття"**.<br>2. Select a specific lesson package from the list (e.g., "Standard: 8 Lessons").<br>3. Review the displayed package information and price.<br>4. Click the **"Оплатити"** button. |
| **Expected Result** | 1. Clicking "Придбати заняття" displays inline buttons with all available lesson packages.<br>2. Selecting a package displays a message with its full description, number of lessons, and accurate cost.<br>3. Clicking "Оплатити" generates and opens a valid external web link to the payment gateway page. |

---

## 📋 002: Lesson Cancellation Flow by Student

| Field | Details |
| :--- | :--- |
| **ID** | 002 |
| **Title** | Verify lesson cancellation flow, terms display, and redirect to tutor communication |
| **Preconditions** | 1. User is registered as a Student.<br>2. Student has at least one active booked lesson in their schedule. |
| **Steps** | 1. Open the bot menu and navigate to the active bookings/lessons section.<br>2. Click the **"Скасувати заняття"** button next to the booked lesson.<br>3. Review the displayed cancellation terms and instructions.<br>4. Click the **"Написати викладачу"** inline button.<br>5. Enter the required text input: date, time of the lesson, and the reason for cancellation. |
| **Expected Result** | 1. Clicking "Скасувати заняття" triggers a message detailing the cancellation policy (e.g., refund rules, 24-hour notice policy).<br>2. The **"Написати викладачу"** button generates a valid internal Telegram link/action that opens a direct chat window with the assigned tutor to send the cancellation details. |
