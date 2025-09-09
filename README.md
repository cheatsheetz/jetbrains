# JetBrains IDEs Cheat Sheet

## Overview of JetBrains IDEs

### IDE Family
- **IntelliJ IDEA** - Java, Kotlin, Scala, Groovy
- **PyCharm** - Python, Django, Flask, data science
- **WebStorm** - JavaScript, TypeScript, React, Vue, Angular
- **PhpStorm** - PHP, Laravel, Symfony, WordPress
- **RubyMine** - Ruby, Ruby on Rails
- **CLion** - C/C++, CMake, embedded development
- **GoLand** - Go development
- **Rider** - .NET, C#, F#, VB.NET, Unity
- **DataGrip** - Database IDE
- **AppCode** - iOS/macOS development (discontinued)

## Installation and Setup

### JetBrains Toolbox (Recommended)
```bash
# Download and install JetBrains Toolbox
# Available at: https://www.jetbrains.com/toolbox-app/

# Linux installation
wget https://download.jetbrains.com/toolbox/jetbrains-toolbox-[version].tar.gz
tar -xzf jetbrains-toolbox-[version].tar.gz
./jetbrains-toolbox

# macOS
brew install --cask jetbrains-toolbox

# Windows
winget install JetBrains.Toolbox
```

### Individual IDE Installation
```bash
# IntelliJ IDEA Community
snap install intellij-idea-community --classic

# PyCharm Community  
snap install pycharm-community --classic

# WebStorm (requires license)
snap install webstorm --classic
```

## Universal Keyboard Shortcuts

### Navigation
| Shortcut | Action |
|----------|---------|
| `Double Shift` | Search Everywhere |
| `Ctrl+Shift+A` | Find Action |
| `Ctrl+N` | Go to Class |
| `Ctrl+Shift+N` | Go to File |
| `Ctrl+Alt+Shift+N` | Go to Symbol |
| `Ctrl+E` | Recent Files |
| `Ctrl+Shift+E` | Recently Edited Files |
| `Ctrl+B` | Go to Declaration |
| `Ctrl+Alt+B` | Go to Implementation |
| `Ctrl+U` | Go to Super Method |
| `Alt+F7` | Find Usages |
| `Ctrl+F7` | Find Usages in File |

### Editing
| Shortcut | Action |
|----------|---------|
| `Ctrl+D` | Duplicate Line |
| `Ctrl+Y` | Delete Line |
| `Ctrl+Shift+Up/Down` | Move Line Up/Down |
| `Ctrl+W` | Extend Selection |
| `Ctrl+Shift+W` | Shrink Selection |
| `Alt+J` | Add Selection for Next Occurrence |
| `Alt+Shift+J` | Unselect Occurrence |
| `Ctrl+Alt+Shift+J` | Select All Occurrences |
| `Tab` | Indent |
| `Shift+Tab` | Unindent |
| `Ctrl+/` | Comment/Uncomment Line |
| `Ctrl+Shift+/` | Block Comment |

### Code Generation
| Shortcut | Action |
|----------|---------|
| `Alt+Insert` | Generate Code |
| `Ctrl+O` | Override Methods |
| `Ctrl+I` | Implement Methods |
| `Ctrl+Alt+T` | Surround With |
| `Ctrl+J` | Insert Live Template |
| `Ctrl+Shift+Enter` | Complete Current Statement |

### Refactoring
| Shortcut | Action |
|----------|---------|
| `Shift+F6` | Rename |
| `F6` | Move |
| `F5` | Copy |
| `Ctrl+Alt+M` | Extract Method |
| `Ctrl+Alt+V` | Extract Variable |
| `Ctrl+Alt+C` | Extract Constant |
| `Ctrl+Alt+F` | Extract Field |
| `Ctrl+Alt+P` | Extract Parameter |
| `Ctrl+Alt+N` | Inline |
| `Ctrl+Shift+Alt+T` | Refactor This |

### Running and Debugging
| Shortcut | Action |
|----------|---------|
| `Shift+F10` | Run |
| `Shift+F9` | Debug |
| `Ctrl+F2` | Stop |
| `F9` | Resume Program |
| `F8` | Step Over |
| `F7` | Step Into |
| `Shift+F8` | Step Out |
| `Alt+F9` | Run to Cursor |
| `Ctrl+F8` | Toggle Breakpoint |
| `Ctrl+Shift+F8` | View Breakpoints |

### Search and Replace
| Shortcut | Action |
|----------|---------|
| `Ctrl+F` | Find |
| `F3` | Find Next |
| `Shift+F3` | Find Previous |
| `Ctrl+R` | Replace |
| `Ctrl+Shift+F` | Find in Path |
| `Ctrl+Shift+R` | Replace in Path |
| `Ctrl+F3` | Find Word at Cursor |

