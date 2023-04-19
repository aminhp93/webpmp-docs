---
sidebar_position: 1
---

# Editor Intro

## Features

Edit Process View, allow add/update/delete items

## Path: PMP/src/temp/Edit.js

Move to PMP/src/components

## Structure

### Render

- Viewport
- Editor

### Context

- props

```tsx
interface Props {
  controllerId: string;
  disableUpdateContext: () => void;
  type: string;
  updateContext: (data) => void;
  viewId: string;
}
```

- view: view of current process view
  - useView hook

```tsx
interface View {
  backgroundColor: string; // "#ffffff"
  canEdit: boolean;
  dimensions: number[]; // [1920, 1080]
  error: boolean;
  errorMessage: string; // "Error: Request failed with status code 404"
  isErrorThrow: boolean;
  items: Item;
  loading: boolean;
  resourcePath: string; // "/controllers/9ec5464b-bf8e-42ae-b740-7cc95a5f9e3b/systems/d1bf21d3-be36-48b7-a69d-c8019356897c/subsystems/42092175-fa07-4f06-a143-0b6eee205065/views/6c5b1709-3ea7-465e-8406-b6e13804227e"
  scrollable: boolean;
  template: null;
  variables: null;
  viewId: string; // "6c5b1709-3ea7-465e-8406-b6e13804227e"
  _meta: {};
}
```

- timeline: store timeline of all action in this editor
  - useTimeline hook

```tsx
interface Timeline {
    addFrame: (data) => void
    frame: Frame
    goBackward: () => void
    goForward: () => void
    length: 1
```

- template: store list template
  - useView hook

```tsx
interface Template {
    backgroundColor: null
    dimensions: null
    error: boolean
    errorMessage: string
    isErrorThrow: boolean
    items: null
    loading: boolean
    resourcePath: null
    template: null
    variables: null
    viewId: string
```

- focusdItems: hold list of all current items

```tsx
interface FocusItem {
    data: any
    id: string // "CompensationCurveButton"
    instance: string //"91d7a256-5cb0-44e0-8e45-c76301add18f"
    properties: any
        // buttonSettings:  {arrow: false, iconPosition: 'left'}
        // dynamicButtonText : {active: false, tag: {…}, dmf: {…}}
        // geometry : {height: 40, width: 120}
        // image : {singleImage: {…}, fillColor: '#65666A', scale: 0.8, active: true}
        // settings : {compensationCurve: {…}, read: null, role: null}
        // style : {border: false, borderColor: '#65666A', borderRadius: 3, borderStyle: 'solid', borderThickness: 2, …}
        // title : {align: 'left', bold: true, color: '#65666A', family: 'Arial', italic: false, …}
        // transform : {anchor: 'center', rotation: 0, scale: 1, show: true, x: 718, …}
```

- ClipBoardContext: use to store copy/paste items

```tsx
interface ClipBoardContext {
    items: Item[]
    isUpdated: boolean
```
