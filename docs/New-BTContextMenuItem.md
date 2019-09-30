---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BTContextMenuItem.md
schema: 2.0.0
---

# New-BTContextMenuItem

## SYNOPSIS
Creates a Context Menu Item object.

## SYNTAX

```
New-BTContextMenuItem [-Content] <String> [-Arguments] <String> [[-ActivationType] <ToastActivationType>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The New-BTContextMenuItem function creates a Context Menu Item object.

## EXAMPLES

### EXAMPLE 1
```
New-BTContextMenuItem -Content 'Google' -Arguments 'https://google.com' -ActivationType Protocol
```

This command creates a new Context Menu Item object with the specified properties.

## PARAMETERS

### -Content
The text to display on the menu item.

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

### -Arguments
App-defined string of arguments that the app can later retrieve once it is activated when the user clicks the menu item.

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

### -ActivationType
Controls what type of activation this menu item will use when clicked.
Defaults to Foreground.

```yaml
Type: ToastActivationType
Parameter Sets: (All)
Aliases:
Accepted values: Foreground, Background, Protocol

Required: False
Position: 3
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
## OUTPUTS

### ToastContextMenuItem
## NOTES
Credit for most of the help text for this function go to the authors of the UWPCommunityToolkit library that this module relies upon.

Please see the originating repo here: https://github.com/Microsoft/UWPCommunityToolkit

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BTContextMenuItem.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BTContextMenuItem.md)