### Window Management
| Shortcut | Action |
|----------|---------|
| `Alt+1` | Project Tool Window |
| `Alt+2` | Bookmarks |
| `Alt+3` | Find Tool Window |
| `Alt+4` | Run Tool Window |
| `Alt+5` | Debug Tool Window |
| `Alt+6` | Problems Tool Window |
| `Alt+7` | Structure Tool Window |
| `Alt+8` | Services Tool Window |
| `Alt+9` | Version Control |
| `Alt+0` | Messages |
| `Shift+Escape` | Hide Active Tool Window |
| `Ctrl+Shift+F12` | Hide All Tool Windows |

## Common Features

### Code Completion
```java
// Smart completion examples
List<String> list = new ArrayList<>();  // Ctrl+Shift+Space suggests ArrayList
list.stream().filter(s -> s.length() > 3).collect(toList());  // Auto-completion

// Postfix completion
list.for  // Expands to for loop
obj.null  // Expands to if (obj == null)
expr.var  // Extracts variable
```

### Live Templates
```text
Common Live Templates:
- psvm → public static void main(String[] args)
- sout → System.out.println()
- iter → for (Type item : collection)
- inst → instanceof
- psf → public static final
- thr → throw new 

Custom Template Creation:
1. File → Settings → Editor → Live Templates
2. Click + to add template group
3. Click + to add template
4. Define abbreviation, template text, and context
```

### Code Inspection
```text
Inspection Categories:
- Code smell detection
- Potential bugs
- Performance issues
- Security vulnerabilities
- Code style violations
- Spelling and grammar

Configuration:
File → Settings → Editor → Inspections
- Enable/disable specific inspections
- Set severity levels (Error, Warning, Weak Warning)
- Configure inspection profiles
- Customize inspection scopes
```

### Version Control Integration
```text
Supported VCS:
- Git (primary)
- Subversion
- Mercurial
- Perforce

Git Features:
- Visual diff and merge
- Interactive rebase
- Cherry-pick
- Branch management
- Stash management
- GitHub/GitLab integration
```

## Project Configuration

### Project Structure
```text
Project Settings (Ctrl+Alt+Shift+S):
├── Project
│   ├── Project SDK
│   ├── Project Language Level
│   └── Project Compiler Output
├── Modules
│   ├── Sources
│   ├── Paths
│   └── Dependencies
├── Libraries
├── Facets
├── Artifacts
└── Problems
```

### SDK Configuration
```text
Configure SDKs:
1. File → Project Structure → Platform Settings → SDKs
2. Click + to add new SDK
3. Select SDK type (Java, Python, etc.)
4. Choose installation directory
5. Verify SDK home and version

Auto-detection:
- JetBrains IDEs automatically detect common SDKs
- Use "Detect SDKs" button for bulk detection
```

### Build Systems
```text
Supported Build Systems:
- Maven
- Gradle  
- SBT (Scala)
- npm/Yarn (JavaScript)
- pip/Poetry (Python)
- Bundler (Ruby)
- CMake (C/C++)
- Go modules

Configuration:
- Build tools auto-imported from project files
- Manual configuration in Project Structure
- Build tool settings in Preferences
```

## Plugins and Extensions

### Essential Plugins (Cross-IDE)
```text
Productivity:
- Key Promoter X - Learn shortcuts
- String Manipulation - Text transformation
- Rainbow Brackets - Bracket colorization
- GitToolBox - Enhanced Git integration
- CodeGlance - Minimap
- Grep Console - Log highlighting

Database:
- Database Tools and SQL (bundled in Ultimate)
- Redis (for Redis support)

Themes and UI:
- Material Theme UI
- Dracula Theme
- One Dark theme
- Atom Material Icons

Code Quality:
- SonarLint - Static analysis
- CheckStyle-IDEA - Java code style
- SpotBugs - Bug detection
- PMD - Code analysis

Language Support:
- Rust - Rust language support
- Go - Go language support (if not using GoLand)
- Scala - Scala support (if not using IntelliJ Ultimate)
```

### Plugin Management
```text
Installation:
1. File → Settings → Plugins
2. Browse Marketplace or search
3. Install and restart IDE

Development:
1. Create plugin project with Plugin DevKit
2. Use IntelliJ Platform SDK
3. Test in sandbox environment
4. Publish to JetBrains Marketplace
```

## Advanced Configuration

### IDE Settings
```text
Essential Settings (Ctrl+Alt+S):

Editor → General:
- Change font size with mouse wheel
- Show line numbers
- Show method separators
- Auto-import settings

Editor → Code Style:
- Language-specific formatting
- Import EditorConfig support
- Code generation templates

Editor → Inspections:
- Enable/disable code analysis
- Configure severity levels
- Custom inspection profiles

Build, Execution, Deployment:
- Compiler settings
- Build tool configurations
- Deployment configurations

Tools:
- Terminal settings
- SSH configurations
- Database connections
```

### Performance Tuning
```text
Memory Settings (Help → Change Memory Settings):
- Increase heap size for large projects
- Default: 2GB, recommended: 4-8GB for large codebases

VM Options:
-Xmx8g                    # Maximum heap size
-XX:ReservedCodeCacheSize=1g  # Code cache for better performance
-XX:+UseConcMarkSweepGC   # Garbage collection optimization

Registry Settings (Help → Find Action → Registry):
- ide.max.intellisense.filesize: Increase for large files
- compiler.automake.allow.when.app.running: Background compilation
- editor.zero.latency.typing: Reduce typing latency
```

