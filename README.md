# Quiz Data Extractor

Extract quiz questions, answers, explanations, and results from online learning platforms into a clean JSON format.

## 📋 Features

- ✅ Extracts all questions with complete text (preserves code blocks)
- ✅ Captures all answer options with individual explanations
- ✅ Identifies correct answers clearly
- ✅ Shows your answers vs correct answers
- ✅ Handles both Multiple Choice and Multi-Select questions
- ✅ Includes overall explanations and domain/objective info
- ✅ Exports to clean JSON format

## 🚀 Quick Start

### Step 1: Complete Your Exam
Take your quiz/exam as normal and submit your answers.

### Step 2: Navigate to Review Page
After completing the exam, click the **"Review Questions"** button to see all questions with answers and explanations.

### Step 3: Expand All Questions (Important!)
Make sure all questions are expanded on the page so their answers are visible. If questions are collapsed:
- Scroll through the page
- Click to expand any collapsed questions
- Ensure you can see all answer options

### Step 4: Open Browser Console
**Windows/Linux:**
- Press `F12` OR
- Press `Ctrl + Shift + J` OR
- Right-click → "Inspect" → Click "Console" tab

**Mac:**
- Press `Cmd + Option + J` OR
- Right-click → "Inspect Element" → Click "Console" tab

### Step 5: Copy and Paste the Script
1. Open the `extractor.js` file from this repository
2. Copy the entire script (Ctrl+A, Ctrl+C)
3. Paste it into the browser console
4. Press `Enter`

### Step 6: Download Your Data
The script will automatically download a JSON file named `quiz-data-[timestamp].json` to your Downloads folder.

## 📊 Output Format

The JSON file contains an array of questions with this structure:

```json
[
  {
    "questionNumber": "Question 1",
    "questionType": "Multiple Choice",
    "status": "Correct",
    "question": "What is the capital of France?",
    "domain": "Geography - European Capitals",
    "yourAnswer": "Paris",
    "correctAnswer": "Paris",
    "allOptions": [
      {
        "option": "London",
        "isCorrect": false,
        "explanation": "London is the capital of the United Kingdom..."
      },
      {
        "option": "Paris",
        "isCorrect": true,
        "explanation": "Paris is the capital and largest city of France..."
      },
      {
        "option": "Berlin",
        "isCorrect": false,
        "explanation": "Berlin is the capital of Germany..."
      }
    ],
    "overallExplanation": "Paris has been the capital of France since..."
  }
]
```

### Multi-Select Questions

For questions with multiple correct answers:

```json
{
  "questionNumber": "Question 5",
  "questionType": "Multi-Select",
  "yourAnswer": ["Option A", "Option B"],
  "correctAnswer": ["Option A", "Option B", "Option C"],
  ...
}
```

## 📁 Repository Structure

```
quiz-data-extractor/
├── README.md           # This file
├── extractor.js        # Main extraction script
├── examples/
│   └── sample-output.json
└── LICENSE
```

## 🔧 Troubleshooting

### No questions extracted
- ✅ Make sure you're on the review/results page, not the quiz-taking page
- ✅ Ensure all questions are expanded (not collapsed)
- ✅ Scroll through the entire page to load all content

### Missing correct answers
- ✅ The page must show which answers are correct
- ✅ You must be viewing the review/results page, not just the exam

### Code blocks not preserved
- ✅ The script automatically preserves inline code as \`code\`
- ✅ Code blocks are preserved as \`\`\`code\`\`\`

### Script error in console
- ✅ Make sure you copied the entire script
- ✅ Try refreshing the page and running again
- ✅ Check if the page structure has changed

## 💡 Use Cases

- 📚 **Study Aid**: Review all questions and explanations offline
- 📊 **Analysis**: Analyze which question types you struggle with
- 🔄 **Backup**: Keep a record of your quiz attempts
- 📝 **Notes**: Create study materials from quiz content
- 🤖 **Processing**: Use JSON data with other tools or scripts

## ⚠️ Important Notes

1. **Ethical Use**: Only use this tool on your own quiz attempts for personal study
2. **Terms of Service**: Ensure you're not violating the platform's terms of service
3. **Copyright**: Quiz content may be copyrighted - use for personal study only
4. **Privacy**: Don't share extracted data publicly if it contains proprietary content

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🐛 Issues

If you encounter any issues or have suggestions, please open an issue on GitHub.

## ⭐ Show Your Support

If this tool helped you, give it a ⭐️!

---

**Note**: This tool is designed for educational purposes to help with personal study and review. Always respect the terms of service of the platform you're using.
