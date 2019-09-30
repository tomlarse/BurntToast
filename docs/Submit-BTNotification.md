---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/Submit-BTNotification.md
schema: 2.0.0
---

# Submit-BTNotification

## SYNOPSIS
Submits a completed toast notification for display.

## SYNTAX

```
Submit-BTNotification [[-Content] <ToastContent>] [[-SequenceNumber] <UInt64>] [[-UniqueIdentifier] <String>]
 [[-AppId] <String>] [[-DataBinding] <Hashtable>] [[-ExpirationTime] <DateTime>] [-SuppressPopup] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The Submit-BTNotification function submits a completed toast notification to the operating systems' notification manager for display.

## EXAMPLES

### EXAMPLE 1
```
Submit-BTNotification -Content $Toast1 -UniqueIdentifier 'Toast001'
```

This command submits the complete toast content object $Toast1, from the New-BTContent function, and tags it with a unique identifier so that it can be replaced/updated.

## PARAMETERS

### -Content
A Toast Content object which is the Base Toast element, created using the New-BTContent function.

```yaml
Type: ToastContent
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SequenceNumber
When updating toasts (not curently working) rapidly, the sequence number helps to ensure that toasts recieved out of order will not be displayed in a manner that may confuse.

A higher sequence number indicates a newer toast.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 0
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
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppId
Specifies the AppId of the 'application' or process that spawned the toast notification.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: $Script:Config.AppId
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
Position: 5
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
Position: 6
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
## OUTPUTS

### None
## NOTES

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/Submit-BTNotification.md](https://github.com/Windos/BurntToast/blob/master/Help/Submit-BTNotification.md)

