---
external help file: Bicep-help.xml
Module Name: Bicep
online version:
schema: 2.0.0
---

# Build-Bicep

## SYNOPSIS
Builds one or more .bicep files.

## SYNTAX

### Default (Default)
```powershell
Build-Bicep [[-Path] <String>] [[-OutputDirectory] <String>] [-ExcludeFile <String[]>] [-GenerateParameterFile]
 [<CommonParameters>]
```

### AsString
```powershell
Build-Bicep [[-Path] <String>] [[-OutputDirectory] <String>] [-ExcludeFile <String[]>] [-AsString]
 [<CommonParameters>]
```

## DESCRIPTION
**Build-Bicep** is equivalent to the Bicep CLI command 'bicep build' but with some additional features.

-Compile all files in a directory
-Generate ARM Template Parameter files
-Output ARM Template directly as string without writing to file

## EXAMPLES

### Example 1: Compile single bicep file in working directory
```powershell
Build-Bicep -Path vnet.bicep
```

### Example 2: Compile single bicep file and specify the output directory
```powershell
Build-Bicep -Path 'c:\bicep\modules\vnet.bicep' - -OutputDirectory 'c:\armtemplates\vnet.bicep'
```

### Example 3: Compile all .bicep files in a directory
```powershell
Build-Bicep -Path 'c:\bicep\modules\'
```

### Example 4: Compile all .bicep files in the working directory except vnet.bicep
```powershell
Build-Bicep -Path 'c:\bicep\modules\' -ExcludeFile vnet.bicep
```

### Example 5: Compile a .bicep file and output as string
```powershell
Build-Bicep -Path '.\vnet.bicep' -AsString
```

### Example 6: Compile a .bicep files in the working directory and generate a parameter files
```powershell
Build-Bicep -Path '.\vnet.bicep' -GenerateParameterFile
```

## PARAMETERS

### -Path
Specfies the path to the directory or file that should be compiled

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: $pwd.path
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputDirectory
Specfies the target directory where the compiled files should be created

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

### -ExcludeFile
Specifies a .bicep file to exclude from compilation

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GenerateParameterFile
The -GenerateParameterFile switch generates a ARM Template parameter file for the compiled template

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsString
The -AsString prints all output as a string instead of corresponding files.

```yaml
Type: SwitchParameter
Parameter Sets: AsString
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

## OUTPUTS

## NOTES
Go to module repository https://github.com/StefanIvemo/BicepPowerShell for detailed info, reporting issues and to submit contributions.

## RELATED LINKS
