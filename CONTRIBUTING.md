# Contributing to DOOM Eternal Offline Setup Assistant

🔥 Thank you for considering contributing to the DOOM Eternal Offline Setup Assistant! Your help makes this project better for everyone.

## 🎯 Ways to Contribute

### 🐛 Bug Reports
Found a bug? Help us fix it!
- Check [existing issues](https://github.com/DOOM-Eternal-Offline-Setup-Assistant/doom-eternal-offline-setup-assistant/issues) first
- Use the bug report template
- Include system specs and error messages
- Add screenshots if helpful

### 💡 Feature Requests
Have an idea for improvement?
- Check [discussions](https://github.com/DOOM-Eternal-Offline-Setup-Assistant/doom-eternal-offline-setup-assistant/discussions) first
- Use the feature request template
- Explain the use case and benefits
- Consider implementation complexity

### 🔧 Code Contributions
Want to submit code changes?
- Fork the repository
- Create a feature branch
- Follow coding standards
- Add tests if applicable
- Submit a pull request

### 📚 Documentation
Help improve our docs!
- Fix typos and grammar
- Add missing information
- Improve clarity and structure
- Translate to other languages

## 🚀 Getting Started

### Prerequisites
- Windows 10/11 development environment
- Visual Studio 2022 or VS Code
- .NET Framework 4.8 or later
- Git for version control

### Development Setup
1. **Fork and clone the repository**
   ```bash
   git clone https://github.com/YOUR-USERNAME/doom-eternal-offline-setup-assistant.git
   cd doom-eternal-offline-setup-assistant
   ```

2. **Set up development environment**
   ```bash
   # Install dependencies
   dotnet restore
   
   # Build the project
   dotnet build
   ```

3. **Run tests**
   ```bash
   dotnet test
   ```

### Making Changes
1. **Create a branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make your changes**
   - Follow the coding style guide
   - Add comments for complex logic
   - Update documentation if needed

3. **Test your changes**
   - Run existing tests
   - Add new tests for new features
   - Test on different Windows versions

4. **Commit your changes**
   ```bash
   git add .
   git commit -m "feat: add new feature description"
   ```

## 📋 Pull Request Process

### Before Submitting
- [ ] Code follows project style guidelines
- [ ] Tests pass locally
- [ ] Documentation updated if needed
- [ ] Commit messages follow conventional format
- [ ] No merge conflicts with main branch

### PR Requirements
1. **Clear description** of what changes were made
2. **Link to related issues** using keywords (fixes #123)
3. **Screenshots** for UI changes
4. **Testing instructions** for reviewers
5. **Breaking changes** clearly documented

### Review Process
1. **Automated checks** must pass (CI/CD)
2. **Code review** by maintainers
3. **Testing** by community members
4. **Approval** from project maintainers
5. **Merge** into main branch

## 🎨 Coding Standards

### Code Style
- Use **C# naming conventions**
- **4 spaces** for indentation
- **PascalCase** for classes and methods
- **camelCase** for variables and fields
- **Clear, descriptive** variable names

### Comments
```csharp
/// <summary>
/// Configures DOOM Eternal graphics settings based on hardware detection
/// </summary>
/// <param name="hardwareInfo">Detected hardware specifications</param>
/// <returns>Optimized graphics configuration</returns>
public GraphicsConfig ConfigureGraphics(HardwareInfo hardwareInfo)
{
    // Auto-detect optimal settings based on GPU benchmarks
    var optimalSettings = GraphicsOptimizer.GetOptimalSettings(hardwareInfo.GPU);
    
    // Apply conservative settings for older hardware
    if (hardwareInfo.GPU.Year < 2018)
    {
        optimalSettings.ApplyConservativeMode();
    }
    
    return optimalSettings;
}
```

### Error Handling
```csharp
try
{
    // Risky operation
    var result = RiskyOperation();
    return result;
}
catch (SpecificException ex)
{
    // Log the error with context
    Logger.LogError($"Failed to execute operation: {ex.Message}", ex);
    
    // Provide user-friendly error message
    throw new UserFriendlyException("Setup failed. Please check system requirements.", ex);
}
```

## 🏷️ Commit Message Format

We use [Conventional Commits](https://www.conventionalcommits.org/) format:

```
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

### Types
- **feat**: New feature
- **fix**: Bug fix
- **docs**: Documentation changes
- **style**: Code style changes
- **refactor**: Code refactoring
- **test**: Adding tests
- **chore**: Maintenance tasks

### Examples
```
feat(installer): add automatic hardware detection

- Detect GPU and CPU specifications
- Configure optimal graphics settings
- Add fallback for unknown hardware

Closes #123
```

## 🧪 Testing Guidelines

### Unit Tests
- Test all public methods
- Mock external dependencies
- Use descriptive test names
- Follow AAA pattern (Arrange, Act, Assert)

```csharp
[Test]
public void ConfigureGraphics_WithHighEndGPU_ReturnsUltraSettings()
{
    // Arrange
    var hardwareInfo = new HardwareInfo { GPU = new GPU { Model = "RTX 3080" } };
    var optimizer = new GraphicsOptimizer();
    
    // Act
    var config = optimizer.ConfigureGraphics(hardwareInfo);
    
    // Assert
    Assert.AreEqual(GraphicsQuality.Ultra, config.Quality);
    Assert.IsTrue(config.RayTracingEnabled);
}
```

### Integration Tests
- Test complete workflows
- Use real system components where possible
- Clean up test artifacts

### Manual Testing
- Test on different Windows versions
- Verify with different hardware configurations
- Check all supported game versions

## 🔒 Security Guidelines

### Sensitive Information
- Never commit API keys or tokens
- Use environment variables for secrets
- Sanitize user inputs
- Validate file paths and names

### Code Security
- Avoid shell injection vulnerabilities
- Validate all external inputs
- Use secure file operations
- Handle permissions properly

## 📞 Getting Help

### Communication Channels
- 💬 [Discord Server](https://discord.gg/doomassistant) - General discussion
- 🐛 [GitHub Issues](https://github.com/DOOM-Eternal-Offline-Setup-Assistant/doom-eternal-offline-setup-assistant/issues) - Bug reports
- 💡 [GitHub Discussions](https://github.com/DOOM-Eternal-Offline-Setup-Assistant/doom-eternal-offline-setup-assistant/discussions) - Feature requests
- 📧 [Email](mailto:contributors@doom-assistant.com) - Private matters

### Code of Conduct
This project follows the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md). Please read it before participating.

## 🏆 Recognition

### Contributors
All contributors are recognized in:
- GitHub contributors list
- Release notes
- Project documentation
- Community spotlights

### Contribution Types
We recognize all types of contributions:
- 💻 Code
- 📖 Documentation
- 🎨 Design
- 🐛 Bug reports
- 💡 Ideas
- 🤔 Feedback
- 🌍 Translations

## 📊 Project Stats

### Current Status
- ![Contributors](https://img.shields.io/github/contributors/DOOM-Eternal-Offline-Setup-Assistant/doom-eternal-offline-setup-assistant)
- ![Issues](https://img.shields.io/github/issues/DOOM-Eternal-Offline-Setup-Assistant/doom-eternal-offline-setup-assistant)
- ![Pull Requests](https://img.shields.io/github/issues-pr/DOOM-Eternal-Offline-Setup-Assistant/doom-eternal-offline-setup-assistant)

### Milestones
- 🎯 **v1.0**: Basic offline setup functionality
- 🎯 **v1.5**: Advanced graphics optimization
- 🎯 **v2.0**: Multi-game support
- 🎯 **v2.5**: Linux compatibility layer

---

## 🎮 Happy Contributing!

Thank you for helping make DOOM Eternal more accessible to everyone! Your contributions help fellow gamers enjoy this amazing game offline.

**Rip and tear... through bugs and features!** 🔥

---

*This guide is inspired by the DOOM community's passion for gaming freedom and accessibility.* 