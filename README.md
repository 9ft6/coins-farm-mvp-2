# About the Project
[Русская версия](https://t.me/CoinsFarmDevChat)

Author tg: [@dev9ft6](https://t.me/dev9ft6)

Developer tg chat: [CoinsFarmDevChat](https://t.me/CoinsFarmDevChat)

## Summary
This project is a private solution developed over four months and has reached 
its current stage of completion. It is currently being tested on 5000 Telegram 
accounts for four games: **Blum**, **Cats**, **HamsterKombat**, and 
**NotPixel**. Development is ongoing, and work has started on MVP-3, which is 
expected to take around 3-4 months. The current goal is to complete this phase 
by January-February 2025, with a public version planned for those who wish to 
try the project.

### Entities
### Accounts
- Account import via drag-and-drop in the browser in any format: TData, session, JSON.
- Validation of incoming data with tracking.
- Exclusive access to accounts is managed through a custom controller that monitors all account actions and applies a safe timeout to each action, preventing bans.
- A random mobile device with a unique, realistic synthetic fingerprint is generated for each account upon import, and this device will be used consistently.
- Each account is linked to a proxy from a proxy pool (proxyverse) with the necessary geolocation, and all actions on the account are carried out with this geo.
- Ability to generate TON wallets of different versions in various ways for further manipulations.
- Various applications can be registered on each account, and tasks can be launched.
- Stores application authentication data.
- Stores application usage statistics.

### Application
- Applications represent a group of tasks grouped by affiliation with a specific app, such as **Blum**, **Cats**, **HamsterKombat**, or **NotPixel**.
- Each application has its own task runner — a separate microservice that starts and stops tasks for its application.

### Task
- A task is an algorithm of actions performed for a specific account and application.
- Task parameters are configured at launch.
- The task reports its status to the system in real time.
- Can be managed or adjust its behavior during execution centrally.
- Has a notification system and lifecycle management.
- Can delay its execution depending on conditions.
- Can be created by other tasks, which is convenient for building complex referral trees.

![Tasks Interface](https://github.com/9ft6/coins-farm-mvp-2/raw/media/pics/pic1.png)

![Task List Interface](https://github.com/9ft6/coins-farm-mvp-2/raw/media/pics/pic2.png)

![Applications Interface](https://github.com/9ft6/coins-farm-mvp-2/raw/media/pics/pic3.png)
