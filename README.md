# Google Tasks Home Assistant add-on

Home assistant custom add-on to add functionalities for Google Tasks.

## Development

1. Install [Google Tasks integration](https://www.home-assistant.io/integrations/google_tasks/) for Home Assistant.
2. Create new credentials in [Google Developers Console](https://console.cloud.google.com/):
   1. Navigate to APIs & Services (left sidebar) > [Credentials](https://console.cloud.google.com/apis/credentials).
   2. In the left sidebar, select Credentials, then select Create credentials (at the top of the screen), then select OAuth client ID.
   3. Set the **Application type** to **Desktop app** and give this credential a name (like "Home Assistant Credentials").
   4. Save credentials as `credentials.json` into the root folder of this project.
3. Run the application:

    ```bash
    yarn dev
    ```

The reason to install the Google Tasks integration is to set up the **OAuth consent screen** and other configurations described in [Scenario 2: You do not have credentials set up yet](https://www.home-assistant.io/integrations/google_tasks/#scenario-2-you-do-not-have-credentials-set-up-yet) that are also needed for the Google Tasks Home Assistant add-on. In the end, you will have one Google project with two different credentials: one for the Google Tasks integration and the other for the Google Tasks Home Assistant add-on.

> **Do not commit `credentials.json` nor `token.json` (generated automatically after running application).**

## Links

- [Google Tasks integration for Home Assistant](https://www.home-assistant.io/integrations/google_tasks/)
- [Google Tasks Node.js quickstart](https://developers.google.com/workspace/tasks/quickstart/nodejs)
