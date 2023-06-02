# @

## Overview

- Store common files in the `@` directory. This is a special directory that is not copied to the output directory. It is used to store files that are used by multiple pages.

- This folder will be updated 1 by 1 to avoid conflicts with current folder with same name and functionality (like `hooks`, `styles`, ect..)

## Structure

```bash
@/
    # Each features already have its own folder. Only add common things here
    ├── assets/         # Store all assets (images, fonts, ...)
    ├── components/     # Store all components. Components is dump component. Use to custom library or own dumb component
    ├── constants/      # Store all constants
    ├── hooks/          # Store all hooks
    ├── interfaces/     # Store all interfaces
    ├── services/       # Store all services
    ├── store/          # Store all store
    ├── stories/        # Store all stories
    ├── styles/         # Store all styles
    └── utils/          # Store all utils
```
