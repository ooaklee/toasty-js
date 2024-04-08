# Toasty JS (WIP)

Toasty is a lightweight, Tailwind CSS-styled, vanilla JS toast notification library. (currently WIP)

## Usage

Please find below the optional options that you can set.

```js
const toasty = new Toasty({
    position: "bottom-center",
    stack: [],
    offsetX: 20,
    offsetY: 20,
    gap: 20,
    numToasts: 0,
    duration: ".5s",
    timing: "ease",
    dimOld: true,
    zIndex: 9999,
    autoCloseTime: 3000,
    toastStyle: { // Optionally change default toast styles
        // ...
        theme: { // theme is the default style used if 'success', 'info', 'warning' or 'error' is not specified
          main: " bg-background dark:bg-[#1F1F1F] border-[1px] ",
          header: "text-foreground uppercase text-xs font-semibold",
          body: "text-muted-foreground",
          closeIcon: "font-medium text-foreground hover:font-bold",
        }
        // ...
    }
})
```

### Push a message to the user


#### Autoclosing toast

```js
toasty.push({
        title: "Hold it!",
        content: "You do not have permission to do this action.",
        style: "error",
    })
```

#### Manual close toast

```js
toasty.push({
        title: "Example Toast",
        content: "Simply specifiy autoCloseTime as false to prevent auto closing.",
        autoCloseTime: false
    })
```



## License

MIT



