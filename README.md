# 🔬 Statistical Pattern Analyzer

> An educational web application demonstrating advanced statistical analysis methods for random number distributions.

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support%20Development-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/quizmybrai7)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?logo=chart.js&logoColor=white)](https://www.chartjs.org/)

## 📋 Overview

The **Statistical Pattern Analyzer** is a comprehensive educational tool that demonstrates various mathematical and statistical analysis techniques on random number distributions. It visualizes complex concepts like Benford's Law, Shannon Entropy, Markov Chains, Monte Carlo Simulations, and Fourier Transforms in an interactive, easy-to-understand format.

This tool is designed for:
- **Students** learning probability theory and statistics
- **Educators** teaching mathematical concepts
- **Data Scientists** exploring statistical analysis methods
- **Anyone** interested in understanding randomness and pattern detection

## ✨ Features

### 📊 Statistical Methods Implemented

1. **Benford's Law Analysis**
   - Compares first-digit distribution against theoretical Benford curve
   - Chi-Square goodness-of-fit test
   - Visual deviation detection

2. **Shannon Entropy Calculation**
   - Measures randomness quality in datasets
   - Normalized entropy scoring (0-1 scale)
   - Rolling window entropy visualization

3. **Markov Chain Analysis**
   - Transition probability matrix calculation
   - Sequential pattern detection
   - Top transition relationships visualization

4. **Monte Carlo Simulation**
   - Configurable iteration counts (500-10,000)
   - Probability distribution modeling
   - Match probability estimation

5. **Fourier Transform (DFT)**
   - Periodic pattern detection
   - Frequency spectrum analysis
   - Cycle identification in time series

6. **Frequency Distribution Analysis**
   - Chi-Square test for uniformity
   - Number occurrence tracking
   - Deviation from expected distribution

7. **Hot & Cold Number Analysis**
   - Recency-weighted scoring
   - Gap analysis between appearances
   - Visual hot/cold mapping

### 🎮 Interactive Features

- **Mock Data Generation**: Generate 100-1000 simulated historical draws
- **Custom Data Input**: Add up to 30 custom records manually
- **Real-Time Analysis**: Instant statistical computations and visualizations
- **Statistical Predictions**: Generate predictions based on composite scoring
- **Responsive Design**: Works on desktop, tablet, and mobile devices

### 🎨 User Interface

- **Dark Mode Design**: Easy on the eyes, professional appearance
- **Interactive Charts**: Powered by Chart.js for smooth, responsive visualizations
- **Color-Coded Indicators**: Green (normal), Yellow (anomaly), Red (danger)
- **Mathematical Formulas**: Display of actual formulas used in calculations
- **Educational Explanations**: Detailed "How It Works" sections for each method

## 🚀 Quick Start

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/mariorazo97/statistical-pattern-analyzer.git
   cd statistical-pattern-analyzer
   ```

2. **Open the application:**
   ```bash
   # Simply open the HTML file in your browser
   open statistical_pattern_analyzer.html
   
   # Or on Linux/Windows:
   xdg-open statistical_pattern_analyzer.html  # Linux
   start statistical_pattern_analyzer.html     # Windows
   ```

That's it! No installation, no dependencies, no build process required.

### Usage

1. **Automatic Start**: The application generates 500 mock draws and runs initial analysis on load
2. **Generate New Data**: Click "Generate New Mock Data" to create fresh random datasets
3. **Run Analysis**: Click "Run Full Analysis" to execute all statistical methods
4. **Generate Prediction**: Click "Generate Statistical Prediction" to create a composite-scored prediction
5. **Add Custom Data**: Click "Input Custom Data" to manually add your own historical records

## 📊 Data Format

### Game Types Supported

- **5-Ball Game (1-69) + Bonus (1-26)**: Standard 5-from-69 format
- **5-Ball Game (1-70) + Bonus (1-25)**: Alternative 5-from-70 format

### Custom Data Entry

When adding custom data, enter:
- 5 main numbers (must be unique)
- 1 bonus number
- Numbers must be within valid range for selected game type

## 🔬 Mathematical Methods Explained

### Benford's Law

Benford's Law states that in many naturally occurring datasets, smaller digits appear as leading digits more frequently:

```
P(d) = log₁₀(1 + 1/d)
```

Where `d` ∈ {1, 2, 3, ..., 9}

### Shannon Entropy

Measures the unpredictability or randomness in a dataset:

```
H(X) = -Σ p(x) × log₂(p(x))
Normalized: H_norm = H(X) / log₂(N)
```

Higher entropy = more randomness (max = 1.0)

### Markov Chain

Models the probability of transitioning from one state to another:

```
P(X_t = j | X_{t-1} = i)
```

Calculates conditional probability that number `j` appears given `i` appeared previously.

### Monte Carlo Simulation

Uses repeated random sampling to estimate probabilities:

```
P(event) ≈ (# favorable outcomes) / (# total simulations)
```

### Discrete Fourier Transform

Decomposes time series into frequency components:

```
X(k) = Σ x(n) × e^(-i2πkn/N)
Magnitude = √(Real² + Imaginary²)
```

### Chi-Square Test

Tests for uniformity in distribution:

```
χ² = Σ((Observed - Expected)² / Expected)
```

## 🛠️ Technical Details

### Technologies Used

- **HTML5**: Structure and content
- **CSS3**: Styling with CSS Grid and Flexbox
- **JavaScript (ES6+)**: All statistical computations and interactivity
- **Chart.js 4.4.0**: Data visualization library (via CDN)

### Browser Compatibility

- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Opera

Requires modern browser with ES6+ support.

### File Structure

```
statistical-pattern-analyzer/
├── statistical_pattern_analyzer.html    # Main application (single file)
├── README.md                             # This file
├── LICENSE                               # MIT License
└── .gitignore                           # Git ignore rules
```

## ⚠️ Important Disclaimers

### Educational Purpose Only

This tool is designed **exclusively for educational purposes** to demonstrate:
- Statistical analysis techniques
- Probability theory concepts
- Mathematical modeling methods
- Data visualization best practices

### Randomness and Prediction

**Critical Understanding:**
- In truly random systems, past results do **NOT** predict future outcomes
- No statistical method can overcome inherent randomness
- Patterns in random data are often coincidental
- This tool demonstrates analysis techniques, not prediction capabilities

### Not for Gambling

This application:
- ❌ Cannot predict lottery outcomes
- ❌ Cannot improve odds in games of chance
- ❌ Should not be used for gambling decisions
- ✅ Is designed to teach statistical concepts

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/AmazingFeature`
3. **Commit your changes**: `git commit -m 'Add some AmazingFeature'`
4. **Push to the branch**: `git push origin feature/AmazingFeature`
5. **Open a Pull Request**

### Areas for Contribution

- Additional statistical methods (e.g., Bayesian analysis, regression)
- Performance optimizations
- Mobile UI improvements
- Additional visualization types
- Internationalization (i18n)
- Accessibility improvements
- Documentation enhancements

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Chart.js** for excellent data visualization library
- **Statistical community** for mathematical methods and formulas
- **Open source contributors** who make projects like this possible

## 📚 Educational Resources

Learn more about the concepts demonstrated:

- [Benford's Law](https://en.wikipedia.org/wiki/Benford%27s_law) - Wikipedia
- [Shannon Entropy](https://en.wikipedia.org/wiki/Entropy_(information_theory)) - Wikipedia
- [Markov Chains](https://en.wikipedia.org/wiki/Markov_chain) - Wikipedia
- [Monte Carlo Method](https://en.wikipedia.org/wiki/Monte_Carlo_method) - Wikipedia
- [Fourier Transform](https://en.wikipedia.org/wiki/Discrete_Fourier_transform) - Wikipedia
- [Chi-Square Test](https://en.wikipedia.org/wiki/Chi-squared_test) - Wikipedia

### ☕ Support This Project

If you find this tool helpful, consider supporting its development:

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-Support%20Development-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/quizmybrai7)

![GitHub stars](https://img.shields.io/github/stars/mariorazo97/statistical-pattern-analyzer?style=social)
![GitHub forks](https://img.shields.io/github/forks/mariorazo97/statistical-pattern-analyzer?style=social)



## 📞 Contact & Support

- **Issues**: Please use the [GitHub Issues](https://github.com/mariorazo97/statistical-pattern-analyzer/issues) page
- **Discussions**: Join the conversation in [GitHub Discussions](https://github.com/mariorazo97/statistical-pattern-analyzer/discussions)

## 🌟 Star History

If you find this project useful, please consider giving it a star ⭐️!

## 📈 Roadmap

Future enhancements under consideration:

- [ ] Export analysis results to PDF/CSV
- [ ] Historical comparison features
- [ ] Additional statistical tests (Kolmogorov-Smirnov, Anderson-Darling)
- [ ] Machine learning pattern recognition
- [ ] Real-time collaboration features
- [ ] API for programmatic access
- [ ] Mobile app version

---

**Made with ❤️ for education and statistical literacy**

*Remember: Mathematics can analyze randomness, but cannot predict it.*
