# Fake-News-Detector
# 🛡️ TruthGuard - Fake News Detector

An intelligent web-based fake news detection tool that analyzes articles and headlines to assess credibility. TruthGuard uses advanced pattern recognition and sentiment analysis to help you identify misinformation before you share it.

##  Table of Contents

- [Features](#features)
- [How It Works](#how-it-works)
- [Live Demo](#live-demo)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage Guide](#usage-guide)
- [Analysis Metrics](#analysis-metrics)
- [Project Structure](#project-structure)
- [API & Functions](#api--functions)
- [Report Generation](#report-generation)
- [Browser Support](#browser-support)
- [Contributing](#contributing)
- [License](#license)

##  Features

- **Real-Time Analysis**: Instant credibility assessment of news articles
- **Comprehensive Scoring System**:
  - Source Credibility Check
  - Writing Quality Analysis
  - Fact Verification Score
  - Bias Detection Meter
- **Detailed Reporting**: Get a full breakdown of what makes an article suspicious
- **PDF/HTML Report Export**: Download detailed analysis reports
- **Share Results**: Easy sharing of credibility assessments
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile
- **Sentiment Analysis**: Detects emotional manipulation in articles
- **Red Flag Detection**: Identifies common clickbait and misinformation patterns
- **Clean UI**: Intuitive, user-friendly interface with visual feedback
- **Animated Results**: Beautiful gradient backgrounds and smooth transitions

## 🔍 How It Works

TruthGuard analyzes articles using a multi-layered approach:

### 1. **Source Credibility Analysis**
- Checks if a legitimate source URL is provided
- Verifies domain authenticity patterns
- Scores source reliability based on known credible outlets

### 2. **Content Quality Assessment**
- Evaluates writing professionalism
- Checks for proper citations and quotes
- Analyzes use of numbers and statistics
- Detects proper nouns and named entities
- Identifies suspicious language patterns

### 3. **Fact Verification**
- Looks for red flag words (conspiracy, secret, miracle, etc.)
- Detects exaggerated claims
- Identifies unverifiable assertions
- Flags extreme or unlikely scenarios

### 4. **Bias & Manipulation Detection**
- Identifies clickbait headline patterns
- Detects emotional manipulation
- Analyzes sentiment (positive/negative/neutral)
- Flags sensationalist language
- Spots rhetorical manipulation tactics

### 5. **Overall Credibility Score**
Combines all metrics using weighted algorithm:
- Source Credibility: 30%
- Content Quality: 30%
- Fact Verification: 20%
- Bias Level: 20%

## 🎯 Verdict Categories

- **✅ Looks Pretty Legit (70%+)**: Article appears credible with professional writing
- **⚠️ Hmm, Better Be Careful (40-69%)**: Some red flags, needs verification
- **❌ Yeah... This Seems Sketchy (<40%)**: Multiple warning signs, likely misinformation

## 🚀 Live Demo

Try TruthGuard now! Open `index.html` in your browser to get started.

## 🛠️ Technologies Used

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Analysis**: Pattern Recognition, NLP-inspired text analysis
- **UI/UX**: CSS Grid, Flexbox, CSS Animations
- **Export**: HTML Report Generation, Blob API
- **Compatibility**: ES6+ JavaScript, Web APIs

## 📦 Installation

### Method 1: Direct Use

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/truthguard.git
   cd truthguard
   ```

2. **Open in browser**
   - Double-click `index.html` or
   - Right-click `index.html` → Open with Browser or
   - Use VS Code's Live Server extension

### Method 2: Local Server (Recommended)

**Using Python:**
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

Then open: `http://localhost:8000`

**Using Node.js (http-server):**
```bash
npm install -g http-server
http-server
```

**Using VS Code:**
- Install "Live Server" extension
- Right-click `index.html` → Open with Live Server

### Method 3: Deploy Online

**Using GitHub Pages:**
1. Push files to GitHub repository
2. Go to Settings → Pages
3. Select main branch as source
4. Your site will be live at `https://yourusername.github.io/truthguard`

## 📖 Usage Guide

### Step 1: Enter Article Information

```
1. Headline: Paste the news headline
2. Article Content: Paste the full article text
3. Source (Optional): Enter the website URL
```

### Step 2: Click "Let's Check This Out!"

The AI will analyze the article in real-time.

### Step 3: Review Results

You'll see:
- **Overall Credibility Score** (0-100%)
- **Detailed Verdict** with explanation
- **Four Analysis Metrics** with progress bars
- **Red Flags Found** listing suspicious patterns
- **Recommendations** for verification steps
- **Reading Statistics** (word count, reading time, sentiment)

### Step 4: Take Action

**Options after analysis:**
- **📥 Save Full Report**: Download detailed HTML report
- **📤 Share This**: Share results with friends
- **🔄 Check Another**: Analyze another article

## 📊 Analysis Metrics

### Source Check (30% weight)
**What it measures:**
- Legitimacy of provided URL
- Known credible news outlets
- Domain age and reputation
- Previous fact-checking records

**Score interpretation:**
- 80-100%: Highly credible source
- 50-79%: Moderate credibility
- 0-49%: Questionable source

### Writing Quality (30% weight)
**What it measures:**
- Professional writing standards
- Proper grammar and punctuation
- Citation and quote usage
- Use of statistics and data
- Presence of journalistic elements

**Red flags:**
- Excessive exclamation marks
- ALL CAPS text
- Poor spelling/grammar
- Sensationalist adjectives

### Fact Check (20% weight)
**What it measures:**
- Presence of verifiable claims
- Use of credible sources
- Likelihood of factual accuracy
- Suspicious language patterns

**Suspicious keywords detected:**
- "Shocking", "Unbelievable", "Miracle"
- "Secret", "They don't want you to know"
- "Conspiracy", "Doctors hate"
- "One weird trick"

### Bias Meter (20% weight)
**What it measures:**
- Political or ideological slant
- Emotional manipulation tactics
- Cherry-picked information
- One-sided reporting

**Detection methods:**
- Clickbait headline patterns
- Emotional language analysis
- Sentiment distribution
- Argumentative techniques

## 📁 Project Structure

```
truthguard/
├── index.html          # Main HTML file with UI structure
├── style.css           # Styling and animations
├── script.js           # Core analysis and functionality
├── .gitignore          # Git ignore rules
├── requirements.txt    # Project dependencies (reference)
├── launch.json         # VS Code debugger config (optional)
└── README.md          # This file
```

## 🔌 API & Functions

### Main Functions

#### `analyzeNews()`
Triggers the analysis process when user clicks the button.
- **Input**: User-entered headline, content, and source
- **Output**: Displays analysis results with verdicts

#### `performAnalysis(headline, content, source)`
Core analysis function that processes all metrics.
```javascript
const analysis = performAnalysis(headline, content, source);
// Returns: analysis object with all scores and details
```

#### `displayResults(analysis)`
Renders analysis results in the UI.
```javascript
displayResults(analysis);
// Updates progress bars, scores, and detailed report
```

#### `downloadReport()`
Generates and downloads an HTML report.
```javascript
downloadReport();
// Creates formatted report with styling
```

#### `shareResults()`
Shares results via native share API or clipboard.
```javascript
shareResults();
// Copies to clipboard or uses navigator.share
```

#### `analyzeSentiment(text)`
Analyzes emotional tone of the article.
```javascript
const sentiment = analyzeSentiment(content);
// Returns: 'Positive', 'Negative', or 'Neutral'
```

#### `reset()`
Clears form and results for next analysis.
```javascript
reset();
// Resets all fields and hides results
```

## 📄 Report Generation

### What's Included in Downloaded Reports:

✅ Header with timestamp
✅ Overall credibility score with color-coded verdict
✅ AI explanation of findings
✅ Original article information (headline, source, preview)
✅ Detailed metric breakdown with progress bars
✅ Reading statistics (word count, reading time, sentiment)
✅ Red flags identified
✅ Recommendations for verification
✅ Disclaimer and usage notes
✅ Professional styling and formatting

### Report Format:
- **File Type**: HTML (self-contained, no external dependencies)
- **File Name**: `TruthGuard-Report-[timestamp].html`
- **Print-Friendly**: Optimized for printing to PDF
- **File Size**: Typically 50-100 KB

## 🌐 Browser Support

| Browser | Version | Support |
|---------|---------|---------|
| Chrome | Latest | ✅ Full |
| Firefox | Latest | ✅ Full |
| Safari | Latest | ✅ Full |
| Edge | Latest | ✅ Full |
| Opera | Latest | ✅ Full |
| IE | 11 | ⚠️ Limited |

**Note:** Uses modern JavaScript (ES6+), Web APIs, and CSS Grid. For IE11 support, would require transpilation.

## 🎨 Customization

### Change Color Scheme

Edit CSS variables in `style.css`:

```css
/* Main gradient colors */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Change to your colors */
background: linear-gradient(135deg, #FF6B6B 0%, #FF8E53 100%);
```

### Modify Suspicious Words List

In `script.js`, update the `suspiciousWords` array:

```javascript
const suspiciousWords = ['shocking', 'unbelievable', 'your-word-here'];
```

### Adjust Scoring Weights

Modify the weights in the `performAnalysis` function:

```javascript
const overallScore = (
    sourceCredibility * 0.3 +      // Change 0.3
    contentQuality * 0.3 +         // Change 0.3
    factVerification * 0.2 +       // Change 0.2
    biasLevel * 0.2                // Change 0.2
);
```

### Change Verdict Thresholds

Modify score ranges in `performAnalysis`:

```javascript
if (overallScore >= 70) {           // Change 70
    // Legit verdict
} else if (overallScore >= 40) {    // Change 40
    // Uncertain verdict
} else {
    // Fake verdict
}
```

## 💡 How Analysis Scoring Works

### Scoring Algorithm

**Example Calculation:**
```
Article Analysis:
- Source URL provided → +65%
- 800 words (above average) → +30% toward content quality
- 8 quotes found → +15% toward content quality
- 0 suspicious words → no penalty
- Clickbait headline detected → -8% toward content quality
- Content Quality = 50 + 30 + 15 + 0 - 8 = 87%

Final Score = (65 × 0.3) + (87 × 0.3) + (55 × 0.2) + (60 × 0.2)
           = 19.5 + 26.1 + 11 + 12
           = 68.6% → "Better Be Careful" ⚠️
```

## 🧪 Testing

### Test Cases Provided:

**Legitimate Article:**
- Headline: "Scientists Discover New Species in Amazon Rainforest"
- Content: Detailed scientific findings with quotes and data
- Expected: 70%+ score, "Looks Pretty Legit" verdict

**Suspicious Article:**
- Headline: "You Won't Believe What This Celebrity Does at Home!"
- Content: Clickbait language, "one weird trick", unverified claims
- Expected: <40% score, "This Seems Sketchy" verdict

**Uncertain Article:**
- Headline: Regular news headline
- Content: Mixed quality with some sources and some unverified claims
- Expected: 40-69% score, "Better Be Careful" verdict

## 🐛 Known Limitations

- **Local Analysis**: All analysis is performed client-side without accessing external APIs
- **Language**: Currently optimized for English language articles
- **Real-Time Fact Checking**: Cannot verify claims against live databases
- **No ML Model**: Uses pattern recognition, not machine learning
- **Source Verification**: Limited to URL pattern analysis, not actual verification
- **Context Awareness**: Cannot understand nuanced context or satire detection

## 🚀 Future Enhancements

 Integration with real fact-checking APIs (Snopes, FactCheck.org)
 Multi-language support
 Machine learning model for improved accuracy
 User accounts and saved analysis history
 Analytics dashboard for trending misinformation
 Advanced NLP for context understanding
 Custom keyword lists for specific domains
 Mobile app (React Native)
 Browser extension for real-time detection
 Cloud integration for distributed analysis

## 🤝 Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Make your improvements
4. Commit changes (`git commit -m 'Add your feature'`)
5. Push to branch (`git push origin feature/YourFeature`)
6. Open a Pull Request

**Ideas for contribution:**
- Improve detection algorithms
- Add more suspicious word patterns
- Enhance UI/UX
- Add new language support
- Create analysis visualizations
- Write tests
- Improve documentation

## 📝 License

This project is open source and available under the MIT License.

## 📧 Support & Feedback

- Found a bug? Open an issue on GitHub
- Have suggestions? Create a feature request
- Want to contribute? See contributing section above

---

##  Educational Purpose

TruthGuard was created to help people understand misinformation and develop critical thinking skills. It demonstrates:

- Pattern recognition in text
- Sentiment analysis basics
- Client-side web application development
- UI/UX design principles
- Data visualization techniques
- Responsive web design

## ⚖️ Disclaimer

**Important:** TruthGuard provides pattern-based analysis to assist in identifying potentially misleading content. It is:

   A helpful second opinion
   A learning tool for media literacy
   A starting point for investigation

**But it is NOT:**

  A replacement for professional fact-checkers
  100% accurate
  Able to verify facts against real databases
  A legal authority on truth

**Always:**
   Verify important information through multiple trusted sources
   Check original sources and citations
   Use critical thinking
   Consult professional fact-checking organizations

## 🔗 Helpful Resources

- [Snopes.com](https://www.snopes.com/) - Fact-checking database
- [FactCheck.org](https://www.factcheck.org/) - Non-partisan fact-checking
- [PolitiFact](https://www.politifact.com/) - Political claim verification
- [NewsGuard](https://www.newsguardtech.com/) - News source ratings
- [Media Literacy Council](https://www.medialiteracycouncil.sg/) - Misinformation guide

---

**Fight misinformation. Think critically. Share responsibly. 🛡️**

**Questions? Issues? Ideas? We'd love to hear from you!**
