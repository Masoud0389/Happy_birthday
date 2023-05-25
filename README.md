# Automatic Happy Birthday Email Sender

This Python script automates the process of sending happy birthday emails to contacts based on their birthdays stored in a CSV file. The script uses the smtplib library to connect to your email server and sends personalized birthday emails using templates.

## Requirements
- pandas
- smtplib

## Setup
1. Update the `MY_EMAIL` variable with your email address.
2. Update the `MY_PASSWORD` variable with your email account password.
3. Prepare a CSV file named "birthdays.csv" with the following columns:
   - `name`: Name of the person
   - `month`: Birth month (numeric)
   - `day`: Birth day (numeric)
4. Create letter templates in the "letter_templates" directory. Each template should be a text file containing the email content with the placeholder [NAME] for the recipient's name.
5. Modify the code to specify the file path of the letter templates (e.g., `file_path = "letter_templates/letter_template.txt"`).

## Usage
1. Run the script to check if any birthdays match the current date.
2. If there is a match, the script selects a random letter template, replaces the [NAME] placeholder with the recipient's name, and sends the email.
3. The script uses the Gmail SMTP server by default. If you use a different email provider, modify the SMTP server details accordingly.
4. The script sends the email from your email address to the recipient's email address using SMTP authentication.

## Deployment on the Cloud

To make the happy birthday email sender code run automatically every day, you can deploy it on a cloud platform of your choice. Here's a general outline of the steps involved:

1. Choose a cloud platform:
   - [Amazon Web Services (AWS)](https://aws.amazon.com/)
   - [Google Cloud Platform (GCP)](https://cloud.google.com/)
   - [Microsoft Azure](https://azure.microsoft.com/), etc.

2. Create an account on the chosen cloud platform if you don't have one already.

3. Set up the necessary services:
   - Create a virtual machine (VM) or an instance on the cloud platform.
   - Configure the VM with the required specifications (e.g., operating system, storage, memory, etc.).

4. Connect to the VM:
   - Use SSH or the provided cloud platform interface to connect to the VM.

5. Upload the code:
   - Transfer the Python script and the "birthdays.csv" file to the VM. You can use secure copy (SCP) or any other file transfer method provided by the cloud platform.

6. Install dependencies:
   - Ensure that Python, pandas, and smtplib are installed on the VM. You can use pip to install any missing packages.

7. Schedule the script:
   - Use the built-in scheduling mechanism of the cloud platform to run the script automatically every day. For example:
     - On AWS, you can use [Amazon CloudWatch Events](https://aws.amazon.com/cloudwatch/).
     - On GCP, you can use [Cloud Scheduler](https://cloud.google.com/scheduler).
     - On Azure, you can use [Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/).

8. Configure email server credentials:
   - Update the `MY_EMAIL` and `MY_PASSWORD` variables with your email address and password directly in the code running on the cloud VM.

9. Monitor and troubleshoot:
   - Monitor the execution logs and any email delivery failures to ensure the script is running successfully. Make any necessary adjustments to the code or environment if issues arise.

10. Celebrate the automated birthday wishes! 🎉

If you're looking for a free cloud platform to deploy your code, you can consider [Heroku](https://www.heroku.com/). Heroku offers a free tier that allows you to run applications with certain limitations. You can follow their documentation to set up a Python environment and deploy your code.

Note: The above steps provide a general guideline, and the specific instructions may vary depending on the cloud platform you choose. Please refer to the cloud platform's documentation for detailed instructions on VM setup, code deployment, and scheduling tasks.

## Contributing
Contributions are welcome! If you find any issues or have suggestions for improvement, please open an issue or submit a pull request.

## Important Note
Ensure that you have enabled "Less Secure Apps" access for your email account or use an app password if your email provider requires it.



## Acknowledgments
The code in this repository was inspired by the need to automate the process of sending birthday wishes to contacts. Special thanks to the original contributors and developers of the libraries used.
