# Weather OpenAPI Store in S3 Bucket

This project demonstrates how to build a weather OpenAPI store using AWS S3 and Python. The application fetches weather data using the OpenWeather API and uploads it to an S3 bucket. Below are the steps, challenges, and lessons learned during the development process.

---

## Project Structure

- **src**: Contains the source code.
- **tests**: Holds unit tests.
- **data**: Stores data files.

### Key Files

- `src/weather_dashboard.py`: The main application logic.
- `.env`: Contains sensitive configurations like API keys and bucket names.
- `requirements.txt`: Lists project dependencies.

---

## Setup Instructions

### Prerequisites

1. **Install Python** and add it to your system's PATH. Verify installation:
   ```bash
   python --version
   ```

2. **Install pip** and verify:
   ```bash
   python -m pip --version
   ```

### Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/amnipriyasowrirajan/DevopsAllStarsChallenge2025.git
   cd DevopsAllStarsChallenge2025
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

   **Dependencies include**:
   - `boto3==1.26.137`
   - `python-dotenv==1.0.0`
   - `requests==2.28.2`

3. **Configure AWS CLI**:
   Run the following command and provide the required details:
   ```bash
   aws configure
   ```
   - Access Key ID
   - Secret Access Key
   - Default Region (e.g., `us-east-1`)

4. **Set Up OpenWeather API**:
   - Sign up on OpenWeather and retrieve your API key.
   - Add the API key and bucket name to the `.env` file:
     ```env
     OPENWEATHER_API_KEY=your_api_key
     AWS_BUCKET_NAME=your_bucket_name
     ```

5. **Run the Application**:
   ```bash
   python src/weather_dashboard.py
   ```

---

## Challenges & Solutions

1. **API Key Issue**:
   - **Problem**: The application initially failed to read the API key from the `.env` file.
   - **Solution**: Adding a newline at the end of the `.env` file resolved the issue.

2. **Environment Differences**:
   - **Problem**: Adapting to PowerShell commands like `New-Item` instead of `touch`.
   - **Solution**: Leveraged platform-specific commands where necessary.

3. **Security Best Practices**:
   - **Solution**: Sensitive information like API keys was excluded from GitHub using `.gitignore`.

---

## Lessons Learned

1. **Attention to Detail**:
   - Small formatting issues (e.g., missing newline) can lead to significant problems.

2. **Tool Adaptability**:
   - Switching between environments and understanding the nuances of each tool is critical.

3. **Documentation**:
   - Tracking errors and solutions helps improve workflows.

4. **Security Awareness**:
   - Always protect sensitive information.

---

## Resources

- **OpenWeather API**: [https://openweathermap.org/api](https://openweathermap.org/api)
- **GitHub Repository**: [DevopsAllStarsChallenge2025](https://github.com/amnipriyasowrirajan/DevopsAllStarsChallenge2025)
