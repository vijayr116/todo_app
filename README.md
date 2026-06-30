# ✅ Todo‑App – Offline Flutter + Firebase

_“Create, update, todos while offline, then sync seamlessly when the network returns.”_

---

| ✨ Feature               | Detail                                                                       |
| ------------------------ | ---------------------------------------------------------------------------- |
| **Offline storage**      | `sqflite` (SQLite 3) as the local cache.                                     |
| **Realtime cloud sync**  | `cloud_firestore` + `firebase_auth` (anonymous).                             |
| **Connectivity watcher** | `connectivity_plus` – queues changes when offline, flushes when back online. |
| **State management**     | `flutter_bloc`, `equatable`, optimistic UI.                                  |
| **Routing**              | `go_router` (same pattern as dynamic_form).                                  |
| **DI**                   | `get_it`.                                                                    |

---

## 🏗️ Folder structure (condensed)

lib/
├─ firebase_options.dart ← auto‑gen (FlutterFire CLI)
├─ src/
│ ├─ app/ ← MaterialApp, GoRouter
│ ├─ common/ ← constants • utils • services_locator.dart
│ │ └─ repos/ ← ApiRepository, PreferencesRepository
│ └─ todo/
│ ├─ bloc/ ← TodoBloc (events, states)
│ ├─ repo/
│ │ ├─ todo_repository.dart ← orchestrates sync
│ │ └─ todo_database_repository.dart ← sqflite CRUD
│ └─ views/
│ ├─ todo_page.dart ← platform switch
│ ├─ mobile/… ← UI widgets
│ └─ todo_page_placeholder.dart ← will add desktop/tablet later
└─ main.dart ← Firebase.init + DI + runApp

## 🔧 Setup



1. **Clone & get packages**

   ```bash
   git clone https://github.com/arulmani70/todo-app.git
   cd todo-app
   flutter pub get

   firebase login
   firebase projects:create todo-app
   flutterfire configure               # generates firebase_options.dart
   ```
