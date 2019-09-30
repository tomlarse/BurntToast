---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BTAppId.md
schema: 2.0.0
---

# New-BTAppId

## SYNOPSIS
Creates a new AppId Registry Key.

## SYNTAX

```
New-BTAppId [[-AppId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The New-BTAppId function create a new AppId registry key in the Current User's Registery Hive.
If the desired AppId is already present in the Registry then no changes are made.

If no AppId is specified then the AppId specified in the config.json file in the BurntToast module's root directory is used.

## EXAMPLES

### EXAMPLE 1
```
New-BTAppId
```

This command creates an AppId registry key using the value specified in the BurntToast module's config.json file, which is 'BurntToast' by default.

### EXAMPLE 2
```
New-BTAppId -AppId 'Script Checker'
```

This command create an AppId registry key called 'Script Checker.'

## PARAMETERS

### -AppId
Specifies the new AppId.
You can use any alphanumeric characters.

Defaults to the AppId specified in the config.json file in the BurntToast module's root directoy if not provided.

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

### System.String
### You cannot pipe input to this cmdlet.
## OUTPUTS

### None
## NOTES

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BTAppId.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BTAppId.md)

