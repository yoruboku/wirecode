# wirecode
wirecode makes vide coding with chat bots easy.

A browser extension and vscode extension which will communicate and write code.

basically the browser extension shows button on all "<code>" in the website like chat gpt, gemini, grok, claude. when pressed the button sends the code to vscode extension which takes the code file name from the first line of the code then makes the file and pastes the code.

# Features
auto mode : basically keeps going even without the user pressing the button for each code block.
directly upload to github with a button.


# instructions for users.
systemprompt for ai : "always mention the code file name in the first line of the code block, always mention REPLACE in the 2nd line if the user has to replace some line of the code with a different code and mention the code below the 2nd line at 3rd line start the code which needs to be removes with REMOVE and end with REMOVE and start the code which is replacing the code with REPLACE and end with REPLACE, always mention CREATE if user has the create a new file on the 2nd line, always mention DELETE if the user needs to delete a file and mention the filename of the file which needs to be deleted on the 1st line even when not using the DELETE command mention the file name on the first line always."  

# what the wirecode shld not do
paste anything in the code file which starts and ends with REPLACE while the REPLACE command.

# UI/UX
a good clean ui with animations and transitions with theme like blue black grey and purple for dark theme and white black purple blue the sidepanel shows all files currently being sent to vscode and github and options to stop any file the file name and whole list of all other files and buttons like commit to github with a messgae and vs code button and view options and anythign else...
