| ID | Step Name (Verification Point) | Status |
| :--- | :--- | :--- |
| 001 | Verify user registration in the database upon sending the `/start` command | 🟢 PASSED |
| 002 | Verify that sending `/start` again recognizes existing user and avoids duplication | 🟢 PASSED |
| 003 | Verify that the `/help` command returns a valid list of active options and support links | 🔴 FAILED |
| 004 | Verify bot fallback behavior when receiving invalid text inputs or unknown commands | 🟢 PASSED |
| 005 | Verify that the `Мій баланс` command correctly displays all available lesson packages | 🟢 PASSED |
| 006 | Verify that updating tariff pricing in the MySQL backend instantly syncs with the bot UI | 🔴 FAILED |
| 007 | Verify that clicking the `Оплатити` inline button generates a valid checkout invoice card | 🟢 PASSED |
| 008 | Verify successful test payment simulation and instant credit reflection on user balance | 🟢 PASSED |
| 009 | Verify input field validation for custom top-up amounts (reject negative values and letters) | 🔴 FAILED |
| 010 | Verify that the `Мій розклад` menu displays only active slots | 🟢 PASSED |
| 011 | Verify that a successfully booked lesson automatically decrements 1 credit from the user's balance | 🟢 PASSED |
| 012 | Verify booking cancellation policy restrictions | 🟢 PASSED |
