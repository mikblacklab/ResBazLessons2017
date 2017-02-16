## ResBaz mini-session Introduction to Command-line tools (Day2)

   A lesson on how to set-up your computer so you can use command-line tools from anywhere, and you don't lose them buried in your direcotries.
   
   Example tool used:
https://www.cog-genomics.org/plink2

   - Make yourself a safe place to keep everything
   
   ```
         mkdir ~/MyTools
         mkdir ~/MyTools/bin
   ```
   
   - From now on when you download a command-line tool save it in the MyTools directoy - that way you won't lose it or delete it
   
   - To run that program from anywhere we need to follow two/three quick set-up steps
      - make a symbolic link to your new tool - this link should live in the ~/MyTools/bin folder you just made
      - symbolic links need full file paths (not relational file paths - as in full/path/to/this/file vs ../this/file - ~ counts as a full path)

   - set-up your bash environment to always search for tools in your ~/MyTools/bin folder (as well as the places it normally searches)
      - To do this make a .bashrc file - a .bashrc file is a file that runs (automatically) every time you open a new terminal window. It's purpose is to provide a place where you can set up variables, functions and aliases, define your prompt/other settings.
      
   ```
   nano ~/.bashrc
      PATH=${PATH}:/Users/myusername/MyTools/bin
   # save and exit nano
   ```
   
   - refresh your bash environment to read from that file
   
   ```
   source ~/.bashrc
   ```
   
   - on a mac you need to complete one final step, linking your .bashrc file to your .bash_profile file - if you do not do this you will need to run source ~/.bashrc everytime you open a new Terminal session
      - here are two possible ways to do this
   
   ```
   ln -s ~/.bashrc ~/.bash_profile
   
   OR [this is useful if your .bash_profile file already has something in it]
   
   nano ~/.bash_profile
      source ~/.bashrc
   # save and exit nano
   
   ```

  - now try it! go to any directory, type in the name of the tool you just installed (eg. plink). Does it run or 

#### NEXT TIME YOU DOWNLOAD A NEW TOOL TO USE YOU ONLY NEED TO DO THE SYMBOLIC LINK STEP TO MAKE IT AVAILABLE FROM ANYWHERE

   - if you have multiple tools in the same folder that you want to set up symbolic links to, use a for loop
   
   ```
   cd ~/MyTools/folder/with/lots/of/tools
   for tool in $(ls *); do ln -s ~/MyTools/folder/with/lots/of/tools/$tool ~/MyTools/bin/${tool}; done
   ```

#### why is any of this important/useful?
   - if you need to access tools via other scripts it is much easier and tidier to only use the tool_name than the full file path
      - eg. this Python script (https://github.com/MerrimanLab/snp_design) requires two command line tools to run, anyone can install & run it without having to edit the script to have their computers exact file path for these tools
   - you can also make a group tools folder so everyone in your group uses the same tools/versions - all have .bashrc pointing to the same place; this is relevant to working on servers that everyone can access - not so much working on your own computer.
