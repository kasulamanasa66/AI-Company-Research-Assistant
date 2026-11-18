# AI-Company-Research-Assistant
An AI-powered company research and outreach assistant that uses web scraping and Google Gemini to research companies, generate personalised outreach emails, and send approved emails through Gmail SMTP using a Streamlit interface.

## Project Overview

The AI-Powered Company Research & Outreach Assistant is a Python-based web application that combines web scraping, Generative AI, and email automation to simplify company research and personalized business communication.

Users can enter a company's website URL along with relevant sender, recipient, and outreach details. The application extracts publicly accessible website information, uses Google Gemini to generate company research and business insights, and creates personalized professional outreach emails.

The application also integrates Gmail SMTP to send emails after explicit user approval.

## Key Features

- **Website Scraping:** Extracts publicly accessible website content using Requests and BeautifulSoup.
- **AI-Powered Company Research:** Uses Google Gemini to analyze company information and generate business insights.
- **Personalized Email Generation:** Generates professional outreach emails based on company research and the provided sender and recipient details.
- **Research Report Download:** Allows users to download company research reports in Markdown format.
- **Email Download:** Allows users to download generated outreach emails in TXT format.
- **Gmail SMTP Integration:** Sends approved outreach emails through Gmail.
- **User Approval:** Requires explicit user approval before sending an email.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Application development |
| Streamlit | Web application interface |
| Requests | Website content retrieval |
| BeautifulSoup | HTML parsing and content extraction |
| Google Gemini API | Company research and email generation |
| Gmail SMTP | Email delivery |
| Google Colab | Development and testing environment |

## Application Workflow

1. The user enters a company website URL.
2. The application retrieves publicly accessible website content.
3. BeautifulSoup extracts relevant information from the website.
4. Extracted information is processed using Google Gemini.
5. Gemini generates company research and business insights.
6. The application generates a personalized outreach email using the research and user-provided details.
7. Users can review and download the research report and generated email.
8. After reviewing and approving the email, users can send it through Gmail SMTP.

## Project Structure

```text
AI-Company-Research-Assistant/
│
├── app.py
├── requirements.txt
├── README.md
└── AI_Company_Research_Assistant.ipynb
```

## Installation and Setup

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd AI-Company-Research-Assistant
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure API Credentials

The application requires the following credentials:

- Google Gemini API Key
- Gmail Sender Email Address
- Gmail App Password

Configure the following environment variables securely:

```text
GEMINI_API_KEY
GMAIL_SENDER_EMAIL
GMAIL_APP_PASSWORD
```

Never expose API keys or Gmail App Passwords in source code or public repositories.

### 4. Run the Application

```bash
streamlit run app.py
```

Open the local application URL provided by Streamlit.

## Security Considerations

- API credentials are configured through environment variables or secure notebook secrets.
- Gmail authentication uses an App Password rather than the regular Gmail account password.
- Emails are sent only after explicit user approval.
- The application retrieves publicly accessible website information.

## Future Enhancements

- Implement automatic retry mechanisms for temporary AI service failures.
- Improve error handling and preserve completed research during temporary failures.
- Support additional AI models.
- Enhance the application interface.
- Deploy the application on a public hosting platform.
- Extend company research capabilities using additional information sources.

## Project Outcome

The project demonstrates the integration of web scraping, Generative AI, and email automation into an end-to-end business research and outreach workflow.

It showcases how Large Language Models (LLMs) can assist with company analysis, business opportunity identification, and personalized professional communication while maintaining human approval before email delivery.
