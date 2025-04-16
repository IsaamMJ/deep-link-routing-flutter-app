# 🚀 Flutter Deep Linking App (Clean Architecture + GetX)

A scalable Flutter application showcasing:

- 🔗 Deep Linking (manual + Firebase-ready)
- 🔐 Login gating before navigation
- 🗃️ Hive local data storage
- 🧠 Clean Architecture with Use Cases & Repositories
- ⚙️ GetX for state management and navigation

---

## 📦 Features

- 🌐 Deep Linking via `uni_links2` package
- ✅ Login check before allowing navigation
- 🛠️ Local persistence using Hive
- 📁 Scalable clean architecture (data → domain → presentation)
- 🧭 Dynamic routing (`/home`, `/api-data`, `/car/:id`)
- 🔄 Resume deep link navigation after login
- 🧪 Hive debug tool for inspecting stored data
- ☁️ Firebase Dynamic Links setup (in progress)

---

## 🧱 Folder Structure (Clean Architecture)

```
lib/
├── core/                  # Core services (deep linking, nav, etc.)
├── controller/            # GetX controllers (Home, Detail, etc.)
├── data/
│   ├── models/            # Hive model classes
│   ├── datasources/       # Local storage (Hive, SharedPrefs)
│   └── repositories/      # Data layer logic
├── domain/
│   └── usecases/          # Business logic (add car, check login, etc.)
├── presentation/
│   ├── pages/             # UI screens (Home, API, Detail)
│   └── bindings/          # GetX bindings
├── routes/                # App routes and page configs
└── main.dart              # App entry point
```

---

## 🚀 Getting Started

### 🔧 Prerequisites

- Flutter 3.x
- Dart 3.x
- Hive & SharedPreferences
- Firebase (optional, for dynamic links)

### 🛠️ Setup

```bash
git clone https://github.com/your-username/flutter-deep-linking-clean-architecture.git
cd flutter-deep-linking-clean-architecture
flutter pub get
flutter run
```

---

## 🔗 Deep Linking Flow

1. User taps a deep link (e.g., `myapp://car/123`)
2. `DeepLinkService` checks login status
3. If not logged in → stores path and redirects to login
4. After login → resumes stored path
5. Navigates to `/car/123` via GetX routing

---

## 🔗 Supported Routes

| Deep Link | Behavior |
|-----------|----------|
| `myapp://home`         | Navigates to Home tab          |
| `myapp://api-data`     | Navigates to API Data tab      |
| `myapp://car/:id`      | Opens Car Detail page by ID    |
| `https://yourapp.page.link/car/:id` | (Firebase-ready link) |

---

## 🔧 Tech Stack

- **Flutter** (UI framework)
- **GetX** (State management & routing)
- **Hive** (Local storage)
- **SharedPreferences** (Auth state)
- **uni_links2** (Manual deep linking)
- **Firebase Dynamic Links** *(optional)*

---

## 🧪 Debug Tools

- `HiveDebugService` lets you print stored cars from Hive.
- FAB on Home tab allows quick car entry for testing.

---


### Made with 💙 by [Mohamed Isaam]
```
