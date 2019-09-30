---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BurntToastShoulderTap.md
schema: 2.0.0
---

# New-BurntToastShoulderTap

## SYNOPSIS
Creates and displays a Shoulder Tap notification.

## SYNTAX

```
New-BurntToastShoulderTap [-Image] <String> [-Person] <String> [[-Text] <String[]>] [[-AppLogo] <String>]
 [[-Button] <IToastButton[]>] [[-Header] <ToastHeader>] [[-ProgressBar] <AdaptiveProgressBar[]>]
 [[-UniqueIdentifier] <String>] [[-ExpirationTime] <DateTime>] [-SuppressPopup] [[-CustomTimestamp] <DateTime>]
 [[-AppId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The New-BurntToastShoulderTap function creates and displays a Shoulder Tap notification on Microsoft Windows 10.

You can provide a static image or animated GIF, which will be displayed above the specified pinned contact.

If a matching contact cannot be found, Windows will fall back to a toast notification.
This toast notification will also been seen in the Action Center (with or without a working Shoulder Tap.)

You can optionally call the New-BurntToastShoulderTap function with the ShoulderTap alias.

## EXAMPLES

### EXAMPLE 1
```
$ShoulderSplat = @{
```

Image = 'https://www.route66sodas.com/wp-content/uploads/2019/01/Alert.gif'
    Person = 'stormy@example.com'
    Text = 'Alarms!', "There's a thing you need to worry about"
}

New-BurntToastShoulderTap @ShoulderSplat

## PARAMETERS

### -Image
The URI of the image.
Can be a static image or animated GIF.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Person
The email address of the "person" from which the Shoulder Tap is coming from.

A contact with a matching email address must be pinned to the task bar.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Text
Specifies the text to show on the Toast Notification.
Up to three strings can be displayed, the first of which will be embolden as a title.

The toast version will be shown on screen if the required contact is not pinned to the task bar, and will also appear in the Action Center.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Button
Allows up to five buttons to be added to the bottom of the Toast Notification.
These buttons should be created using the New-BTButton function.

```yaml
Type: IToastButton[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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
Position: 6
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
Position: 7
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
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpirationTime
The time after which the notification is no longer relevant and should be removed from the People notification and Action Center.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
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
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppId
Specifies the AppId of the 'application' or process that spawned the toast notification.

Defaults to the People App, rather than the configured default.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: Microsoft.People_8wekyb3d8bbwe!x4c7a3b7dy2188y46d4ya362y19ac5a5805e5x
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

### LOTS...
## OUTPUTS

### None
###     New-BurntToastShoulderTap displays the Shoulder Tap that is created.
## NOTES
There's some manual steps required to create and pin a contact which matches the specified email address in the Person parameter.

There will be a blog post about this on https://toastit.dev, and also further documented within this module in the next release.

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BurntToastShoulderTap.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BurntToastShoulderTap.md)

