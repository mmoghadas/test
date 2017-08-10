# Thread-Resigner

This repository provides instructions and tools to resign Thread packages

## Requirements
- This repository
- MacOS

## Signing MacOS Thread Packages

### Signing Thread
> Update the variable below with path to the file to be signed
> ```bash
> export IDENTITY='Developer ID Application: Tactile, Inc.'
> export IDENTIFIER='com.tactile.Thread-Mac'
> export FILE='Thread.app'
> codesign --force --sign "$IDENTITY" --identifier "$IDENTIFIER" "$FILE"
> codesign --verify --verbose Thread.app
> ```

> Alternatively, you can use the script provided
> 1. Place the Thread.app in `Images/Mac/Input`
> 2. Run the below script.
> 3. The signed file will be generated in `Images/Mac/Output`.
> ```bash
> ./scripts/mac.sh
> ```


### Signing Thread for GE
> Update the variable below with path to the file to be signed
> ```bash
> export IDENTITY='Developer ID Application: Tactile, Inc.'
> export IDENTIFIER='com.tactile.Thread-Mac-GE'
> export FILE='Thread 3.app'
> codesign --force --sign "$IDENTITY" --identifier "$IDENTIFIER" "$FILE"
> codesign --verify --verbose Thread.app
> ```

> Alternatively, you can use the script provided
> 1. Place the Thread.app in `Images/Mac-GE/Input`
> 2. Run the below script.
> 3. The signed file will be generated in `Images/Mac-GE/Output`.
> ```bash
> ./scripts/mac-ge.sh
> ```
