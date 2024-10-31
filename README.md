# 🛡️ OpenScreen

**Advanced Privacy Scrubbing for Screen Parsing and Action Models**

OpenScreen is a dedicated module designed to detect and scrub PII/PHI data from screen captures and action logs, enhancing privacy across applications like [OpenAdapt](https://github.com/OpenAdaptAI/OpenAdapt) and [OpenAdapter](https://github.com/OpenAdaptAI/OpenAdapter/). This tool integrates with deployment frameworks to ensure data protection in automation and screen parsing workflows.

## ✨ Features
- **PII/PHI Detection and Scrubbing**: Identify and remove sensitive data from screen and action inputs using state-of-the-art privacy tools.
- **Powerful Privacy Stack**: OpenScreen includes integrations with [Microsoft Presidio](https://microsoft.github.io/presidio/) for identifying and redacting PII entities, [Private AI](https://private-ai.com/) for customizable and GDPR-compliant scrubbing, and [AWS Comprehend](https://aws.amazon.com/comprehend/) for natural language processing to enhance data protection.
- **Flexible Integration**: Supports OpenAdapt and OpenAdapter for end-to-end privacy in screen-based automation.
- **Efficient Processing**: Streamlined for low latency in high-frequency applications.

## ⚙️ Setup

### Prerequisites
- **Python 3.10+**
- **Environment variables** for PII/PHI detection settings (e.g., `DETECTION_MODE`, `LOG_LEVEL`).

### Installation
1. **Clone this repository**:
   ```bash
   git clone https://github.com/OpenAdaptAI/OpenSanitize.git
   cd OpenSanitize
   ```
2. **Set up virtual environment and install dependencies**:
   ```bash
   python3 -m venv venv && source venv/bin/activate
   pip install -r requirements.txt
   ```

## 💡 Usage Example

Use OpenSanitize to scrub sensitive data from screen logs before processing:
```python
from opensanitize import ScreenScrubber

scrubber = ScreenScrubber()
cleaned_data = scrubber.scrub(screenshot_data, action_data)
```

## 🔒 Security
OpenSanitize complies with privacy standards for PII/PHI handling and is optimized for healthcare and enterprise deployments.

## 🛠️ Roadmap
- **Expanded Scrubbing Patterns**: Add support for custom scrubbing patterns.
- **Cloud Integration**: Automate PII/PHI scrubbing in cloud deployments for EC2 and containerized models.
- **Modular Expansion**: Extend compatibility with additional OpenAdapt tools.

## License
OpenSanitize is licensed under the MIT License.
