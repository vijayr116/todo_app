# ✅ Todo App – Offline First Notes Application

_"Create, update, and delete notes while offline, then automatically sync them with a Mock REST API when connectivity is restored."_

---

| Feature                  | Detail                                                     |
| ------------------------ | ---------------------------------------------------------- |
| **Offline storage**      | `sqflite` (SQLite)                                         |
| **Remote API**           | Mock REST API (JSON Server / MockAPI)                      |
| **Connectivity watcher** | `connectivity_plus`                                        |
| **Automatic sync**       | Queues offline operations and syncs when online            |
| **Conflict resolution**  | Detects local vs remote conflicts and lets the user choose |
| **State management**     | `flutter_bloc` + `equatable`                               |
| **Routing**              | `go_router`                                                |
| **Dependency Injection** | `get_it`                                                   |

---

## 🏗️ Folder Structure

```text
lib/
├── src/
│   ├── app/
│   ├── common/
│   │   ├── constants/
│   │   ├── services/
│   │   ├── repos/
│   │   └── services_locator.dart
│   └── notes/
│       ├── bloc/
│       ├── repo/
│       ├── models/
│       └── views/
└── main.dart
```

## ✨ Features

- Create Notes
- Edit Notes
- Delete Notes
- Offline-first architecture
- Automatic synchronization
- Pending sync queue
- Connectivity monitoring
- Conflict detection
- Conflict resolution dialog
- Sync status indicators
