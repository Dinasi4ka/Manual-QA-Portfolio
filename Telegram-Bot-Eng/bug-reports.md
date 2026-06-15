## 🪲 001: Missing "/help" command and menu action

| Field | Details |
| :--- | :--- |
| **ID** | 001 |
| **Title** | Missing "/help" command button and lack of response in the Main Menu interface |
| **Preconditions** | User has launched the bot and is currently on the Main Menu screen. |
| **Steps** | 1. Review the available text commands and inline menu buttons in the chat interface.<br>2. Try to manually type and send the command `/help`. |
| **Postconditions** | User cannot access customer support, instructions, or the list of active commands. |
| **Expected Result** | 1. The Main Menu should contain a visible button for support/help.<br>2. Sending the `/help` command should return an automated message with a list of active options and support links. |
| **Actual Result** | 1. There is no button for "Help" or "Support" in the menu.<br>2. Typing `/help` manually returns no response from the bot, causing a dead-end in the user experience. |
| **Severity / Priority** | 🟡 **Medium / Medium** |
| **Status** | 🔓 **OPEN (Unresolved)** |
| **Environment** | Telegram Mobile App (v10.12, IOS 17 ) & Telegram Desktop (v5.1, Windows 11) |

---

## 🪲 002: Data mismatch after manual configuration update

| Field | Details |
| :--- | :--- |
| **ID** | 002 |
| **Title** | Data mismatch between button label and external payment link after manual price update |
| **Preconditions** | Admin has manually changed the package price info and updated the payment hyperlink for the "Individual Package" directly in the bot configurations. |
| **Steps** | 1. Click the menu button **"Придбати заняття"**.<br>2. Select the **"Individual Package"** button (which was updated to display the new price: 500 UAH).<br>3. Review the pricing details message.<br>4. Click the **"Оплатити"** button and redirect to the external payment page. |
| **Postconditions** | The user is billed an incorrect amount at checkout, leading to either financial loss or a broken payment flow. |
| **Expected Result** | The price displayed on the bot's button (500 UAH), the description text, and the actual amount requested on the external payment gateway link must be completely synchronized. |
| **Actual Result** | While the button name successfully displays `Individual - 500 UAH`, the underlying manual payment link was not mapped correctly and redirects to the old checkout page requesting the old price of `450 UAH`. |
| **Severity / Priority** | 🔴 **High / High** |
| **Status** | 🔓 **OPEN (Unresolved)** |
| **Environment** | Production Bot Environment / External Payment Gateway Interface |
