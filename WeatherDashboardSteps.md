![github-header-image (4)](https://github.com/user-attachments/assets/36d55115-b85e-4651-a7db-a815416d3edc)




### 1. Head to Open Weather Map website to create an account and generate your API key.
 ( https://openweathermap.org/ )

<img src="https://github.com/user-attachments/assets/094f2a88-9e7d-471d-8f4c-4a25e9f48c3d" width="75%" />




### 2. You will need to copy this generated key later

<img src="https://github.com/user-attachments/assets/848e2ad3-e31f-4b08-8914-dc5b4cc02a65" width="75%" />




### 3. Create a folder for this project in your VM and change to that directory. (you can name it whatever you want)
  
   Enter cmd:
   ```bash
WeatherDashboard
```   
<img src="https://github.com/user-attachments/assets/97dec451-68ec-48bc-bf85-fa4f48414f63" width="75%" />




### 4. In this folder create 3 directories names src, tests, and data.
  
   Enter cmd:
   ```bash
mkdir src tests data
```   
<img src="https://github.com/user-attachments/assets/9d221be3-a525-4363-8a5d-7a64b0efbfd2" width="75%" />




### 5. Create two files with python extensions in the src directory. These file are for the weather dashboard and init script.
   
   Enter cmd:
   ```bash
touch src/__init__.py src/weather_dashboard.py
```
   
<img src="https://github.com/user-attachments/assets/c7ec1cd6-1439-4714-9019-3f4cf7a8d15a" width="75%" />




### 6. Create 3 more files in your current directory. This will be a text file, a markdown file, and an environment variable file.
  
   Enter cmd:
   ```bash
touch requirements.txt, README.md, .env
```
   
<img src="https://github.com/user-attachments/assets/6c691119-ffae-4ca7-aecc-b871ddf37147" width="75%" />




### 7. Install git if you do not already have it installed.

Enter cmd:
```bash
sudo apt install git
```

   Enter "y" when prompted to continue.

<img src="https://github.com/user-attachments/assets/f00f49b7-f0be-47f8-bee5-6bb5e5e73dc1" width="75%" />




### 8. Initialize git.
  
   Enter cmd:
   ```bash
git init
```

<img src="https://github.com/user-attachments/assets/44fceb35-dae0-4a2d-9eee-4c54ac623ddf" width="75%" />




### 9. Name your git branch to "main".
   
   Enter cmd:
```bash
git branch -M main
```

<img src="https://github.com/user-attachments/assets/1f2bc842-74d4-458f-848d-8b6126296b89" width="75%" />




### 10. Ignore python cache files and any zip files from git repository.

Enter cmd:
```bash
echo "__pycache__/" >> .gitignore
echo "*.zip" >> .gitignore
```

<img src="https://github.com/user-attachments/assets/210c419f-3aee-40f8-aa06-1c500311de26" width="75%" />




### 11. Append 3 packages to the requirements text file using echo cmd. Specify the version for package. 

boto3: A library for interacting with Amazon Web Services (AWS) to manage cloud resources.
python-dotenv: A tool to load environment variables from a .env file into your Python app, for managing sensitive data like API keys.
requests: A library for making HTTP requests, such as sending and receiving data from websites or APIs.

Enter cmd:
```bash
echo "boto3==1.26.137" >> requirements.txt
echo "python-dotenv==1.0.0" >> requirements.txt
echo "requests==2.28.2" >> requirements.txt
```

<img src="https://github.com/user-attachments/assets/31e2ede0-1bcb-4736-9c5d-7b68b949676d" width="75%" />




### 12. Install python3 pip if you do not have it.

Enter cmd:
```bash
    sudo apt install python3-pip
```

Enter "y" when prompted to continue.

If the above command doesn't work, you may need to install the python3-venv package and create a Python virtual environment to install python3-pip.

Enter cmd:
```bash
    python3 -m venv venv
    sudo apt install python3.12-venv
    python3 -m venv venv
    source venv/bin/activate
```

<img src="https://github.com/user-attachments/assets/e5e4c6d4-1e1b-425c-ad3d-e971c6acb4ce" width="75%" />




### 13. Install pip dependencies to the requirements txt file.

Enter cmd:
```bash
pip install -r requirements.txt
```

<img src="https://github.com/user-attachments/assets/f431083f-347b-4c29-98df-3648fbef6126" width="75%" />




### 14. Configure AWS to enter credentials for access.

Enter cmd:
```bash
aws configure
```

<img src="https://github.com/user-attachments/assets/d551797c-8d6d-48ed-b44c-fd37db0f3a97" width="75%" />




### 15. Log into your AWS account. You will need to get your "AWS Access Key ID", "AWS Secret Access Key", "Default region name".


### 16. Click on "IAM" service. 

![image](https://github.com/user-attachments/assets/ff5a7de0-766e-4f68-8fc5-64d9e8fc4ef1)


### 17. Scroll down to Access Keys and click "Create access key".

<img src="https://github.com/user-attachments/assets/7128fcb7-9652-4523-b473-ec62724adf7" width="75%" />



   - AWS Access Key ID and Secret Access Key is located in the IAM service: click "Security credentials", then "Create access key"

<img src="https://github.com/user-attachments/assets/e2f56f25-a0ac-4644-8f49-88e98045866e" width="75%" />

   - Check the box to agree with creating a root access key (which is not a best practice). Then Click the orange create button.

<img src="https://github.com/user-attachments/assets/39b33026-5e14-47a9-9c5d-a73bd02f5071" width="75%" />

   - You will use both access keys to copy and insert AWS configuration

<img src="https://github.com/user-attachments/assets/0665ea5e-653d-4f85-8c60-e46890aad099" width="75%" />

   - Default region name is located on your top right, under "Global".
   - You will enter "us-east-1" or whatever is showing for location.
  
<img src="https://github.com/user-attachments/assets/75722d5d-7756-45db-b259-52a25d1f56d2" width="75%" />

   - Default output will be "JSON"

<img src="https://github.com/user-attachments/assets/5040b3a3-79a3-4d25-95d3-cbe43c30cbbf" width="75%" />




### 16. Create a variable for the Weather API Key and redirect to the environment variable file.
      Enter cmd:

<img src="https://github.com/user-attachments/assets/f657290c-588c-4eaf-a3ce-3080c7703186" width="75%" />




### 17. Create a variable for a randomly generated s3 bucket name that is redirected to the environment variable file.

<img src="https://github.com/user-attachments/assets/94024aa2-2043-496f-8e35-e9a2ad26582b" width="75%" />




### 18. Add Python to the weather dashboard Python file in the src directory to save data in the S3 Bucket.
    Enter cmd:

<img src="https://github.com/user-attachments/assets/784550d8-a329-454b-953a-7aad729e2659" width="75%" />

<img src="https://github.com/user-attachments/assets/4898673e-dfa6-4ebb-b509-2a0528001fe2" width="75%" />





### 19. Head to AWS S3 Bucket service and validate the weather dashboard was created. Look under "General purpose buckets"

<img src="https://github.com/user-attachments/assets/5630be47-0266-441d-9f2c-37bd95d805a9" width="75%" />




### 20. Click on your weather-dashboard, then weather-data to see all 3 objects created.

<img src="https://github.com/user-attachments/assets/2dabae56-e461-4e66-b542-13d15efb8755" width="75%" />

<img src="https://github.com/user-attachments/assets/4de5fc0b-d330-4cfb-8b91-c7950b92941e" width="75%" />

<img src="https://github.com/user-attachments/assets/a69cf383-5ddc-44a2-855b-38d16b0620c7" width="75%" />










































    

