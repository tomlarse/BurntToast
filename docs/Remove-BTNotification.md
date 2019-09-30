---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/Remove-BTNotification.md
schema: 2.0.0
---

# Remove-BTNotification

## SYNOPSIS
Removes toast notifications from the Action Center.

## SYNTAX

```
Remove-BTNotification [[-AppId] <String>] [[-Tag] <String>] [[-Group] <String>]
```

## DESCRIPTION
The Remove-BTNotification function removes toast notifications from the Action Center.

If no parameters are specified, all toasts (for the default AppId) will be removed.

Tags and Groups for Toasts can be found using the Get-BTHistory function.

## EXAMPLES

### EXAMPLE 1
```
Remove-BTNotification
```

### EXAMPLE 2
```
Remove-BTNotification -Tag 'UniqueIdentifier'
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

### -Tag
Specifies the tag, which identifies a given toast notification.

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

### -Group
Specifies the group, which helps to identify a given toast notification.

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

## INPUTS

### LOTS
## OUTPUTS

### NONE
## NOTES

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/Remove-BTNotification.md](https://github.com/Windos/BurntToast/blob/master/Help/Remove-BTNotification.md)