### Keymap Customization
```text
Keymap Settings:
1. File → Settings → Keymap
2. Choose base keymap (Default, Eclipse, VS Code, etc.)
3. Search for actions to modify
4. Right-click to add/remove shortcuts
5. Resolve conflicts

Popular Keymaps:
- Default (JetBrains)
- Eclipse
- Visual Studio Code
- Emacs
- Vim (with IdeaVim plugin)

Export/Import:
- Export custom keymaps for sharing
- Import from other JetBrains IDEs
```

## Database Tools (Ultimate Edition)

### Database Integration
```text
Supported Databases:
- MySQL, PostgreSQL, Oracle
- SQL Server, SQLite
- MongoDB, Redis
- Apache Cassandra
- Amazon Redshift

Connection Setup:
1. Database tool window (right sidebar)
2. Click + to add data source
3. Configure connection parameters
4. Test connection
5. Download missing drivers if prompted
```

### SQL Development
```sql
-- Query console features
SELECT * FROM users WHERE created_at > '2023-01-01';

-- Auto-completion for:
-- - Table names
-- - Column names  
-- - SQL keywords
-- - Database functions

-- Code generation:
-- - INSERT statements from table structure
-- - SELECT statements with all columns
-- - UPDATE and DELETE templates

-- Query execution:
-- - Run single query: Ctrl+Enter
-- - Run all queries: Ctrl+Shift+F10
-- - Explain plan visualization
-- - Query result export
```

## Team Collaboration

### Code Sharing
```text
Features:
- Code With Me (pair programming)
- Share project via VCS
- Export/Import settings
- Plugin synchronization

Code With Me:
1. Tools → Code With Me → Start Session
2. Share invitation link
3. Set permissions (view/edit)
4. Voice chat integration
```

### Settings Synchronization
```text
Settings Repository:
1. File → Settings Repository
2. Connect to Git repository
3. Merge or overwrite settings
4. Auto-sync across machines

IDE Settings Sync:
1. File → Settings → Settings Sync
2. Login with JetBrains account
3. Choose what to sync
4. Enable automatic synchronization
```

## Best Practices

### Project Organization
```text
Structure Guidelines:
- Use meaningful module names
- Organize source roots properly
- Configure output directories
- Set up proper test directories
- Use build tool conventions

Code Style:
- Configure team code style
- Use EditorConfig for consistency
- Enable format on save
- Set up inspection profiles
- Use consistent naming conventions
```

### Performance Optimization
```text
IDE Performance:
- Exclude unnecessary directories from indexing
- Use power save mode for basic editing
- Increase memory allocation
- Disable unused plugins
- Use local history sparingly

Large Projects:
- Enable shared indexes
- Use selective VCS refresh
- Configure appropriate inspection scopes
- Use file watchers judiciously
```

### Debugging Tips
```text
Effective Debugging:
- Use conditional breakpoints
- Leverage evaluate expression
- Use method breakpoints for interfaces
- Set up exception breakpoints
- Use drop frame feature
- Master step filtering
```

## Troubleshooting

### Common Issues
```text
Indexing Problems:
1. File → Invalidate Caches and Restart
2. Delete .idea directory and reimport
3. Check excluded directories
4. Verify project SDK configuration

Performance Issues:
1. Increase memory allocation
2. Check system resources
3. Disable unused plugins
4. Clear caches
5. Check antivirus exclusions

Plugin Conflicts:
1. Start in safe mode
2. Disable recently installed plugins
3. Check plugin compatibility
4. Update to latest versions
```

### Log Files and Diagnostics
```text
Log Locations:
- Windows: %APPDATA%\JetBrains\[IDE]\log
- macOS: ~/Library/Logs/JetBrains/[IDE]
- Linux: ~/.cache/JetBrains/[IDE]/log

Diagnostic Tools:
- Help → Collect Logs and Diagnostic Data
- Help → Show Log in Explorer/Finder
- Thread dumps for performance analysis
- Memory dumps for memory issues
```

## License and Pricing

### License Types
```text
Community Edition:
- Free and open source
- Available for IntelliJ IDEA and PyCharm
- Basic features for learning and small projects

Ultimate/Professional:
- Commercial license required
- Full feature set
- Enterprise integrations
- Premium support

Educational License:
- Free for students and teachers
- All Ultimate features
- Verification required
```

## Official Resources

- [JetBrains Official Documentation](https://www.jetbrains.com/help/)
- [IntelliJ IDEA Documentation](https://www.jetbrains.com/help/idea/)
- [Plugin Development](https://plugins.jetbrains.com/docs/intellij/)
- [JetBrains Marketplace](https://plugins.jetbrains.com/)
- [JetBrains Blog](https://blog.jetbrains.com/)
- [Community Forums](https://intellij-support.jetbrains.com/hc/en-us/community/topics)
- [Issue Tracker](https://youtrack.jetbrains.com/)
- [Educational Resources](https://www.jetbrains.com/academy/)