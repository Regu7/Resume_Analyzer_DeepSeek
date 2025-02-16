# Resume Analyzer

A Streamlit-based application that analyzes resumes using GROQ LLM API (deepseek-r1-distill-qwen-32b) and stores results in AWS DynamoDB. The analyzer provides comprehensive insights including match scores, qualification analysis, and improvement suggestions.

## Demo Screenshots

![Upload Page](screenshots/upload_page.png)
*Resume upload interface with job description input*

![Analysis Results](screenshots/analysis_results.png)
*Detailed analysis showing match score and qualifications*

![Skills Analysis](screenshots/skills_analysis.png)
*Breakdown of matching and missing skills*

## Features

- Resume matching score (0-100)
- Key qualifications analysis
- Identification of missing skills and requirements
- Candidate strengths assessment
- Areas for improvement highlights
- Actionable resume enhancement suggestions
- Automatic storage of analysis results in AWS DynamoDB

## Prerequisites

- Python 3.8+
- AWS Account with DynamoDB access
- GROQ API key
- Conda or Python virtual environment

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/resume-analyzer.git
cd resume-analyzer
```

2. Create and activate a virtual environment:

Using Conda:
```bash
conda create -n resume-analyzer python=3.8
conda activate resume-analyzer
```

OR using venv:
```bash
python -m venv venv
# On Windows
.\venv\Scripts\activate
# On Unix or MacOS
source venv/bin/activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the project root directory with your credentials:
```plaintext
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
AWS_REGION=your_aws_region
GROQ_API_KEY=your_groq_api_key
```

## Usage

1. Start the Streamlit application:
```bash
streamlit run main.py
```

2. Open your web browser and navigate to the provided local URL (typically http://localhost:8501)

3. Upload a resume file and wait for the analysis results

## Project Structure

```
resume-analyzer/
├── main.py
├── requirements.txt
├── .env
├── README.md
├── screenshots/           # Add this directory for storing app images
│   ├── upload_page.png
│   ├── analysis_results.png
│   └── skills_analysis.png
└── utils/
    ├── __init__.py
    ├── analyzer.py
    ├── aws_utils.py
    └── llm_utils.py
```

## Adding Screenshots

To add your own screenshots to the README:

1. Create a `screenshots` directory in your project root:
```bash
mkdir screenshots
```

2. Take screenshots of your application (recommended resolutions):
   - Full page screenshots: 1200x800 px
   - Feature highlights: 800x600 px
   - Modal windows: 600x400 px

3. Save your screenshots in PNG format with descriptive names:
   - upload_page.png
   - analysis_results.png
   - skills_analysis.png

4. Add screenshots to your README using Markdown syntax:
```markdown
![Description](screenshots/image_name.png)
*Caption text explaining the feature*
```

5. Optimize images before adding them:
   - Compress PNG files using tools like TinyPNG
   - Keep file sizes under 500KB for better loading
   - Maintain aspect ratios when resizing

## Dependencies

Key dependencies include:
- streamlit
- boto3
- python-dotenv
- groq
- pandas

Full list of dependencies can be found in `requirements.txt`

## Environment Variables

Required environment variables in `.env` file:
- `AWS_ACCESS_KEY_ID`: Your AWS access key
- `AWS_SECRET_ACCESS_KEY`: Your AWS secret access key
- `AWS_REGION`: AWS region for DynamoDB
- `GROQ_API_KEY`: Your GROQ API key

## Contributing

1. Fork the repository
2. Create a new branch for your feature
3. Commit your changes
4. Push to the branch
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please open an issue in the GitHub repository or contact [your-email@example.com]
