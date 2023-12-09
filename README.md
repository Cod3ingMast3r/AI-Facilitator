# AI-Facilitator

The aim of this Project is to prove the Feesability of an AI Class facilitator which would ultimatley allow for more asynchronous course instructions

## Setting Up the Project

To set up the project, follow these steps:

### 1. Clone the Repository
First, clone the repository to your local machine:
```bash
git clone [Your Repository URL]
cd [Your Repository Name]
```

### 2. Create a Virtual Environment (Optional but Recommended)
Creating a virtual environment for your project keeps your project's dependencies separate from your system's Python packages.

On Windows:
```bash
python -m venv venv
.\venv\Scripts\activate
```
On macOS and Linux:
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies
Install the project dependencies using the `requirements.txt` file:
```bash
pip install -r requirements.txt
```

### 4. Environment Variables Setup
Create a `.env` file in the current working directory with the following:
```plaintext
OPENAI_API_KEY=
OPENAI_ASSISTANT_ID=
DISCORD_TOKEN=
DISCORD_CHANNEL_ID=
```

### OPENAI Related Instructions:
1. Go to Openai.com
2. In the Top Right click Menu 
3. Click Log In
4. Click API
   #### Create and Get Open AI Key:
     5. On the left Panel Click the lock icon labeled API keys
     6. Click + Create new secret key
     7. Name the key something like AI Facilitator
     8. Copy the secret key
     9. Set the OPENAI_API_KEY in the .env file to the secret key
   #### Create and Get Open AI Assistant ID:
     5. On the left Panel Click the robot icon labeled Assistants
     6. In the Top Right Click + Create
     7. For the Model Select gpt-4-1106-preview (Don't worry about name or instructions)
     8. Turn On Retrieval
     9. Click Add next to files
       - Attach the lecture.txt file in this folder
     10. Click Save
     11. Copy the Assistant ID and in the .env file set OPENAI_ASSISTANT_ID to the Assistant ID

### DISCORD Related Instructions
  #### Enable Discord Developer Mode
    1. Open Discord
    2. Go to user Settings
    3. Under App Settings click advanced and enable developer mode

  #### Discord Bot Setup
    1. Create a Discord server where the bot will operate.
    2. Visit the [Discord Developer Portal](https://discord.com/developers/applications).
    3. Create a new application and add a bot to it.
      - Ensure Bot has all Privileged Gateway Intents
      - Ensure the Bot has Admin Access

    4. Reset Bot Token and copy the bot token and set `DISCORD_TOKEN` in the `.env` file.
    5. Generate and use an OAuth2 URL to add the bot to your server.
      1. On the left Pane in Discord Developer Portal Select OAuth2
      2. Under this select URL Generator
      3. For scopes Select Bot and then for bot permissions select Administrator
      4. Copy and enter the URL
      5. Select the server you created above
      6. On the server right click the channel you want the bot to interact with
      7. At the bottom of the list that pops up, click Copy Channel ID
      8. Psste the Channel ID in the .env folder for DISCORD_CHANNEL_ID

### Run The Program and chat with Professor:
  On Windows:
  ```bash
  .\venv\Scripts\activate
  python connect.py
  ```
  On macOS and Linux:
  ```bash
  source venv/bin/activate
  python connect.py
  ```