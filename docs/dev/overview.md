# Overview

## Installation

```shell-session
<!-- Install package -->
yarn install

<!-- Run client -->
npm run dev:client

<!-- Run server -->
npm run dev:server
```

## Old Structure

```bash
PMP/
└── src/
    ├── assets/
        # images, styles, fonts, ...
        # move to @/assets
    ├── BAS/
        # item use BAS will be imported from components
        # move to @/features/BAS
    ├── components/
        # Rewrite all component to new structure.
        # If dumb component, move to @/components. Else, move to features
    ├── constant/
        # move to @/constants
    ├── containers/
    ├── Core/
        # If dumb component, move to @/components. Else, move to features
    ├── enum/
        # move to @/constants
    ├── features/                       # keep as current
    ├── GK/
        # move to @/features/BAS
    ├── hooks/
        # move to @/hooks
    ├── interfaces/
        # move to @/interfaces
    ├── items/                          # keep as current
    ├── json/
    ├── layouts/
    ├── lib/
        # move to @/features/
    ├── OAP/
        # move to @/features/OAP
    ├── pages/                          # keep as current
    ├── store/
        # move to @/store
    ├── stories-examples/
        # move to @/stories
    ├── temp/
        # move to @/features
    ├── utils/
        # move to @/utils
    ├── App.tsx                         # keep as current
    ├── env.ts                          # keep as current
    ├── i18n.ts                         # keep as current
    ├── index.scss                      # keep as current
    ├── index.tsx                       # keep as current
    ├── LegacyAppProvider.js            # keep as current
    ├── PMP.js                          # keep as current
    ├── react-app-env.d.ts              # keep as current
    ├── reportWebVitals.ts              # keep as current
    └── setupTests.ts                   # keep as current
```

## New Structure (WIP)

```bash
PMP/
└── src/
    ├── items/
        # Store all items need to add in process view. Can keep as current structure (bas, basic, ...). Consider to remove assets from here
    ├── pages/
        # Pages view by url.
        # For example:
        #   - /search -> Search page - search.tsx
        #   - /search/:id -> Search detail page - search/[id].tsx
        # Reference https://nextjs.org/docs/routing/introduction
    ├── @
        # Each features already have its own folder. Only add common things here
        ├── hooks/          # Store all hooks
        ├── constants/      # Store all constants
        ├── services/       # Store all services
        ├── utils/          # Store all utils
        ├── interfaces/     # Store all interfaces
        ├── styles/         # Store all styles
        ├── assets/         # Store all assets (images, fonts, ...)
        ├── components/     # Store all components. Components is dump component. Use to custom library or own dumb component
        ├── store/          # Store all store
        ├── stories/        # Store all stories
    ├── features/
        # Store all features
        # Each component will contain all of its related files (scss, utils, constants, types, ...)
        # For example:
        # ├── alarm/
        #     ├── AlarmList.tsx
        #     ├── AlarmList.scss
        #     ├── AlarmList.utils.ts
        #     ├── AlarmList.constants.ts
        #     ├── AlarmList.types.ts
        #     ├── AlarmList2.tsx
        #     ├── AlarmList3.tsx
        #     ├── alarmDetail/
        #         ├── AlarmDetail.tsx
        #         ├── AlarmDetail.constants.ts
        #         ├── AlarmDetail.scss
        #         ├── AlarmDetail.test.tsx
    ├── App.tsx
    ├── env.ts
    ├── i18n.ts
    ├── index.scss
    ├── index.tsx
    ├── LegacyAppProvider.js
    ├── PMP.js
    ├── react-app-env.d.ts
    ├── reportWebVitals.ts
    └── setupTests.ts
    ├── ----------------------
    ├── assets/
    ├── BAS/
    ├── components/
    ├── constant/
    ├── containers/
    ├── Core/
    ├── enum/
    ├── features/
    ├── GK/
    ├── hooks/
    ├── interfaces/
    ├── json/
    ├── layouts/
    ├── lib/
    ├── OAP/
    ├── pages/
    ├── store/
    ├── stories-examples/
    ├── temp/
    ├── utils/
```
