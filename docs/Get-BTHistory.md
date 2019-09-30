---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/Get-BTHistory.md
schema: 2.0.0
---

# Get-BTHistory

## SYNOPSIS
Shows all toast notifications in the Action Center.

## SYNTAX

```
Get-BTHistory [[-AppId] <String>] [[-UniqueIdentifier] <String>]
```

## DESCRIPTION
The Get-BTHistory function returns all toast notifications that are in the Action Center.
Toasts that have been dismissed by the user will not be returned.

The object returned includes tag and group information which can be used with the Remove-BTNotification function to clear specific notification from the Action Center.

## EXAMPLES

### EXAMPLE 1
```
Get-BTHistory
```

## PARAMETERS

### -AppId
Specifies the AppId of the 'application' or process that spawned the toast notification.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $Script:Config.AppId
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

## INPUTS

### STRING
## OUTPUTS

### TODO
## NOTES

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/Get-BTHistory.md](https://github.com/Windos/BurntToast/blob/master/Help/Get-BTHistory.md)

