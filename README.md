# Weather Dashboard

![image](https://github.com/user-attachments/assets/9af14640-b6e9-4270-ad3c-b7c2fd356da1)


## **Project Highlights**

🌦️ This project shows the current weather to users based on where they are.

⛅ It uses OpenWeather API to get the weather data and AWS S3 to store the data in the cloud.

🌈 The project shows how to work with APIs, store data online, and set up your project using Python.

🌪️ It also demonstrates how to manage your environment and make sure all the tools your project needs are installed and set up correctly.


## **Capabilities**
🔧 Fetches real-time weather data for multiple cities

🔧 Displays temperature (°F), humidity, and weather conditions

🔧 Automatically stores weather data in AWS S3

🔧 Supports multiple cities tracking

🔧 Timestamps all data for historical tracking


## **⚙️Technologies⚙️**
- **Cloud Provider**: AWS
- **Core Services**: S3
- **External API**: OpenWeather API
- **Programming Language**: Python 3.x
- **Version Control**: Git
- **Environment Management**: Environment Variables
- **Error Handling**: Custom error handling in Python
- **IAM Security**: Secure management of API keys and AWS credentials
- **Infrastructure as Code**: AWS resource management through scripts

---

## **Technical Architecture**



---

## **Prerequisites**
Free account subscription and an OpenWeather API Key at [OpenWeather API](https://openweathermap.org/api)


## **Setup Instructions**

1. Clone the repository 
```bash
git clone https://github.com/MJaloui/weather---dashboard
```

2. Install dependencies:
bashCopypip install -r requirements.txt

3. Configure environment variables (.env):
CopyOPENWEATHER_API_KEY=your_api_key
AWS_BUCKET_NAME=your_bucket_name

4. Configure AWS credentials:
bashCopyaws configure

5. Run the application:
   python src/weather_dashboard.py

---

## **Key Takeaways**

✔️ AWS S3 bucket creation and management

✔️ Environment variable management for secure API keys

✔️ Python best practices for API integration

✔️ Git workflow for project development

✔️ Error handling in distributed systems

✔️ Cloud resource management

## **Opportunitues for Growth**

🌱 Add weather forecasting.

🌱 Implement data visualization

🌱 Add more cities

🌱 Create automated testing

🌱 Set up CI/CD pipeline


