Setup: For the set up I had to first install python3 on both of my local and aws systems! I also had to download pip to both systems, then used pip to install Discord.py
and python-dontev. Once I had all the software/depedencies downloaded, had to create a discord bot! This process fascinated me, anyway I had to create a new bot in discords
developer portal. This made made choose the bots name, then to create a new server for the bot! I had to authenticate the bot to the guild using the generated url in which
puts the bot in your server. After the bot was populated into the guild I had to create two files one was bot.py and a .env! The bot.py is where the code runs the commands and
what to prompt for your server's messages! The .env is where your bots API key is stored and will be able to be connected, which was copied from the developer portal! 

Usage: Had to add the bots token inside of .env, then inside of bot.py I added to the message content if you say "Hello!" then it will print out 
        'Hi! Welcome to Project1!',
        'Great to see you! Welcome to our server!',
        'Hello Friend! Welcome to the server Project1!',
        'Welcome! Thanks for joining our server Project1!'
        However, you have to make sure you are running bot.py for your discords bot to react to any message! 
        
Research: I can make the program stop automatticaly by creating another file and adding a command that can exit the application or make it sleep for example time.sleep(20)
os.system(bots file) and could make it restart with a similar file! I believe these would work if you could add in your token and the program would realize that the bot
has been inactive and when to restart!
