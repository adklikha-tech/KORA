---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

![Likha Process Designer](../../images/process-designer.png)

## Mouse and Keyboard activities

Mouse and Keyboard activities send input to the currently focused window.

Use these activities when an application does not expose a reliable selector, or when the automation needs to type into whatever field is already active.

### Mouse and Keyboard > Get Mouse Coordinate

`Get Mouse Coordinate` reads the current mouse pointer location and saves it into two Number variables.

Properties:

```txt
X Position output    variable that receives the current X coordinate
Y Position output    variable that receives the current Y coordinate
```

Example:

```txt
X Position output: mouse_x
Y Position output: mouse_y
```

After the activity runs, you can use `mouse_x` and `mouse_y` in later activities such as `Move Mouse`, logs, or Set Variable operations.

`Get Mouse Coordinate` includes error handling:

```txt
Retry on error
retry count
interval seconds
on error
error label
```

### Mouse and Keyboard > Move Mouse

`Move Mouse` moves the mouse pointer to absolute screen coordinates.

Properties:

```txt
X position    horizontal screen coordinate, integer variable, or token
Y position    vertical screen coordinate, integer variable, or token
Send click    optionally send a click action after moving
Click type    click or mouse-button action to send
wait seconds  delay used when Click type is wait
```

Example:

```txt
X position: 500
Y position: 300
```

This moves the pointer to `x=500`, `y=300`.

You can also use Number variables, for example values captured by `Get Mouse Coordinate`:

```txt
X position: mouse_x
Y position: mouse_y
```

Token syntax is also supported:

```txt
X position: {{mouse_x}}
Y position: {{mouse_y}}
```

Click type options:

```txt
Left click
Right click
Double click
Middle click
Left button down
Left button up
Right button down
Right button up
wait
```

If `Send click` is enabled, the click action runs after the pointer moves.

Use `wait` when you want the activity to move the pointer and pause before the next activity.

`Move Mouse` includes error handling:

```txt
Retry on error
retry count
interval seconds
on error
error label
```

### Mouse and Keyboard > Send Keys

`Send Keys` types text and can optionally press one special key or modifier after the text.

### Properties

```txt
Text to send                text typed into the active window
Special key / modifier      optional key pressed after the text
delay between keystrokes    seconds to wait between each typed character
```

### Special keys and modifiers

The dropdown includes common keyboard keys such as:

```txt
enter
tab
esc
backspace
delete
space
up
down
left
right
home
end
pageup
pagedown
insert
ctrl
alt
shift
win
f1 - f12
```

### Example: type text and press Enter

Properties:

```txt
Text to send: Hello world
Special key / modifier: enter
delay between keystrokes: 0.02
```

This types:

```txt
Hello world
```

Then presses:

```txt
Enter
```

### Using variables

You can use normal variable tokens in `Text to send`.

Example:

```txt
{{queue_item.payload.name}}
```

If the queue item payload contains `John Doe`, the activity types:

```txt
John Doe
```

### Error handling

`Send Keys` includes the same basic error handling options as other automation activities:

```txt
Retry on error
retry count
interval seconds
on error
error label
```

Use retries when the target application may not be ready immediately.

### Important notes

`Send Keys` sends input to the active/focused window.

Before using `Send Keys`, make sure the correct application and field are focused. You can do this with a Desktop click, Desktop activate, or Browser click activity.

For hotkey combinations such as `Ctrl+S`, use `Desktop > Hotkey` when possible.
