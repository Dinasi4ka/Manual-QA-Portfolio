| ID | Step Name (Verification Point) | Status |
| :--- | :--- | :--- |
| **001** | Verify new user registration with unique email and secure password hashing | 🟢 PASSED |
| **002** | Verify user profile update functionality (saving `about` text and `google_drive_link`) | 🟢 PASSED |
| **003** | Verify User Access Control and data isolation based on roles (Student, Tutor, Admin) | 🟢 PASSED |
| **004** | Verify creation of an individual meeting (`StudentMeetings`) with specific hour blocks | 🔴 FAILED  |
| **005** | Verify creation of a group meeting (`TutorGroupMeetings`) with date, time, and price fields | 🟢 PASSED |
| **006** | Verify validation logic for meeting prices (system must reject negative pricing values) | 🟢 PASSED |
| **007** | Verify schedule conflict detection when booking overlapping tutor time slots | 🟢 PASSED |

