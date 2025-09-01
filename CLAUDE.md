# Git Commit Rules

## Commit Guidelines

### 1. Atomic Commits
- Each commit should represent a single, complete change
- If a change affects multiple areas, consider breaking it into separate commits
- Commits should be self-contained and not break the build

### 2. Single Line Commit Messages
- Keep commit messages to a single line (under 50 characters when possible)
- Use the imperative mood (e.g., "Fix bug" not "Fixed bug" or "Fixes bug")
- Start with a capital letter
- Do not end with a period

### 3. Gitmoji Usage
Use gitmoji to categorize commits visually:

- ✨ `:sparkles:` New features
- 🐛 `:bug:` Bug fixes
- 📚 `:books:` Documentation
- 🎨 `:art:` Code style/formatting
- ⚡ `:zap:` Performance improvements
- 🔧 `:wrench:` Configuration changes
- 🧪 `:test_tube:` Tests
- 🚀 `:rocket:` Deployments
- 🔒 `:lock:` Security fixes
- ♻️ `:recycle:` Refactoring
- 🗑️ `:wastebasket:` Remove code/files
- 🔨 `:hammer:` Build system changes

### Examples
```
✨ Add user authentication system
🐛 Fix login form validation
📚 Update API documentation
🎨 Format code with prettier
⚡ Optimize database queries
🔧 Update build configuration
```

### Commands
- `./gradlew lint` - Run lint checks
- `./gradlew test` - Run tests
- `./gradlew build` - Build the project