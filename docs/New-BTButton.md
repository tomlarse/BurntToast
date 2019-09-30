---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BTButton.md
schema: 2.0.0
---

# New-BTButton

## SYNOPSIS
Creates a new clickable button for a Toast Notification.

## SYNTAX

### Button (Default)
```
New-BTButton -Content <String> -Arguments <String> [-ActivationType <ToastActivationType>] [-ImageUri <String>]
 [-Id <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Snooze
```
New-BTButton [-Snooze] [-Content <String>] [-Id <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Dismiss
```
New-BTButton [-Dismiss] [-Content <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The New-BTButton function creates a new clickable button for a Toast Notification.
Up to five buttons can be added to one Toast.

Buttons can be fully customized with display text, images and arguments or system handled 'Snooze' and 'Dismiss' buttons.

## EXAMPLES

### EXAMPLE 1
```
New-BTButton -Dismiss
```

This command creates a button which mimmicks the act of 'swiping away' the Toast when clicked.

### EXAMPLE 2
```
New-BTButton -Snooze
```

This command creates a button which will snooze the Toast for the system default snooze time (often 10 minutes).

### EXAMPLE 3
```
New-BTButton -Snooze -Content 'Sleep' -Id 'TimeSelection'
```

This command creates a button which will snooze the Toast for the time selected in the SelectionBox with the ID 'TimeSelection'.
The button will show the text 'Sleep' rather than 'Dismiss.'

### EXAMPLE 4
```
New-BTButton -Content 'Blog' -Arguments 'https://king.geek.nz'
```

This command creates a button with the display text "Blog", which will launch a browser window to "http://king.geek.nz" when clicked.

### EXAMPLE 5
```
$Picture = 'C:\temp\example.png'
```

New-BTButton -Content 'View Picture' -Arguments $Picture -ImageUri $Picture

This example creates a button with the display text "View Picture" with a picture to the left, which will launch the default picture viewer application and load the picture when clicked.

## PARAMETERS

### -Snooze
Specifies a system handled snooze button.
When paired with a selection box the snooze time is customizable and user selectable, otherwise the system default snooze time is used.

Display text defaults to a localized 'Snooze', but this can be overridden with the Content parameter.

```yaml
Type: SwitchParameter
Parameter Sets: Snooze
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dismiss
Specifies a system handled dismiss button.
Clicking the resulting button has the same affect as 'swiping away' or otherwise dismissing the Toast.

Display text defaults to a localized 'Dismiss', but this can be overridden with the Content parameter.

```yaml
Type: SwitchParameter
Parameter Sets: Dismiss
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Content
Specifies the text to display on the button.

```yaml
Type: String
Parameter Sets: Button
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Snooze, Dismiss
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Arguments
Specifies an app defined string.

For the purposes of BurntToast notifications this is generally the path to a file or URI and paired with the Protocol ActivationType.

```yaml
Type: String
Parameter Sets: Button
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActivationType
Defines tne ActivationType that is trigger when the button is pressed.

Defaults to Protocol which will open the file or URI specified in with the Arguments parameter in the rlevant system default application.

```yaml
Type: ToastActivationType
Parameter Sets: Button
Aliases:
Accepted values: Foreground, Background, Protocol

Required: False
Position: Named
Default value: Protocol
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageUri
Specifies an image icon to display on the button.

```yaml
Type: String
Parameter Sets: Button
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifies the ID of a relevant Toast control.

Standard buttons can be paried with a text box which makes the button appear to the right of it.

Snooze buttons can be paired with a selection box to select the ammount of time to snooze.

```yaml
Type: String
Parameter Sets: Button, Snooze
Aliases: TextBoxId, SelectionBoxId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
###     You cannot pipe input to this function.
## OUTPUTS

### Microsoft.Toolkit.Uwp.Notifications.ToastButton
### Microsoft.Toolkit.Uwp.Notifications.ToastButtonDismiss
### Microsoft.Toolkit.Uwp.Notifications.ToastButtonSnooze
## NOTES

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BTButton.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BTButton.md)

