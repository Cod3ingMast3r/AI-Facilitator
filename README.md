# Project Title

A brief description of your project.

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

### OPENAI Related Instructions
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

