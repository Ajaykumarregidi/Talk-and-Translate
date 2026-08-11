# 🎙️ Talk and Translate

A simple speech translation web application built with **Python and Streamlit**.

The application allows users to select an input language and a target language, record speech, convert speech to text, translate the text, and generate translated audio.

## ✨ Features

* 🎤 Speech recording
* 📝 Speech-to-text conversion
* 🌐 Multiple language support
* 🤖 AI-based text translation
* 🔊 Text-to-speech output
* ⬇️ Download translated audio
* 🎨 Simple Streamlit interface
* 🌍 Designed for web deployment

## 🛠️ Technology Stack

* **Python**
* **Streamlit** – Web application interface
* **SpeechRecognition** – Speech-to-text processing
* **Google Gemini** – Text translation
* **gTTS** – Text-to-speech conversion

## 📁 Project Structure

```text
Talk-and-Translate/
│
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
│
└── .streamlit/
    └── config.toml
```

## ⚙️ Requirements

Python 3.11 or a compatible supported Python version is recommended.

Required Python packages are listed in:

```text
requirements.txt
```

Install them with:

```bash
pip install -r requirements.txt
```

A virtual environment is recommended for local development, but it should **not** be uploaded to GitHub.

## 🔐 API Key

The Gemini API key should **never be written directly into `app.py` or committed to GitHub**.

For local Streamlit development, use:

```text
.streamlit/secrets.toml
```

Example:

```toml
GEMINI_API_KEY = "YOUR_API_KEY"
```

Make sure this file is included in `.gitignore`.

The application can then access the key through Streamlit secrets.

## ▶️ Run Locally

Open PowerShell and navigate to the project folder:

```powershell
cd F:\Ajay\Talk-and-Translate
```

Install the dependencies:

```powershell
pip install -r requirements.txt
```

Start Streamlit:

```powershell
streamlit run app.py
```

Then open:

```text
http://localhost:8501
```

## 🌐 Deployment

The application can be deployed to a cloud hosting service that supports Streamlit.

For Streamlit Community Cloud:

1. Push the project to GitHub.
2. Open Streamlit Community Cloud.
3. Select the GitHub repository.
4. Select the branch containing the public version.
5. Select `app.py` as the main file.
6. Add `GEMINI_API_KEY` through Streamlit Secrets.
7. Deploy the application.

After deployment, the application can be accessed through a public web URL.

## 🎤 Microphone

For a public web application, microphone recording should use the **user's browser microphone** rather than trying to access a microphone attached to the cloud server.

The recommended Streamlit approach is:

```python
st.audio_input()
```

This allows each visitor to provide audio through their own browser.

## 🔒 Security

Do not commit any of the following files or information:

```text
venv/
.venv/
.streamlit/secrets.toml
API keys
passwords
private credentials
```

Use environment variables or Streamlit Secrets for sensitive information.

## 🚀 Future Improvements

* Real-time translation
* Better recording controls
* More languages
* Translation history
* User interface improvements
* Faster speech processing

## 📄 License

This project is for educational and development purposes.
