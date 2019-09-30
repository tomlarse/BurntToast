---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BTShoulderTapPeople.md
schema: 2.0.0
---

# New-BTShoulderTapPeople

## SYNOPSIS
Creates a new ToastPeople object.

## SYNTAX

### Email (Default)
```
New-BTShoulderTapPeople -Email <String> [<CommonParameters>]
```

### RemoteId
```
New-BTShoulderTapPeople -RemoteId <String> [<CommonParameters>]
```

### PhoneNumber
```
New-BTShoulderTapPeople -PhoneNumber <String> [<CommonParameters>]
```

## DESCRIPTION
The New-BTShoulderTapPeople function creates a new ToastPeople object.
This object identifies a user from the People app which has been pinned to the Windows Taskbar.

This function is mainly used internally, as it is abstracted away when using New-BurntToastShoulderTap.

## EXAMPLES

### EXAMPLE 1
```
$Person = New-BTShoulderTapPeople -Email 'bob@example.com'
```

## PARAMETERS

### -Email
The email address which matches a contact in the Contacts app.

```yaml
Type: String
Parameter Sets: Email
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteId
The remote identifier which matches a contact in the Contacts app.

```yaml
Type: String
Parameter Sets: RemoteId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PhoneNumber
The phone number which matches a contact in the Contacts app.

```yaml
Type: String
Parameter Sets: PhoneNumber
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### STRING
## OUTPUTS

### ToastPeople
## NOTES

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BTShoulderTapPeople.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BTShoulderTapPeople.md)

