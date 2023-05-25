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

## Important Note
Ensure that you have enabled "Less Secure Apps" access for your email account or use an app password if your email provider requires it.



## Acknowledgments
The code in this repository was inspired by the need to automate the process of sending birthday wishes to contacts. Special thanks to the original contributors and developers of the libraries used.

