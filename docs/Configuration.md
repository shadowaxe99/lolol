```python
# docs/Configuration.md

# Configuration

## API Keys

To use Sara's functionality, you will need to generate and set up API keys for the following services:

1. Google API: To access Gmail, Google Calendar, and Google Tasks APIs.
2. Microsoft API: To access Microsoft Graph API and Microsoft Outlook Calendar API.
3. Zoom API: To manage Zoom meetings.

Follow the instructions below to generate and set up the API keys for each service.

### Google API

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project or select an existing project.
3. Enable the necessary APIs: Gmail API, Google Calendar API, and Google Tasks API.
4. Go to the "Credentials" section.
5. Click on "Create Credentials" and select "API key".
6. Copy the generated API key.

### Microsoft API

1. Go to the [Microsoft Azure Portal](https://portal.azure.com/).
2. Create a new Azure AD application or select an existing one.
3. Go to the "Certificates & secrets" section.
4. Click on "New client secret" and generate a new secret.
5. Copy the generated client secret.

### Zoom API

1. Go to the [Zoom App Marketplace](https://marketplace.zoom.us/).
2. Sign in with your Zoom account or create a new account.
3. Go to the "Develop" section and click on "Build App".
4. Select the "JWT" app type.
5. Fill in the required information and click on "Create".
6. Copy the generated API key and API secret.

## Environment Variables

To securely store the API keys, you can set them as environment variables in your local development environment or in your deployment environment. Follow the instructions below to set up the environment variables.

### Linux/MacOS

1. Open a terminal.
2. Run the following commands, replacing the placeholders with your API keys:

```bash
export GOOGLE_API_KEY="<your_google_api_key>"
export MICROSOFT_CLIENT_SECRET="<your_microsoft_client_secret>"
export ZOOM_API_KEY="<your_zoom_api_key>"
export ZOOM_API_SECRET="<your_zoom_api_secret>"
```

### Windows

1. Open a command prompt.
2. Run the following commands, replacing the placeholders with your API keys:

```bash
set GOOGLE_API_KEY="<your_google_api_key>"
set MICROSOFT_CLIENT_SECRET="<your_microsoft_client_secret>"
set ZOOM_API_KEY="<your_zoom_api_key>"
set ZOOM_API_SECRET="<your_zoom_api_secret>"
```

Make sure to replace `<your_google_api_key>`, `<your_microsoft_client_secret>`, `<your_zoom_api_key>`, and `<your_zoom_api_secret>` with the actual API keys you generated.

## Conclusion

By following the instructions above, you have successfully generated and set up the necessary API keys for Sara's functionality. These API keys will allow Sara to interact with the Google, Microsoft, and Zoom APIs, enabling seamless integration with commonly used productivity tools.
```
