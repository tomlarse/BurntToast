---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BTVisual.md
schema: 2.0.0
---

# New-BTVisual

## SYNOPSIS
Creates a new visual element for toast notifications.

## SYNTAX

```
New-BTVisual [-BindingGeneric] <ToastBindingGeneric> [[-BindingShoulderTap] <ToastBindingShoulderTap>]
 [-AddImageQuery] [[-BaseUri] <Uri>] [[-Language] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The New-BTVisual function creates a new visual element for toast notifications, which defines all of the visual aspects of a toast.

## EXAMPLES

### EXAMPLE 1
```
New-BTVisual -BindingGeneric $Binding1
```

This command creates a new Visual element taking a previously configured binding element as input.

## PARAMETERS

### -BindingGeneric
The generic Toast binding, which can be rendered on all devices.
This binding is created using the New-BTBinding function.

```yaml
Type: ToastBindingGeneric
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BindingShoulderTap
{{ Fill BindingShoulderTap Description }}

```yaml
Type: ToastBindingShoulderTap
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddImageQuery
Specify this switch to allow Windows to append a query string to the image URI supplied in the Toast notification.
Use this attribute if your server hosts images and can handle query strings, either by retrieving an image variant based on the query strings or by ignoring the query string and returning the image as specified without the query string.
This query string specifies scale, contrast setting, and language.

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

### -BaseUri
A default base URI that is combined with relative URIs in image source attributes.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Language
The target locale of the XML payload, specified as BCP-47 language tags such as "en-US" or "fr-FR".
This locale is overridden by any locale specified in binding or text.
If this value is a literal string, this attribute defaults to the user's UI language.
If this value is a string reference, this attribute defaults to the locale chosen by Windows Runtime in resolving the string.

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

### ToastVisual
## NOTES
Credit for most of the help text for this function go to the authors of the UWPCommunityToolkit library that this module relies upon.

Please see the originating repo here: https://github.com/Microsoft/UWPCommunityToolkit

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BTVisual.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BTVisual.md)

