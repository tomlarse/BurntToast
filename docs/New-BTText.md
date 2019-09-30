---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BTText.md
schema: 2.0.0
---

# New-BTText

## SYNOPSIS
Creates a new Text Element for Toast Notifications.

## SYNTAX

```
New-BTText [[-Text] <String>] [[-MaxLines] <Int32>] [[-MinLines] <Int32>] [-Wrap]
 [[-Align] <AdaptiveTextAlign>] [[-Style] <AdaptiveTextStyle>] [[-Language] <String>] [-Bind] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The New-BTText function creates a new Text Element for Toast Notifications.

You can specify the text you want displayed in a Toast Notification as a string, or run the function without a paramter for a blank line.

Each Text Element is the equivalent of one line in on a Toast Notification, long lines will wrap.

## EXAMPLES

### EXAMPLE 1
```
New-BTText -Content 'This is a line with text!'
```

Creates a Text Element that will show the string 'This is a line with text!' on a Toast Notification.

### EXAMPLE 2
```
New-BTText
```

Creates a Text Element that will show a blank line on a Toast Notification.

## PARAMETERS

### -Text
The text to display.
Data binding support added in Creators Update, only works for toast top-level text elements (But appears to not be working via PowerShell yet.)

```yaml
Type: String
Parameter Sets: (All)
Aliases: Content

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxLines
The maximum number of lines the text element is allowed to display.
For Toasts, top-level text elements will have varying max line amounts (and in the Anniversary Update you can change the max lines).

Text on a Toast inside a group (not yet implemented) will behave identically to Tiles (default to infinity).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinLines
The minimum number of lines the text element must display.
Note that for Toast, this property will only take effect if the text is inside a group (not yet implemented.)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wrap
Supply this switch to enable text wrapping.
For Toasts, this is true on top-level text elements, and false inside a group (not yet implemented.)

Note that for Toast, setting wrap will only take effect if the text is inside a group (you can use HintMaxLines = 1 to prevent top-level text elements from wrapping).

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

### -Align
The horizontal alignment of the text.
Note that for Toast, this property will only take effect if the text is inside a group (not yet implemented.)

```yaml
Type: AdaptiveTextAlign
Parameter Sets: (All)
Aliases:
Accepted values: Default, Auto, Left, Center, Right

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Style
The style controls the text's font size, weight, and opacity.
Note that for Toast, the style will only take effect if the text is inside a group (not yet implemented.)

```yaml
Type: AdaptiveTextStyle
Parameter Sets: (All)
Aliases:
Accepted values: Default, Caption, CaptionSubtle, Body, BodySubtle, Base, BaseSubtle, Subtitle, SubtitleSubtle, Title, TitleSubtle, TitleNumeral, Subheader, SubheaderSubtle, SubheaderNumeral, Header, HeaderSubtle, HeaderNumeral

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Language
The target locale of the XML payload, specified as a BCP-47 language tags such as "en-US" or "fr-FR".
The locale specified here overrides any other specified locale, such as that in binding or visual.
If this value is a literal string, this attribute defaults to the user's UI language.
If this value is a string reference, this attribute defaults to the locale chosen by Windows Runtime in resolving the string.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bind
{{ Fill Bind Description }}

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

### String
### You cannot pipe input to this function.
## OUTPUTS

### Text
## NOTES
TODO: Implement hint-style (https://blogs.msdn.microsoft.com/tiles_and_toasts/2015/06/30/adaptive-tile-templates-schema-and-documentation/)

Credit for most of the help text for this function go to the authors of the UWPCommunityToolkit library that this module relies upon.

Please see the originating repo here: https://github.com/Microsoft/UWPCommunityToolkit

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BTText.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BTText.md)

