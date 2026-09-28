![mkfile](https://socialify.git.ci/mehedi-codes/mkfile/image?description=1&font=KoHo&forks=1&issues=1&language=1&name=1&pattern=Solid&stargazers=1&theme=Auto)

---

**mkfile** is a powerful, lightweight PowerShell utility that streamlines file and directory creation. Whether you're scaffolding new projects, organizing directories, or automating workflows, mkfile eliminates repetitive manual file creation with a single command.

Perfect for developers, DevOps engineers, and anyone who spends time setting up file structures manually.

---

## 🚀 Features

✅ **Create Single or Multiple Files** - Add one file or dozens in a single command  
✅ **Auto-Create Parent Directories** - No more manual folder creation  
✅ **Nested Path Support** - Create deeply nested file structures instantly  
✅ **Path Safety** - Prevents accidental file creation outside your working directory  
✅ **Simple & Intuitive** - Minimal learning curve, maximum productivity  
✅ **Cross-Friendly** - Works with relative paths and complex directory structures  
✅ **Lightweight** - Zero dependencies, pure PowerShell  

---

## 📋 Requirements

- **Windows 10+** or **Windows Server 2016+**
- **PowerShell 5.1+** (included by default on all supported Windows versions)
- **Administrator Access** (optional, depending on target directory permissions)

---

## ⚡ Quick Start

### 1. Load mkfile

```powershell
. .\mkfile.ps1
```

### 2. Start Creating Files

```powershell
# Single file
mkfile index.html

# Multiple files
mkfile index.html style.css script.js

# Nested structure (directories auto-created)
mkfile src/components/Button.tsx src/styles/Button.css
```

That's it! Files are created instantly.

---

## 📦 Installation

### Method 1: Direct Usage (Simplest)

1. Download `mkfile.ps1` from this repository
2. Place it in your project directory
3. Load it in your PowerShell session:

```powershell
. .\mkfile.ps1
```

### Method 2: Add to PowerShell Profile (Recommended)

Make mkfile available in **every** PowerShell session:

```powershell
# Open your PowerShell profile
notepad $PROFILE

# Add this line to the file
. "C:\path\to\mkfile.ps1"

# Save and close

# Reload your profile
. $PROFILE
```

Now you can use `mkfile` from any directory!

### Method 3: Add to System PATH

1. Save `mkfile.ps1` to a permanent location (e.g., `C:\Scripts\`)
2. Add that folder to your Windows PATH environment variable
3. Create a shortcut batch file in your PowerShell scripts folder

---

## 💡 Usage Guide

### Basic Syntax

```powershell
mkfile [OPTIONS] <file_path> [<file_path2>] [<file_path3>]...
```

### Common Use Cases

#### Create a Single File
```powershell
mkfile README.md
mkfile index.html
mkfile config.json
```

#### Create Multiple Files at Once
```powershell
mkfile app.js style.css index.html manifest.json
```

#### Create Files in Subdirectories
```powershell
# Creates 'src' directory automatically
mkfile src/main.ts
mkfile src/index.tsx

# Creates nested directories
mkfile src/components/Button/Button.tsx
mkfile src/components/Button/Button.css
mkfile src/components/Button/index.ts
```

#### Mix Files and Directories
```powershell
mkfile src/App.tsx public/index.html docs/API.md config/settings.json
```

#### View Version
```powershell
mkfile -v
# Output: v1.1.0
```

#### View Function Info
```powershell
mkfile -i
# Output: mkfile: A PowerShell function to create files.
#         Repository: https://github.com/mehedi-codes/mkfile
#         Author: mehedi-codes
#         Version: v1.1.0
```

---

## 🎯 Real-World Examples

### Example 1: Bootstrap a React Project

```powershell
mkfile public/index.html `
         src/App.tsx `
         src/index.tsx `
         src/App.css `
         src/components/Header/Header.tsx `
         src/components/Header/Header.css `
         .env.local `
         .gitignore `
         README.md
```

### Example 2: Create a Node.js Project Structure

```powershell
mkfile src/server.js `
         src/routes/api.js `
         src/middleware/auth.js `
         src/config/database.js `
         tests/server.test.js `
         .env `
         .env.example `
         package.json
```

### Example 3: Organize Documentation

```powershell
mkfile docs/Getting-Started.md `
         docs/API/Authentication.md `
         docs/API/Users.md `
         docs/API/Products.md `
         docs/CONTRIBUTING.md
```

### Example 4: Setup a Python Project

```powershell
mkfile src/__init__.py `
         src/main.py `
         src/utils/helpers.py `
         tests/test_main.py `
         requirements.txt `
         README.md `
         .gitignore
```

---

## ⚙️ Advanced Features

### Auto-Create Directories
If a directory in the path doesn't exist, mkfile creates it automatically:

```powershell
mkfile very/deeply/nested/structure/file.txt
# Creates all directories if they don't exist
# Output: Directory 'C:\...\very\deeply\nested\structure' created.
#         File 'C:\...\very\deeply\nested\structure\file.txt' created successfully.
```

### Skip Existing Files
If a file already exists, mkfile skips it gracefully:

```powershell
mkfile existing_file.txt
# Output: File 'C:\path\to\existing_file.txt' already exists.
```

### Error Handling
mkfile provides clear error messages:

```powershell
mkfile ../../../outside/project/file.txt
# Output: Error: Target path is outside the current working directory.
```

---

## 🔒 Security

- **Path Containment**: mkfile prevents creation of files outside the current working directory
- **Safe Permissions**: Respects Windows file permissions
- **No Elevation Required**: Works within user permissions (unless accessing restricted directories)
- **Error Reporting**: Clear feedback on what went wrong

---

## 🤝 Contributing

Found a bug? Have a feature request? We'd love your help!

1. [Report an Issue](https://github.com/mehedi-codes/mkfile/issues)
2. [Submit a Pull Request](https://github.com/mehedi-codes/mkfile/pulls)
3. Check out [open issues](https://github.com/mehedi-codes/mkfile/issues) for ways to contribute

---

## 💬 Feedback & Support

- **Questions?** Open a [GitHub Discussion](https://github.com/mehedi-codes/mkfile/discussions)
- **Bug Report?** Create an [Issue](https://github.com/mehedi-codes/mkfile/issues)
- **Feature Request?** Let us know in [Discussions](https://github.com/mehedi-codes/mkfile/discussions)

---

## 📊 Why mkfile?

| Feature | mkfile | mkdir -p | New-Item |
|---------|--------|----------|----------|
| Create Files | ✅ | ❌ | ✅ |
| Auto-Create Dirs | ✅ | ✅ | ❌ |
| Multiple Files | ✅ | ❌ | ⚠️ Verbose |
| Ease of Use | ⭐⭐⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐ |
| Speed | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ |

---

## 📝 Version History

**v1.1.0** (Current)
- Improved error handling
- Better directory creation logic
- Enhanced path safety
- Cleaner output messages

---

## 📄 License Information

This project is provided as-is for community use. See the repository for more details.
