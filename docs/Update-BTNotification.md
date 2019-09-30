---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/Update-BTNotification.md
schema: 2.0.0
---

# Update-BTNotification

## SYNOPSIS
Updates a toast notification for display.

## SYNTAX

```
Update-BTNotification [[-SequenceNumber] <UInt64>] [[-UniqueIdentifier] <String>] [[-AppId] <String>]
 [[-DataBinding] <Hashtable>] [<CommonParameters>]
```

## DESCRIPTION
The Update-BTNotification function updates a toast notification in the operating systems' notification manager.

## EXAMPLES

### EXAMPLE 1
```
$FirstDataBinding = @{
```

FirstLine = 'Example Toast Heading'
    SecondLine = 'This toast is still the original'
}

New-BurntToastNotification -Text 'FirstLine', 'SecondLine' -UniqueIdentifier 'ExampleToast' -DataBinding $FirstDataBinding

$SecondDataBinding = @{
    SecondLine = 'This toast has been updated!'
}

Update-BTNotification -UniqueIdentifier 'ExampleToast' -DataBinding $SecondDataBinding

## PARAMETERS

### -SequenceNumber
When updating toasts (not curently working) rapidly, the sequence number helps to ensure that toasts recieved out of order will not be displayed in a manner that may confuse.

A higher sequence number indicates a newer toast.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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
Position: 2
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
Position: 3
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
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### LOTS...
## OUTPUTS

### NONE
## NOTES

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/Update-BTNotification.md](https://github.com/Windos/BurntToast/blob/master/Help/Update-BTNotification.md)

