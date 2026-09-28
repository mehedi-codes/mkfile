# mkfile PowerShell Function

`mkfile` is a PowerShell function that creates one or more files in the specified paths. If a directory does not exist, it will be created automatically.

## Installation

You can load the function in your current PowerShell session:

```powershell
. .\mkfile.ps1
```

To make it available in every PowerShell session, add the following line to your PowerShell profile:

```powershell
. "C:\path\to\mkfile.ps1"
```

Then reload the profile:

```powershell
. $PROFILE
```

## Usage

```powershell
# Create a file in the current directory
mkfile index.html

# Create a file in a specific directory
mkfile src/main.ts

# Create multiple files
mkfile app/settings.json docs/README.md

# Show version information
mkfile -v

# Show function information
mkfile -i
```

## Examples

```powershell
# Create a nested file structure
mkfile src/components/Button.tsx

# If the folder does not exist, it will be created automatically
# Output: Directory 'C:\path\to\src\components' created.
# Output: File 'C:\path\to\src\components\Button.tsx' created successfully.
```

## Contributing

If you find any issues or have suggestions for improvements, feel free to open an issue or submit a pull request in the GitHub repository.
