# BiplovNotepad-python
As you must be already aware, Notepad is a simple text editor for Microsoft Windows that allows users to create text documents, save them as plain text, and edit plaintext files. It is extremely useful for viewing or writing relatively short text documents saved as plain text.

The File menu has options like New, Open, Save, Save As, and Exit.
The Edit menu has options like Cut, Copy, Paste, Delete, Find, Select All, and Time/Date.
The Help menu has options like About Notepad.
**********************************************************************************************************************************************************************
After importing all the libraries and packages, we initialize the GUI window with the title Python Notepad. I have made the window size fixed by passing values (0,0) to the resizable function. We use the ScrolledText function to make our notepad window scrollable as more text gets added.

The File menu has options like New, Open, Save, Save As, and Exit.
The Edit menu will have the options Cut, Copy, Paste, Delete, Find, Select All and Time/Date.
The Help menu item will have the option About Notepad that just displays some basic text and information.
Python Tkinter provides a set of functions that we can use while working with files. By using these, we do not have to design standard dialogues by ourselves. I have opened a file and saved the file using the filedialog library.

The messagebox widget in Tkinter is used to display the message boxes in the python applications. It has several functions that we can use to display appropriate messages. I have used the askyesno and showerror functions.

Add Commands
#notepad menu items
notepadMenu = Menu(root)
root.configure(menu=notepadMenu)
#file menu
fileMenu = Menu(notepadMenu, tearoff = False)
notepadMenu.add_cascade(label='File', menu = fileMenu)
#adding options in file menu
fileMenu.add_command(label='New', command = cmdNew)
fileMenu.add_command(label='Open...', command = cmdOpen)
fileMenu.add_command(label='Save', command = cmdSave)
fileMenu.add_command(label='Save As...', command = cmdSaveAs)
fileMenu.add_separator()
fileMenu.add_command(label='Exit', command = cmdExit)
#edit menu
editMenu = Menu(notepadMenu, tearoff = False)
notepadMenu.add_cascade(label='Edit', menu = editMenu)
#adding options in edit menu
editMenu.add_command(label='Cut', command = cmdCut)
editMenu.add_command(label='Copy', command = cmdCopy)
editMenu.add_command(label='Paste', command = cmdPaste)
editMenu.add_command(label='Delete', command = cmdClear)
editMenu.add_separator()
editMenu.add_command(label='Find...', command = cmdFind)
editMenu.add_separator()
editMenu.add_command(label='Select All', command = cmdSelectAll)
editMenu.add_command(label='Time/Date', command = cmdTimeDate)
#help menu
helpMenu = Menu(notepadMenu, tearoff = False)
notepadMenu.add_cascade(label='Help', menu = helpMenu)
#adding options in help menu
helpMenu.add_command(label='About Notepad', command = cmdAbout)
Tkinter has predefined virtual events which can be used using the event_generate function. I have used the events <<Cut>>, <<Copy>>, <<Paste>>, <<Clear>>, and <<SelectAll>> to implement the options available in the edit menu of python notepad.
The find function is to find a given string or substring from the text in the notepad. The TimeDate function is to display the current time and date to the user.

We will be using all these functions when we add commands to our menu options for File, Edit, and Help. This is why we have named the functions as cmdNew, cmdSave, cmdOpen, etc. where cmd is an abbreviation for command. This makes the code more understandable and readable.

notepad.pack()
root.mainloop()
The last thing we need to do is to add the menu options in notepad for File, Edit, and Help, and then add specific commands to these menus. While creating the menus using the Menu function, the parameter ‘tearoff = False’ is to prevent Tkinter from adding a dotted line in the menu which is added by default.

We label the commands using the ‘label’ parameter. This is how the menu option will appear to the user. The ‘command’ parameter is used to assign the functions that we created earlier, that will define how the command will behave.

Finally ‘root.mainloop()’ is a method on the main window that runs our application. This method will continuously loop, it will wait for events from the user till the user exits the program.

When we close the window that we have created, we will see a new prompt is displayed in the python shell.

Python Notepad Output Screenshots
python notepad screenshot

python notepad text-editor screenshot


Conclusion
We have successfully developed a text editor / notepad using python. Along with a simple notepad we have developed file, edit, and help menu. In this python project, we have used tkinter and basic python concepts.
