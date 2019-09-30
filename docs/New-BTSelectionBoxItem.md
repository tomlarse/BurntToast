---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BTSelectionBoxItem.md
schema: 2.0.0
---

# New-BTSelectionBoxItem

## SYNOPSIS
Creates a selection box item.

## SYNTAX

```
New-BTSelectionBoxItem [-Id] <String> [-Content] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The New-BTSelectionBoxItem function creates a selection box item, for inclusion in a selection box created with New-BTInput.

## EXAMPLES

### EXAMPLE 1
```
$Select1 = New-BTSelectionBoxItem -Id 'Item1' -Content 'First option in the list'
```

This command creates a new Selection Box Item object which can now be used with the New-BTInput function.

## PARAMETERS

### -Id
Developer-provided ID that the developer uses later to retrieve input when the Toast is interacted with.

Can also be provided to a selection box to identify the default selection.

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

### -Content
String that is displayed on the selection item.
This is what the user sees.

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

### ToastSelectionBoxItem
## NOTES
Credit for most of the help text for this function go to the authors of the UWPCommunityToolkit library that this module relies upon.

Please see the originating repo here: https://github.com/Microsoft/UWPCommunityToolkit

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BTSelectionBoxItem.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BTSelectionBoxItem.md)

