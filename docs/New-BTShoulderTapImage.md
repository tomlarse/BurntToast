---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BTShoulderTapImage.md
schema: 2.0.0
---

# New-BTShoulderTapImage

## SYNOPSIS
Creates a new ToastShoulderTapImage object.

## SYNTAX

### Image (Default)
```
New-BTShoulderTapImage -Source <String> [-AlternateText <String>] [-AddImageQuery] [<CommonParameters>]
```

### Sprite
```
New-BTShoulderTapImage -SpriteSheet <String> -FrameHeight <UInt32> -FPS <UInt32> [-StartingFrame <UInt32>]
 [-AlternateText <String>] [-AddImageQuery] [<CommonParameters>]
```

## DESCRIPTION
The New-BTShoulderTapImage function creates a new ToastShoulderTapImage object.

The image can be a static image or anitmated gif, specified using the Source parameter.
It can also be a spritesheet.

This function is mainly used internally, as it is abstracted away when using New-BurntToastShoulderTap.

## EXAMPLES

### EXAMPLE 1
```
$Image = New-BTShoulderTapImage -Source 'https://www.route66sodas.com/wp-content/uploads/2019/01/Alert.gif'
```

## PARAMETERS

### -Source
{{ Fill Source Description }}

```yaml
Type: String
Parameter Sets: Image
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SpriteSheet
{{ Fill SpriteSheet Description }}

```yaml
Type: String
Parameter Sets: Sprite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrameHeight
{{ Fill FrameHeight Description }}

```yaml
Type: UInt32
Parameter Sets: Sprite
Aliases:

Required: True
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -FPS
{{ Fill FPS Description }}

```yaml
Type: UInt32
Parameter Sets: Sprite
Aliases:

Required: True
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartingFrame
{{ Fill StartingFrame Description }}

```yaml
Type: UInt32
Parameter Sets: Sprite
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### -AlternateText
{{ Fill AlternateText Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddImageQuery
{{ Fill AddImageQuery Description }}

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### LOTS
## OUTPUTS

### ToastShoulderTapImage
## NOTES

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BTShoulderTapImage.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BTShoulderTapImage.md)

