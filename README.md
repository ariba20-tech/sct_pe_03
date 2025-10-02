# Task Automation Prompting System

A web-based interface for semi-automating real-world tasks using AI prompting, designed for extracting structured data from unstructured text. This project was created for **TASK 03: Prompting for Task Automation**.

![Task Automation System](https://img.shields.io/badge/Project-Task%2003-blue)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

## 🚀 Live Demo

[View Live Demo](https://ariba20-tech.github.io/sct_pe_03)

## 📋 Features

- **Multiple Task Types**: Data extraction, text summarization, format transformation
- **Interactive Examples**: Pre-built examples demonstrating system capabilities
- **Clean Interface**: Modern, responsive design that works on all devices
- **Structured Output**: Consistent JSON formatting for reliable data processing
- **Real-time Processing**: Instant transformation of unstructured text to structured data

## 🛠️ Technologies Used

- **HTML5** - Semantic structure and accessibility
- **CSS3** - Modern styling with Grid, Flexbox, and CSS Variables
- **Vanilla JavaScript** - Client-side processing and interactivity
- **Git & GitHub** - Version control and deployment

## 📁 Project Structure

```
task-automation-system/
│
├── index.html              # Main application interface
├── README.md               # Project documentation (this file)
├── assets/                 # Additional resources
│   ├── images/             # Screenshots and graphics
│   ├── css/                # Stylesheets (if extracted)
│   └── js/                 # JavaScript modules (if extracted)
└── examples/               # Example data and test cases
    └── example-outputs.md  # Additional test cases
```

## 🎯 Task 03 Submission Details

### System Prompt
```text
You are a helpful assistant that extracts structured data from unstructured text. Extract the following information from the provided text and format it as a JSON object with the specified keys. If any information is missing, use null.

Required fields:
- name
- email
- phone
- company
- position
```

### Input-Output Examples

#### Example 1: Complete Information
**Input:**
```
Hello, I'm Sarah Johnson, Marketing Director at InnovateCo. Contact me at sarah.j@innovateco.com or 555-987-6543.
```

**Output:**
```json
{
  "name": "Sarah Johnson",
  "email": "sarah.j@innovateco.com",
  "phone": "555-987-6543",
  "company": "InnovateCo",
  "position": "Marketing Director"
}
```

#### Example 2: Missing Phone Number
**Input:**
```
Dr. Michael Chen, Professor at University of Tech. Email: mchen@unitech.edu. Research focus: AI and Machine Learning.
```

**Output:**
```json
{
  "name": "Dr. Michael Chen",
  "email": "mchen@unitech.edu",
  "phone": null,
  "company": "University of Tech",
  "position": "Professor"
}
```

#### Example 3: Dash-Separated Format
**Input:**
```
Alex Taylor - Software Engineer - Google - alex.taylor@google.com - 415-555-7890
```

**Output:**
```json
{
  "name": "Alex Taylor",
  "email": "alex.taylor@google.com",
  "phone": "415-555-7890",
  "company": "Google",
  "position": "Software Engineer"
}
```

## 🔧 Installation & Local Development

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- A code editor (VS Code, Sublime Text, etc.) - optional

### Quick Start
1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/task-automation-system.git
   cd task-automation-system
   ```

2. **Open the application**
   - Simply open `index.html` in your web browser, or
   - Use a local server for better performance:
     ```bash
     # Using Python 3
     python -m http.server 8000
     # Then visit http://localhost:8000
     ```

3. **Start using the system**
   - Select a task type from the dropdown
   - Enter your text in the input area
   - Click "Process Input" to see the structured output

## 📝 Reflection on Prompt Iteration

### Development Process
Creating an effective prompting system required multiple iterations and careful testing. The journey from initial concept to reliable system revealed several important insights about prompt engineering.

### Initial Challenges
- **Inconsistent Output Formats**: Early versions produced varying structures
- **Missing Data Handling**: The system struggled with incomplete information
- **Over-extraction**: Sometimes included irrelevant content from input text
- **Format Inconsistency**: Outputs varied between JSON, plain text, and other formats

### Iterative Improvements
1. **Explicit Format Specification**: Required JSON format with specific keys
2. **Null Handling Instructions**: Explicitly instructed to use `null` for missing data
3. **Field Definition**: Clearly listed required fields to prevent over-extraction
4. **Structured Examples**: Provided clear input-output pairs in the prompt itself
5. **Edge Case Testing**: Validated with various text structures and missing information

### Key Lessons Learned
- **Specificity is Crucial**: Vague prompts lead to unpredictable outputs
- **Examples Improve Reliability**: Clear demonstrations help the model understand expectations
- **Error Handling Matters**: Explicit instructions for missing data prevent incomplete outputs
- **Consistent Formatting**: Requesting specific formats (JSON) ensures machine-readable results
- **Testing is Essential**: Diverse test cases reveal weaknesses in prompt design

### Final Insights
The final prompt demonstrates remarkable consistency across different input formats while maintaining structured, reliable output. This project highlights how careful prompt design can transform unstructured text into valuable, structured data suitable for automation pipelines and data processing systems.

## 🎨 Customization

### Adding New Task Types
1. Modify the task type dropdown in `index.html`
2. Add corresponding system prompts in the JavaScript
3. Update the processing logic for the new task type

### Extending Data Fields
To extract additional information, modify the system prompt and processing logic:

```javascript
// Add new fields to the prompt
const extendedPrompt = `Extract the following information:
- name
- email
- phone
- company
- position
- department
- location
Format as JSON with null for missing values.`;
```

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Create a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👥 Author

**Your Name**
- GitHub: [ariba20-tech](https://github.com/yourusername)
- Project: Task Automation Prompting System

## 🙏 Acknowledgments

- Inspired by TASK 03: Prompting for Task Automation requirements
- Built with modern web standards and best practices
- Designed for reliability and user experience

---

**⭐ If you find this project helpful, please give it a star on GitHub!**

---

*Last updated: September 2025*
