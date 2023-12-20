# AutoReply

This Node.js application enables you to automatically monitor and reply to unread emails in your Gmail every 2 minutes.
(For testing,we are checking every 1 minute)

# Libraries and Technologies used:
  Node.js,
  node-cron,
  googleapis,
  fs,
  readline,
  OAuth 2.0,
  JSON

## Steps to be followed:

1. **Clone the repository**

   ```bash
   git clone https://github.com/AditiRout/AutoReply.git
   ```

2. **Install dependencies**

   Navigate to the cloned repository directory:

   ```bash
   cd AutoReply
   ```

   Install the required dependencies:

   ```bash
   npm install
   ```

3. **Obtain credentials.json**

   - Go to the Google Cloud Console.
   - Create a new project or select an existing project.
   - Enable the Gmail API for your project.
   - Create credentials (OAuth client ID) for a Web/Desktop application by setting up the Oauth Consent Screen.
   - Download the credentials JSON file and save it as `credentials.json` in the project directory.

4. **Run the application**

   Run the following command:

   ```bash
   node app.js
   ```

   The application will prompt you to authorize it by clicking on a URL. Follow the authorization flow and enter the generated authorization code in the terminal from browser url bar.
   Below is sample URL, where YOUR_CODE is the token you need to put in the terminal.
   
   http://localhost:3000/oauth2callback?code={YOUR_CODE}&scope=https://www.googleapis.com/auth/gmail.modify

5. **Application Improvement Ideas**

   Allow users to configure settings like reply messages, label names, and cron job intervals through a user interface 
   Extend the application to handle multiple Gmail accounts and manage labels independently for each account.
   Ensure sensitive data, such as API keys or credentials, is properly secured and not exposed in the codebase or logs.(Hashing)
   Minimize unnecessary API calls by caching or storing retrieved data locally and avoiding redundant operations.
