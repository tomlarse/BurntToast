---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BTHeader.md
schema: 2.0.0
---

# New-BTHeader

## SYNOPSIS
Creates a new toast notification header.

## SYNTAX

```
New-BTHeader [-Id] <String> [-Title] <String> [[-Arguments] <String>] [[-ActivationType] <ToastActivationType>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The New-BTHeader function creates a new toast notification header for a Toast Notification.

These headers are diaplyed at the top of a toast and are also used to categorize toasts in the Action Center.

## EXAMPLES

### EXAMPLE 1
```
New-BTHeader -Id 'primary header' -Title 'First Category'
```

This command creates a Toast Header object, which will be displayed with the text "First Category."

### EXAMPLE 2
```
New-BTHeader -Id '001' -Title 'Stack Overflow Questions' -Arguments 'http://stackoverflow.com/'
```

This command creates a Toast Header object, which will be displayed with the text "First Category."

Clicking the header will take the user to the Stack Overflow website.

## PARAMETERS

### -Id
Unique string that identifies a header.
If a new Id is provided, the system will treat the header as a new header even if it has the same display text as a previous header.

It is possible to update a header's display text by re-using the Id but changing the title.

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

### -Title
The header string that is displayed to the user.

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

### -Arguments
Specifies an app defined string.

For the purposes of BurntToast notifications this is generally the path to a file or URI and paired with the Protocol ActivationType.

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

### -ActivationType
Defines tne ActivationType that is trigger when the button is pressed.

Defaults to Protocol which will open the file or URI specified in with the Arguments parameter in the relevant system default application.

```yaml
Type: ToastActivationType
Parameter Sets: (All)
Aliases:
Accepted values: Foreground, Background, Protocol

Required: False
Position: 4
Default value: Protocol
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

### Microsoft.Toolkit.Uwp.Notifications.ToastHeader
## NOTES

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BTHeader.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BTHeader.md)
