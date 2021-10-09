# API Reference

## usePopperjs

```ts
function usePopperjs(
  reference: MaybeRef<Element | VirtualElement>,
  popper: MaybeRef<HTMLElement>,
  options: MaybeRef<{
    // The Popperjs options
    placement?: Placement; // default: "bottom"
    modifiers?: Array<TModifier>; // default: []
    strategy?: PositioningStrategy; // default: "absolute"
    onFirstUpdate?: (arg0: Partial<State>) => void;

    // Extra options
    trigger?: MaybeRef<Trigger | undefined>; // default: "hover"
    delayOnMouseover?: number; // default: 200
    delayOnMouseout?: number; // default: 200
    forceShow?: boolean; // default: false
    onShow?: Function;
    onHide?: Function;
  }>
): {
  // The Popperjs instance
  instance: Instance;
  visible: Ref<boolean>;
};
```

## Popper

```ts
type props = {
  // The Popperjs options
  placement?: Placement; // default: "bottom"
  modifiers?: Array<TModifier>; // default: []
  strategy?: PositioningStrategy; // default: "absolute"
  onFirstUpdate?: (arg0: Partial<State>) => void;

  // The usePopperjs options
  trigger?: MaybeRef<Exclude<Trigger, "manual"> | undefined>; // default: "hover"
  delayOnMouseover?: number; // default: 200
  delayOnMouseout?: number; // default: 200
  forceShow?: boolean; // default: false

  // Extra props
  referenceIs?: string; // default: "div"
  referenceProps?: Object;
  popperIs?: string; // default: "div"
  popperProps?: Object;
  disabled?: boolean;
  teleportProps?: TeleportProps;
  transitionProps?: TransitionProps;
};

type emitOptions = [
  "show",
  "hide",

  // Transition only
  "before-enter",
  "enter",
  "after-enter",
  "enter-cancelled",
  "before-leave",
  "leave",
  "after-leave",
  "leave-cancelled"
];
```