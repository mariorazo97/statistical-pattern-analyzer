# Contributing to Statistical Pattern Analyzer

First off, thank you for considering contributing to Statistical Pattern Analyzer! It's people like you that make this educational tool better for everyone.

## 🎯 Our Mission

This project aims to make complex statistical concepts accessible and understandable through interactive visualizations. We welcome contributions that advance this educational mission.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Guidelines](#development-guidelines)
- [Style Guidelines](#style-guidelines)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)

## 📜 Code of Conduct

### Our Standards

- Be respectful and inclusive
- Welcome newcomers and help them learn
- Focus on what is best for the educational community
- Show empathy towards other community members

### Unacceptable Behavior

- Harassment or discriminatory language
- Trolling or insulting comments
- Public or private harassment
- Publishing others' private information
- Other conduct inappropriate in a professional setting

## 🤝 How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues. When creating a bug report, include:

- **Clear title and description**
- **Steps to reproduce** the issue
- **Expected behavior** vs actual behavior
- **Screenshots** if applicable
- **Browser/OS information**

Example:
```markdown
**Bug**: Entropy calculation shows NaN on empty dataset

**Steps to Reproduce**:
1. Open the application
2. Clear all data
3. Click "Run Full Analysis"

**Expected**: Error message or graceful handling
**Actual**: Displays "NaN" in entropy score

**Browser**: Chrome 120.0, Windows 11
```

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion:

- **Use a clear title** describing the enhancement
- **Provide detailed description** of the proposed functionality
- **Explain why this enhancement would be useful** to users
- **Include mockups or examples** if applicable

### Contributing Code

#### Good First Issues

Look for issues labeled `good-first-issue` - these are perfect for newcomers!

Areas great for beginners:
- Documentation improvements
- Adding comments to code
- UI/UX enhancements
- Additional chart types
- Accessibility improvements

#### More Advanced Contributions

- New statistical methods
- Performance optimizations
- Complex algorithm implementations
- Architecture improvements

## 💻 Development Guidelines

### Prerequisites

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Basic text editor or IDE
- Understanding of HTML5, CSS3, and JavaScript ES6+

### Setting Up Development Environment

1. **Fork the repository** on GitHub

2. **Clone your fork**:
   ```bash
   git clone https://github.com/mariorazo97/statistical-pattern-analyzer.git
   cd statistical-pattern-analyzer
   ```

3. **Create a branch**:
   ```bash
   git checkout -b feature/your-feature-name
   ```

4. **Open the HTML file** in your browser and start coding!

### Testing Your Changes

Since this is a single-file HTML application:

1. Open `statistical_pattern_analyzer.html` in your browser
2. Test all functionality thoroughly
3. Test in multiple browsers (Chrome, Firefox, Safari, Edge)
4. Test on mobile devices if possible
5. Verify no console errors appear

### Key Areas to Test

- [ ] Data generation works correctly
- [ ] All charts render properly
- [ ] Mathematical calculations are accurate
- [ ] UI remains responsive
- [ ] No JavaScript errors in console
- [ ] Mobile/tablet view works
- [ ] Custom data input validation works
- [ ] All buttons and controls function

## 🎨 Style Guidelines

### JavaScript Style

```javascript
// Use const/let, not var
const myConstant = 10;
let myVariable = 20;

// Use meaningful variable names
const historicalDataArray = [];  // Good
const hda = [];                   // Bad

// Use camelCase for variables and functions
function calculateEntropy() { }   // Good
function calculate_entropy() { }  // Bad

// Add comments for complex logic
// Calculate normalized Shannon entropy
const entropy = -sum(probabilities.map(p => p * Math.log2(p)));

// Use template literals for strings
const message = `Analysis complete: ${result}`;  // Good
const message = 'Analysis complete: ' + result;   // Bad

// Handle errors gracefully
try {
    performCalculation();
} catch (error) {
    console.error('Calculation failed:', error);
    showNotification('Error in calculation', 'danger');
}
```

### CSS Style

```css
/* Use CSS custom properties for colors */
:root {
    --primary-color: #00d4ff;
}

/* Use meaningful class names */
.analysis-section { }        /* Good */
.as { }                      /* Bad */

/* Add comments for complex sections */
/* Responsive grid for analysis cards */
.analysis-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
}
```

### HTML Style

```html
<!-- Use semantic HTML -->
<section class="analysis-section">  <!-- Good -->
<div class="analysis-section">      <!-- Less ideal -->

<!-- Add ARIA labels for accessibility -->
<button aria-label="Run statistical analysis">Analyze</button>

<!-- Keep indentation consistent (2 or 4 spaces) -->
```

## 📝 Commit Guidelines

### Commit Message Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- **feat**: New feature
- **fix**: Bug fix
- **docs**: Documentation changes
- **style**: Code style changes (formatting, no logic change)
- **refactor**: Code refactoring
- **perf**: Performance improvements
- **test**: Adding tests
- **chore**: Maintenance tasks

### Examples

```bash
feat(entropy): add rolling window entropy calculation

Implement sliding window entropy calculation to show
entropy trends over time. Uses configurable window size.

Closes #42

---

fix(benford): correct chi-square calculation

Fixed off-by-one error in degrees of freedom calculation
for Benford's Law chi-square test.

---

docs(readme): update installation instructions

Add troubleshooting section for common browser issues.
```

## 🔄 Pull Request Process

### Before Submitting

1. ✅ Test your changes thoroughly
2. ✅ Update documentation if needed
3. ✅ Follow style guidelines
4. ✅ Write clear commit messages
5. ✅ Ensure no console errors
6. ✅ Test on multiple browsers

### Submitting Pull Request

1. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

2. **Create Pull Request** on GitHub

3. **Fill out the PR template**:
   ```markdown
   ## Description
   Brief description of changes
   
   ## Type of Change
   - [ ] Bug fix
   - [ ] New feature
   - [ ] Documentation update
   - [ ] Performance improvement
   
   ## Testing
   - [ ] Tested in Chrome
   - [ ] Tested in Firefox
   - [ ] Tested on mobile
   - [ ] No console errors
   
   ## Screenshots
   (if applicable)
   
   ## Related Issues
   Closes #123
   ```

4. **Wait for review** - maintainers will review and provide feedback

### Review Process

- Maintainers will review within 1-2 weeks
- You may be asked to make changes
- Once approved, your PR will be merged!

## 🎓 Educational Focus

Remember, this project is educational. Contributions should:

- ✅ Help users understand statistical concepts
- ✅ Include clear explanations and documentation
- ✅ Be mathematically accurate
- ✅ Include visual aids when possible
- ❌ Not promote gambling or prediction of random events
- ❌ Not include misleading statistical claims

## 💡 Ideas for Contributions

### Easy
- Add tooltips to charts
- Improve mobile responsiveness
- Add more color schemes
- Translate to other languages
- Improve accessibility (ARIA labels, keyboard navigation)

### Medium
- Add new chart types
- Implement data export (CSV, JSON)
- Add animation to visualizations
- Create comparison mode between datasets
- Add statistical test results explanations

### Advanced
- Implement Bayesian inference visualization
- Add regression analysis
- Create interactive formula editor
- Implement time-series forecasting demos
- Add collaborative features

## 📚 Resources

- [Chart.js Documentation](https://www.chartjs.org/docs/)
- [MDN Web Docs](https://developer.mozilla.org/)
- [Statistics How To](https://www.statisticshowto.com/)
- [Khan Academy - Statistics](https://www.khanacademy.org/math/statistics-probability)

## ❓ Questions?

- Open an issue with the `question` label
- Join discussions in GitHub Discussions
- Review existing documentation

## 🙏 Thank You!

Your contributions help make statistical education more accessible to everyone. Every contribution, no matter how small, is valuable!

---

**Happy Contributing! 🎉**