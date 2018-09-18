# [AU]Market
allen.leung@'s script for the automation of labeling street addresses for the Australian market.

[IMPORTANT!]
The digits at the start of every command indicates the range of lines that the script will run on. The first number is the starting line, the second number is the ending line. A vim search and replace command :%s/foo/bar/g must be ran in order to specify a range of lines before every use!

Example:
:%s/111/500/g
:%s/222/1000/g
The first command replaces all instances of 111 to the desired start line of 500.
The second command replaces all instances of 222 to the desired end line of 1000.
The script will now only run between lines 500 to 1000. Avoid having both lines being the same, Ex: 1935,1935 because now you can't change them individually anymore and will have to redownload the default version.

!!!The purpose of this is to make it look like we're still only doing a certain amount of lines and lines per hour everyday!!!

How to do this on a mac:
1. Move the sheet that you are working on to your desktop.
2. Open up a terminal (Command space > terminal)
3. Type in this command: cd desktop
4. Then type: vim [name of your sheet] 
 - Include any extensions at the end [name of your sheet.txt]
5. Enter the commands exactly as follows:
 :%s/111/Desired start line/g
 :%s/222/Desired end line/g
6. After running both of those commands, type
:wq [This will save the edits made to the sheet and close the vim text editor]

South/Western Australia is currently labeled as South/Western[State] Australia[Country]. You must re-lable Australia to [State].
This is because another line in the script labels any instance of Australia as [Country]. I've not been able to resolve this yet.

The script currently doesn't label road, avenue, way, street. You must label these yourself. I'm working on it.

If you don't need to edit the query at all, the labels will stay gray and not actually edit the text file (green labels). All you have to do is uncheck the "Skipped" box in the tool and go to the next query. 

Only 1 word in the query must be labeled through the tool and the script can do the rest. You can test this out by going to the next query without labeling anything, and go back. Then label one thing, anything, in the query and go next then come back. Everything that the script labeled should be green now.

List of everything this script labels: https://docs.google.com/spreadsheets/d/13Lk_XoEZ7AsVLwG_JIXmGpiZ1_JtILwdRADwfVEL-nc/edit?usp=sharing

You all have editing rights to this document, feel free to add anything not on there, but let me know if you do so.
