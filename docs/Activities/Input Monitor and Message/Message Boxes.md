---
layout: default
---

<nav class="doc-home-link"><a href="{{ '/' | relative_url }}">&larr; Go back Home</a></nav>

![Likha Process Designer](../../images/process-designer.png)

## Message Boxes activities

Message Boxes activities show simple desktop prompts during a flow.

Use these when the automation needs confirmation from the attended user before continuing.

### Message Boxes > Display message

`Display message` opens a Windows message box and saves the clicked button into a Text variable.

Properties:

```txt
Message box title       title shown at the top of the message box
Message to Display      message body shown to the user
Message box buttons     button layout to display
button Selected         output variable that receives the selected button
```

Button options:

```txt
Yes - No
OK
OK - Cancel
```

Example:

```txt
Message box title: Confirm
Message to Display: Continue processing this queue item?
Message box buttons: Yes - No
button Selected: button_selected
```

If the user clicks `Yes`, the variable contains:

```txt
button_selected = Yes
```

Possible output values are:

```txt
OK
Cancel
Yes
No
```

You can use the output in `Logic > If Else`, for example:

```txt
button_selected == "Yes"
```
