# wirecode
wirecode makes vide coding with chat bots easy.

A browser extension which detects all code blocks in all websites and show a button on all code block \<code\> like github, ai websites like chat gpt and gemini more... and when the button is pressed it adds all of the codes in the browser extension with options to preview code, rename code, remove code, multiselect, view options, download option, commit to github repo option, auto mode which keeps adding all \<code\> blocks and btw this browser extension will also auto name the codes it wll get the names from the 1st line of all codes because of the system prompt but this will only work with ai so for other times like github it will just the file name already and for other times it will just put a default code based name on the file like if its a python code it will name it 1.py if no other choice, a selecting tool which basically lets me normaly select all code/text then right click and add to list. it also has a option to go back and see where the code was taken from like if i took a code from chat gpt it will redirect me to the link and the exact place the code is on. and history where i can see the full history of all the code ive ever taken with dates and stuff tho not full codes just the links and position and name of that code i can press on that code and it will redirect me to its exact link and position in the page. sorting saves all projects in a folder in the sidepanel like if i got code from chat gpt with auto mode like all code form same link it will automaticlaly be saved in a folder even if not using auto mode, user can create folder inside folders and sort everythiing with multiselect and darg and drop users can even drag and drop whole folders from the browsers to a local folder in the pc, and btw if the extension doesnt see any name in the 1st line of the code it looks around that code like when chat gpt says save this as main.py it will use that as name and if theres not even that it will use the default names.


# Features
auto mode : basically keeps going even without the user pressing the button for each code block.
directly upload to github with a button.


# instructions for users.
systemprompt for ai : "always mention the code file name in the first line of the code block, always mention REPLACE in the 2nd line if the user has to replace some line of the code with a different code and mention the code below the 2nd line at 3rd line start the code which needs to be removes with REMOVE and end with REMOVE and start the code which is replacing the code with REPLACE and end with REPLACE, always mention CREATE if user has the create a new file on the 2nd line, always mention DELETE if the user needs to delete a file and mention the filename of the file which needs to be deleted on the 1st line even when not using the DELETE command mention the file name on the first line always."  

# what the wirecode shld not do
paste anything in the code file which starts and ends with REPLACE while the REPLACE command.

# UI/UX
a good clean ui with animations and transitions with theme like blue black grey and purple for dark theme and white black purple blue the sidepanel shows all files currently being sent to vscode and github and options to stop any file the file name and whole list of all other files and buttons like commit to github with a messgae and vs code button and view options and anythign else...
