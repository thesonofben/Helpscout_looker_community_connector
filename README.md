# Integration between Google Apps Script and Help Scout

This guide will walk you through the process of creating a Google Apps Script project that integrates with Help Scout using OAuth2 authentication.

## Prerequisites

Before you start, ensure you have the following:

- A Google account.
- Access to Google Apps Script.
- A Help Scout account.

## Step 1: Creating a Google Apps Script

1. **Access Google Apps Script:** Go to [Google Apps Script](https://script.google.com/) and log in with your Google account.

2. **Create a New Project:** Click on the "+ New Project" button to create a new project. Give your project a name and click "Create."

3. **Set Up Your Script:** In the Apps Script editor, you can now write or paste your script. Be sure to include the necessary functions for authentication, data retrieval, and any other functionalities you need.

## Step 2: Creating an App in Help Scout

1. **Access Help Scout Developer Portal:** Log in to your Help Scout account and access the [Help Scout Developer Portal](https://developer.helpscout.com/).

2. **Create a New App:** Click on "My Apps" and then "Create My App."

3. **Configure Your App:**
   - **App Name:** Provide a name for your app.
   - **OAuth Redirect URL:** Set up the callback URL. This URL should point to your Google Apps Script's callback function. Typically, it will be in the format `https://script.google.com/macros/s/your_script_id/usercallback`. Replace `your_script_id` with your actual Google Apps Script project ID.

4. **Save Your App:** After configuring your app, click "Create App."

## Step 3: Setting Up the Callback URL

1. **Retrieve Your Script's Project ID:** In the Google Apps Script editor, go to `File > Project properties`. Note your script's "Script ID."

2. **Update the OAuth Redirect URL:** Go back to the Help Scout Developer Portal and edit your app. Update the "OAuth Redirect URL" to match the one you noted in the previous step, including your script's ID.

3. **Save Changes:** After updating the URL, save the changes to your app.

## Step 4: Installing OAuth2 in Google Apps Script

1. **Access OAuth2 Library:** In your Google Apps Script project, go to `Resources > Libraries`.

2. **Add the OAuth2 Library:** In the "Add a library" field, enter `MSWhizzle4in1cF_RJ18EiX1s2Yzw4ybE4j` and click "Add."

3. **Select the Latest Version:** Choose the latest version and click "Save."

4. **Set Up OAuth2:** In your script, set up OAuth2 by configuring the `getOAuthService()` function. Make sure to provide your Help Scout app's credentials (Client ID and Client Secret) and set the required scopes.

5. **Authenticate Your Script:** Run the `get3PAuthorizationUrls()` function to authorize your script to access Help Scout data. Follow the authorization process to grant access.

6. **Test Your Integration:** Test your script's functionality by running the appropriate functions to retrieve data from Help Scout.
