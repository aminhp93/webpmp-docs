# Editor

## Overview

Editor of Process View after entering the editor mode.

## Structure

- If have `template` or `timeline` load view from there. If not create empty view as `Editor`

## Todo

- Update `PMP/src/temp/Edit.js` as main page
- Move all related files to `PMP/src/features/editor` like hooks, utils, constants, types, ...
- Related folders:

  - `PMP/src/components/Editor`
  - `PMP/src/components/edit`:

    - This component is huge. Find the way to move it.
    - Suggestion: can move all core property first to check impact if happens: `transform, geometry, style`

    - Check if component is implemented
      - Multiembedded: yes
      - Embedded: yes
      - SliderEmbeddedView: yes
      - StatusTableItem: yes
      - UserLog: yes
      - MultiChart: already implemented but not used
