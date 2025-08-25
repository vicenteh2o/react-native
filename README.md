## Arquitectura: feature-based con capas de Clean Architecture.

app/
├── (tabs)/
│ ├── home/
│ │ └── index.js
│ ├── profile/
│ │ └── index.js
│ └── settings/
│ └── index.js
│
│── \_layout.js // Configuración de Tabs y redireccion inicial
│
├── auth/
│ ├── login.js
│ └── register.js
│
|
├── shared/ // Cosas compartidas entre features
│ ├── components/ // Botones, inputs, modales reutilizables
│ ├── hooks/ // hooks comunes
│ └── services/ // AuthService, etc.
│
├── store/ // Estado global (Zustand, Redux, React context, etc.)
|
└── utils/ // Helpers/utilidades
├── features/ // Cada módulo aislado (Feature-Based + Clean)
│ ├── home/
│ │ ├── components/ // UI específica del feature
│ │ └── hooks/ // UI lógica: hooks, viewmodels
│ │ ├── service/ // UI específica del feature
│ │ └── screens/ // Pantallas (pueden mapear a app/(tabs))
│ │
│ ├── auth/
│ │ ├── components/ // UI específica del feature
│ │ └── hooks/ // UI lógica: hooks, viewmodels
│ │ ├── service/ // UI específica del feature
│ │ └── screens/ // Pantallas (pueden mapear a app/(tabs))
│ │
│ ├── profile/
│ │ ├── components/ // UI específica del feature
│ │ └── hooks/ // UI lógica: hooks, viewmodels
│ │ ├── service/ // UI específica del feature
│ │ └── screens/ // Pantallas (pueden mapear a app/(tabs))

## Levantar proyecto

1. Install dependencies

   ```bash
   npm install
   ```

2. Start the app

   ```bash
   npx expo start
   ```

In the output, you'll find options to open the app in a

- [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go), a limited sandbox for trying out app development with Expo
