# automated_study
Creates a shortcut for Python/DevOps leanring environment. Calls up website of your choice, a blank notepad, git, and OracleVM
Run using cmd for Windows. Save the file to default directory location. When cmd is called, type python study.py and the file will execute the script.


import webbrowser # for URL
import os
from pathlib import Path 
import time # delay makes sure all programs work before self-exiting.

learning_website = "https://learning.google/" # swap this url with one of your choosing.
notes = Path(r'C:\Users\Guest\VirtualBox VMs\Notes for VM.txt') # follow whatever .exe path you need and cut/paste here
gitbash = Path(r'C:\Program Files\Git\git-bash.exe') # ibid
# oracle = Path(r'"C:\Program Files\Oracle\VirtualBox\VirtualBox.exe"') 3 ibid

webbrowser.open(learning_website)
os.startfile(notes)
os.startfile(gitbash)
# os.startfile(oracle)

# function to close cmd prompt on it's own
def closeFile():
    command = os.system('TASKKILL /F /IM cmd.exe')


print('-----------------------------------------------')
print('All programs up and running. Happy studying!')
print('-----------------------------------------------')

time.sleep(7)

closeFile()
