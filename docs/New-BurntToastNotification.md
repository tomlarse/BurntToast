---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BurntToastNotification.md
schema: 2.0.0
---

# New-BurntToastNotification

## SYNOPSIS
Creates and displays a Toast Notification.

## SYNTAX

### Sound (Default)
```
New-BurntToastNotification [-Text <String[]>] [-AppLogo <String>] [-Sound <String>] [-Header <ToastHeader>]
 [-ProgressBar <AdaptiveProgressBar[]>] [-UniqueIdentifier <String>] [-DataBinding <Hashtable>]
 [-ExpirationTime <DateTime>] [-SuppressPopup] [-CustomTimestamp <DateTime>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Sound-Button
```
New-BurntToastNotification [-Text <String[]>] [-AppLogo <String>] -Sound <String> -Button <IToastButton[]>
 [-Header <ToastHeader>] [-ProgressBar <AdaptiveProgressBar[]>] [-UniqueIdentifier <String>]
 [-DataBinding <Hashtable>] [-ExpirationTime <DateTime>] [-SuppressPopup] [-CustomTimestamp <DateTime>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Sound-SnD
```
New-BurntToastNotification [-Text <String[]>] [-AppLogo <String>] -Sound <String> [-SnoozeAndDismiss]
 [-Header <ToastHeader>] [-ProgressBar <AdaptiveProgressBar[]>] [-UniqueIdentifier <String>]
 [-DataBinding <Hashtable>] [-ExpirationTime <DateTime>] [-SuppressPopup] [-CustomTimestamp <DateTime>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Silent-Button
```
New-BurntToastNotification [-Text <String[]>] [-AppLogo <String>] [-Silent] -Button <IToastButton[]>
 [-Header <ToastHeader>] [-ProgressBar <AdaptiveProgressBar[]>] [-UniqueIdentifier <String>]
 [-DataBinding <Hashtable>] [-ExpirationTime <DateTime>] [-SuppressPopup] [-CustomTimestamp <DateTime>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Silent-SnD
```
New-BurntToastNotification [-Text <String[]>] [-AppLogo <String>] [-Silent] [-SnoozeAndDismiss]
 [-Header <ToastHeader>] [-ProgressBar <AdaptiveProgressBar[]>] [-UniqueIdentifier <String>]
 [-DataBinding <Hashtable>] [-ExpirationTime <DateTime>] [-SuppressPopup] [-CustomTimestamp <DateTime>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Silent
```
New-BurntToastNotification [-Text <String[]>] [-AppLogo <String>] [-Silent] [-Header <ToastHeader>]
 [-ProgressBar <AdaptiveProgressBar[]>] [-UniqueIdentifier <String>] [-DataBinding <Hashtable>]
 [-ExpirationTime <DateTime>] [-SuppressPopup] [-CustomTimestamp <DateTime>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SnD
```
New-BurntToastNotification [-Text <String[]>] [-AppLogo <String>] [-SnoozeAndDismiss] [-Header <ToastHeader>]
 [-ProgressBar <AdaptiveProgressBar[]>] [-UniqueIdentifier <String>] [-DataBinding <Hashtable>]
 [-ExpirationTime <DateTime>] [-SuppressPopup] [-CustomTimestamp <DateTime>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Button
```
New-BurntToastNotification [-Text <String[]>] [-AppLogo <String>] -Button <IToastButton[]>
 [-Header <ToastHeader>] [-ProgressBar <AdaptiveProgressBar[]>] [-UniqueIdentifier <String>]
 [-DataBinding <Hashtable>] [-ExpirationTime <DateTime>] [-SuppressPopup] [-CustomTimestamp <DateTime>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The New-BurntToastNotification function creates and displays a Toast Notification on Microsoft Windows 10.

You can specify the text and/or image displayed as well as selecting the sound that is played when the Toast Notification is displayed.

You can optionally call the New-BurntToastNotification function with the Toast alias.

## EXAMPLES

### EXAMPLE 1
```
New-BurntToastNotification
```

This command creates and displays a Toast Notification with all default values.

### EXAMPLE 2
```
New-BurntToastNotification -Text 'Example Script', 'The example script has run successfully.'
```

This command creates and displays a Toast Notification with customized title and display text.

### EXAMPLE 3
```
New-BurntToastNotification -Text 'WAKE UP!' -Sound 'Alarm2'
```

This command creates and displays a Toast Notification which plays a looping alarm sound and lasts longer than a default Toast.

### EXAMPLE 4
```
$BlogButton = New-BTButton -Content 'Open Blog' -Arguments 'https://king.geek.nz'
```

New-BurntToastNotification -Text 'New Blog Post!' -Button $BlogButton

This exmaple creates a Toast Notification with a button which will open a link to "https://king.geek.nz" when clicked.

### EXAMPLE 5
```
$ToastHeader = New-BTHeader -Id '001' -Title 'Stack Overflow Questions'
```

New-BurntToastNotification -Text 'New Stack Overflow Question!', 'More details!' -Header $ToastHeader

This example creates a Toast Notification which will be displayed under the header 'Stack Overflow Questions.'

### EXAMPLE 6
```
$Progress = New-BTProgressBar -Status 'Copying files' -Value 0.2
```

New-BurntToastNotification -Text 'File copy script running', 'More details!' -ProgressBar $Progress

This example creates a Toast Notification which will include a progress bar.

### EXAMPLE 7
```
New-BurntToastNotification -Text 'Professional Content', 'And gr8 spelling' -UniqueIdentifier 'Toast001'
```

New-BurntToastNotification -Text 'Professional Content', 'And great spelling' -UniqueIdentifier 'Toast001'

This example will show a toast with a spelling error, which is replaced by a second toast because they both shared a unique identifier.

## PARAMETERS

### -Text
Specifies the text to show on the Toast Notification.
Up to three strings can be displayed, the first of which will be embolden as a title.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Default Notification
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppLogo
Specifies the path to an image that will override the default image displayed with a Toast Notification.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sound
Selects the sound to acompany the Toast Notification.
Any 'Alarm' or 'Call' tones will automatically loop and extent the amount of time that a Toast is displayed on screen.

Cannot be used in conjunction with the 'Silent' switch.

```yaml
Type: String
Parameter Sets: Sound
Aliases:

Required: False
Position: Named
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Sound-Button, Sound-SnD
Aliases:

Required: True
Position: Named
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### -Silent
Indicates that the Toast Notification will be displayed on screen without an accompanying sound.

Cannot be used in conjunction with the 'Sound' parameter.

```yaml
Type: SwitchParameter
Parameter Sets: Silent-Button, Silent-SnD, Silent
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -SnoozeAndDismiss
Adds a default selection box and snooze/dismiss buttons to the bottom of the Toast Notification.

```yaml
Type: SwitchParameter
Parameter Sets: Sound-SnD, Silent-SnD, SnD
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Button
Allows up to five buttons to be added to the bottom of the Toast Notification.
These buttons should be created using the New-BTButton function.

```yaml
Type: IToastButton[]
Parameter Sets: Sound-Button, Silent-Button, Button
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Header
Specify the Toast Header object created using the New-BTHeader function, for seperation/categorization of toasts from the same AppId.

```yaml
Type: ToastHeader
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgressBar
Specify one or more Progress Bar object created using the New-BTProgressBar function.

```yaml
Type: AdaptiveProgressBar[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UniqueIdentifier
A string that uniquely identifies a toast notification.
Submitting a new toast with the same identifier as a previous toast will replace the previous toast.

This is useful when updating the progress of a process, using a progress bar, or otherwise correcting/updating the information on a toast.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataBinding
A hashtable that binds strings to keys in a toast notification.
In order to update a toast, the original toast needs to include a databinding hashtable.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpirationTime
The time after which the notification is no longer relevant and should be removed from the Action Center.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SuppressPopup
Bypasses display to the screen and sends the notification directly to the Action Center.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomTimestamp
Sets the time at which Windows should consider the notification to have been created.
If not specified the time at which the notification was recieved will be used.

The time stamp affects sorting of notifications in the Action Center.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

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

### None
###     New-BurntToastNotification displays the Toast Notification that is created.
## NOTES
I'm *really* sorry about the number of Parameter Sets.
The best explanation is:

* You cannot specify a sound and mark the toast as silent at the same time.
* You cannot specify SnoozeAndDismiss and custom buttons at the same time.

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BurntToastNotification.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BurntToastNotification.md)

