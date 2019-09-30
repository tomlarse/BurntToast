---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BTAudio.md
schema: 2.0.0
---

# New-BTAudio

## SYNOPSIS
Creates a new Audio object for Toast Notifications.

## SYNTAX

### StandardSound (Default)
```
New-BTAudio -Source <Uri> [-Loop] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CustomSound
```
New-BTAudio -Path <String> [-Loop] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Silent
```
New-BTAudio [-Silent] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The New-BTAudio function creates a new Audio object for Toast Notifications.

You can use the parameters of New-BTAudio to select an audio file or a standard notification sound (including alarms).
Alternativly you can specify that a Toast Notification should be silent.

## EXAMPLES

### EXAMPLE 1
```
New-BTAudio -Source ms-winsoundevent:Notification.SMS
```

Creates an Audio  which will cause a Toast Notification to play the standard Microsoft 'SMS' sound.

### EXAMPLE 2
```
New-BTAudio -Path 'C:\Music\FavSong.mp3'
```

Creates an Audio  which will cause a Toast Notification to play the specified song.

### EXAMPLE 3
```
New-BTAudio -Silent
```

Creates an Audio  which will cause a Toast Notification to be silent.

## PARAMETERS

### -Source
Specifies one of the built in Microsoft notification sounds.

This paramater takes the full form of the sounds, in the form of a uri.
The New-BurntToastNotification function simplifies this, so be aware of the difference.

```yaml
Type: Uri
Parameter Sets: StandardSound
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
The full path to an audio file.
Supported file types include:

*.aac
*.flac
*.m4a
*.mp3
*.wav
*.wma

```yaml
Type: String
Parameter Sets: CustomSound
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Loop
Specifies that the slected sound should play multiple times if its duration is shorter than that of the toast it accompanies.

```yaml
Type: SwitchParameter
Parameter Sets: StandardSound, CustomSound
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Silent
Specifies that the toast should be displayed without sound.

```yaml
Type: SwitchParameter
Parameter Sets: Silent
Aliases:

Required: True
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

### None
### You cannot pipe input to this cmdlet.
## OUTPUTS

### Microsoft.Toolkit.Uwp.Notifications.ToastAudio
## NOTES

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BTAudio.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BTAudio.md)

