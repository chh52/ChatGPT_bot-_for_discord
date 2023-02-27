# ChatGPT_bot-_for_discord
a bot for use in discord that responds to prompts using ChatGPT's Davinci model 

---

## Technologies

Python 3.9 was used to code this app.  
Libraries used are:
- discord.py 2.1.0
- openai 0.26.0
- python-dotenv 0.21.0
- requests 2.25.1
- os
    
---

## Installation Guide

in the chatgpt_ai folder:
If you run the command "pip install -r requirements.txt" it will auto install the necessary libraries, or you can go into requirements.txt and manually install.

I also needed to install SSL since it was giving me an "SSL is not supported" error when I was trying to connect to my server.  
you can do that by using the following command in terminal/gitbash:  
"conda install -c anaconda openssl"

**OPENAI:**

You will need an OpenAI account [here](https://openai.com/api/)

go to [https://platform.openai.com/account/api-keys](https://platform.openai.com/account/api-keys)
  - 'Create new secret key' and copy that down as this will be your one chance you can copy it.  **(needed for .env file)**


**DISCORD:**

You'll need to create a bot in discord via the [discord developer portal](https://discord.com/developers/applications)
  - New application
  - name it whatever you want
  - create

1. Click on "Bot" on the left sidebar
2. Make sure "Message Content Intent" is turned on
3. Add Bot
4. Click on "OAuth2" on the left sidebar
5. Click on "URL Generator"
6. click on the 'bot' box under SCOPES
7. give the bot admin permissions, or just click the relevant text permissions
8. The generated URL at the bottom will be the link you need to use to add the bot to a new or existing server
9. Click on "General" on the left sidebar
10. Default Authorization Link should be set to Custom URL where you'll paste the URL from URL Generator.
11. Click on "Bot" on the left sidebar
12. click on "Reset Token" which will give you your DISCORD_TOKEN **(needed for .env file)**
13. go to the URL Generator link in a web browser to add the bot to servers you have access to.


**.ENV:**

You will need to create a .env file in the chatgpt_ai folder with the following variables:
DISCORD_TOKEN and CHATGPT_API_KEY

---

## Usage

In terminal, go to the \chatgpt_ai folder and run the run.py file -> `python run.py`
Go to discord where you have it linked and ask it questions using the /ai, /bot, or /chatgpt prefixes.
  Example:  `/ai what is 2 plus 2?`

Note: by default, this will limit the responses to 200 tokens, which is about 150 words.  You can adjust the max_tokens variable in chatgpt_ai\openai.py

> for context, 1000 tokens cost $.02.  I think OpenAI gives you $18 dollars worth of tokens to start for testing purposes.
---

## Contributors

This was created by Cuong Ha

---

## License

public






