# Components

## Overview

Component will not contain any logic and data. If it does, consider to move it to features.

Each components will contain all of its related files (scss, utils, constants, types, ...)

## Structure

```bash
components/
    ├── Plot.tsx
    ├── Plot.constants.ts
    ├── Plot.utils.ts
    ├── Plot.test.ts
    ├── Plot.scss
    ├── ...
    ├── plotDetail # name of subgroup will be start by lowercase
       ├── PlotDetail.tsx
       ├── PlotDetail.constants.tsx
       ├── PlotDetail.utils.ts
       └── ....
    ├── hooks/
       ├── useHook1.ts
       ├── useHook1.ts
       └── useHook2.ts
    ├── utils/ # If folder needs to split into smaller files, place all those files under folder. If it is just single file, name it with featuers like Plot.utils.ts
       ├── util1.ts
       ├── util2.ts
       └── util3.ts
    └── ...
```
