# List of Bot Commands

> `/` is the default command prefix.

| Command | Description | State Flow |
|---------|-------------|------------|
| `login` | Start authentication process | `WAITING_FOR_ACCESS_CODE` → `AUTHORIZED` |
| `logout` | Clear session and deactivate | Clears Redis session |
| `info` | Display user profile information | Reads from Redis session |
| `report_income` | Record income for a period | `WAITING_FOR_PERIOD` → `WAITING_FOR_INCOME` |

> [!NOTE]
> All commands except `/login` require prior user authorization.

---

# Notification System

> The bot includes an automated notification system that sends periodic updates and greetings to users.

| Type | Frequency | Trigger |
|------|-----------|---------|
| **Monthly Payment Reminders** | Monthly (days 1-3) | `now.day in 1-3` |
| **Birthday Greetings** | Daily check | User's birth date |
| **Holiday Greetings** | Daily check | Holiday calendar |

> [!NOTE]
> The notification system runs independently of bot commands and continues sending messages even when users aren't interacting with the bot.