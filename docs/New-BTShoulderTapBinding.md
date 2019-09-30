---
external help file: BurntToast-help.xml
Module Name: BurntToast
online version: https://github.com/Windos/BurntToast/blob/master/Help/New-BTShoulderTapBinding.md
schema: 2.0.0
---

# New-BTShoulderTapBinding

## SYNOPSIS
Creates a new Shoulder Tap Binding object.

## SYNTAX

```
New-BTShoulderTapBinding [-Image] <ToastShoulderTapImage> [-AddImageQuery] [[-BaseUri] <Uri>]
 [[-Language] <String>] [<CommonParameters>]
```

## DESCRIPTION
The New-BTShoulderTapBinding function creates a new Shoulder Tap Binding Object, with which you can specify the Image to be displayed.

## EXAMPLES

### EXAMPLE 1
```
$Image = New-BTShoulderTapImage -Source 'https://www.route66sodas.com/wp-content/uploads/2019/01/Alert.gif'
```

New-BTShoulderTapBinding -Image $Image

## PARAMETERS

### -Image
The image displayed in the Shoulder Tap notification, this object is created using the New-BTShoulderTapImage function.

```yaml
Type: ToastShoulderTapImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddImageQuery
Set to "true" to allow Windows to append a query string to the image URI supplied in the Toast notification.
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
Position: 2
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
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### LOTS...
## OUTPUTS

### ToastBindingShoulderTap
## NOTES

## RELATED LINKS

[https://github.com/Windos/BurntToast/blob/master/Help/New-BTShoulderTapBinding.md](https://github.com/Windos/BurntToast/blob/master/Help/New-BTShoulderTapBinding.md)

