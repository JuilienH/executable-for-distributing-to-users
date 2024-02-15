# executable-for-distributing-to-users

### When you work on a team where other analysts are not programmers, you may want to have them run your python scripts with confidence once one development is done. It is common to make an executable for the distribution purpose.
### Tools I use for this development:
1. Code editor: Microsoft Visual Studio
2. Scripting language: Python
3. The main python library for creating the executable application: Pyinstaller

#### In my favorite code editor (you definitely choose any you feel comfortable with!), I always start with local development, which means the input, the output and the script are all saved in my local folder. By doing so, I can make sure there are no any connections or access issues during my python development. Once the script is complete and ready for use, I then start to change the paths to which I download or upload data files. The most easier way is to locate a shared folder that you, as well as your users, have already had access to. The shared folder location must include the forward slash in the directory. (It is tricky as when you copy it, it is by default backward slash. 
Readable directory in the python script: Z:/main_folder/folder1/main.py
#### As python is easy to learn, but it is not easy for anybody to run it. The goal here is help your users run your script without learning from scracth. So there are many python libraries you can leverage to create an executable, which is designed to be run on other people's machines without haveing them install all the required python libraries and devepdencies. How great this sounds! 
1. In Mirocrsoft Visual Studio, install the python library, pyinstaller "in the python project" that you want the users to run. You can search many ways how to install it in cmd window, but I prefer in installlation in the same virtual environment where I build the python script to be shared. For keeping each development project clean while I usually have multiple lines of development going on, this is the best practice I always stick to.
2. Once pyinstaller is installed successfully, click the highlighted link to open PowerShell, located at the bottom right panel in Microsoft Visual Studio.
   
![PowerSHell](https://github.com/JuilienH/executable-for-distributing-to-users/assets/22305109/da539f9f-dc60-4662-bf4b-0e8ccfce45f2)


3. Now we can see the directory in PowerShell has been pointing the virtual environment where I want to package my specifit python script. Then it is way clear where you are working on packing the script. Then simply type in ```pyinstaller --onefile your_script_name.py``` And wait for few minutes until you see the comments in PowerShell indicate the EXE is successfully created!
4. You should easily find the folder "dist" under this specific virtual environment folder. You should see the executable is included inside. Now it is time to send out the executable for users!
5. All the users have to do is "Double click" the executable and a prompt will be open. When the executable is completely run, the prompt will disappear. 
