# Automatic-Email-sender-Handles-Ice-cream-
Email sender

Usage

The first thing you need to do is to configure the data/login.secret file. This files contains the authentication credentials to connect to your email provider. The file must contain two lines only, the first line is the username, and the second line is the password! Most services (Google included) require you first create an "App password", a special token that will act as your password. This can be easily created from your account web page (for Google, visit here for more info). Therefore, in the login.secret file you will need to put your username and then the app password.

Next, you need to setup your contacts in the data/contacts.csv file. Finally, you need to write the template body of your email in the data/email-template.txt file. The current template contains the email I used for my paper as an example. If you want to change the variables injected in the template, you need to change the create_emails() method in the mail.py file.

# Provides CLI support to execute the script
pip install fire

# Show help
python main.py send_emails

# Executes the script
python main.py send_emails data/contacts.csv data/email-template.txt data/login.secret "Your Name" "The Subject" --dry-run
Remove --dry-run when you are ready to send the emails for real.

Note that, by default, this script is configured to work with Google emails. You can easily change that by changing the SMTP server through the --email_server_smtp_address and --email_server_smtp_port parameters.
