A combination of notes from all Otago ResBaz2017 etherpads:
- http://pad.software-carpentry.org/resbaz-dunedin-2017-201
- http://pad.software-carpentry.org/resbaz-dunedin-2017-202
- http://pad.software-carpentry.org/resbaz-dunedin-2017-203

Welcome to Software Carpentry Etherpad!

This pad is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

Use of this service is restricted to members of the Software Carpentry and Data Carpentry community; this is not for general purpose use (for that, try etherpad.wikimedia.org).

Users are expected to follow our code of conduct: http://software-carpentry.org/conduct.html

All content is publicly available under the Creative Commons Attribution License: https://creativecommons.org/licenses/by/4.0/

# Welcome to the Research Bazaar Dunedin
## Welcome to Room 201,202,203!

Feb 8 - 10 2017

See here for our schedule:
https://2017.resbaz.com/dunedin

Software Carpentry Code of Conduct: https://software-carpentry.org/conduct/

Set up instructions for the Software used in these workshops can be found here: https://mikblack.github.io/2017-02-08-dunedin/
Please contact one of our helpers if you need any assistance setting up your laptop (or questions about the content).


Notes for our workshops are on the Software Carpentry website or uploaded to our GitHub:
   
   SWC Shell (Day1): http://swcarpentry.github.io/shell-novice

   SWC SQL (Day 1 elective): http://swcarpentry.github.io/sql-novice-survey/
   
   SWC R (Day 2): http://swcarpentry.github.io/r-novice-inflammation
   
   SWC Git (Day 3): http://swcarpentry.github.io/git-novice
   
   ResBaz R lessons (Shiny, Packages, Parallel): https://github.com/mikblacklab/ResBazLessons2017
   
https://github.com/mikblacklab/ResBazLessons2017/tree/master/R_Shiny_Web_Apps


# Morning Sessions

## SWC Shell (Day1)

Notes:
```
   ~ shortcut for home directory
   mkdir make directory
   \ allows terminal to read folders with a 'space' in the name. Avoid spaces 
    
    nano Thesis.txt             ## mac and linux has nano installed
    notepad Thesis.txt       ## windows default
    touch Thesis.txt            ## create a file without opening and editor
    
    COMMANDS WE LEARNT TODAY:
    cd - change directory
    pwd - present working directory
    ls - list
    ls -F list with slashes at end of floder
    mkdir folder - make a directory
    rm - remove
    rmdir - remove directory
    rm -R -i - remove recursively (all folders, sub-folders, & sub-files) but ask me before things get deleted
    head - first 10 lines
    tail - last 10 lines
    less - take a look in whole file (q to quit)
    touch - make an empty file
    nano - open text file to edit it
    | - pipe symbol, separates commands, work one after the other
    * - wildcare symbol
    for this in that; do things; done - the necessary structure of a for loop (italic is changeable portions)
    script.sh - saving commands to a script (end scripts in .sh)
    bash script.sh - run a script
    $1 - name of the first variable in a script
    \# - comment symbol, can add notes to scripts (these lines won't run)
```    


## SWC R (Day2)

Notes:  

    http://swcarpentry.github.io/r-novice-inflammation/
    
    http://swcarpentry.github.io/r-novice-inflammation/files/r-novice-inflammation-data.zip

```
    git clone https://github.com/swcarpentry/r-novice-inflammation.git

    getwd() = It will give you information where you are or what is your PATH (in R studio).
    Assigning value to some variable use "<-" sign.
    e.g: to assign 123 to weight  write it in a way weight  <-  123
    use # to write any comment in R studio
```   


## SWC Git (Day3)

Notes:


    
# Advanced Morning Sessions


## ResBaz R Packages (Day1)

Notes:
    
https://github.com/mikblacklab

https://github.com/mikblacklab/ResBazLessons2017/tree/master/R_Packages_Functions


## ResBaz R Reproducible Research (Day2)

Notes:

https://github.com/mikblacklab/ResBazLessons2017

http://www.markdowntutorial.com/


## ResBaz R Shiny (Day3)

Notes:



# Afternoon Sessions   

## ResBaz mini-session Advanced Shell (Day1)

Notes:


## ResBaz mini-session parallel computing and scripting in R (Day1) with the New Zealand eScience Infrastructure

Notes:


## SWC SQL (Day1)

Notes:

setup: https://swcarpentry.github.io/workshop-template/

lessons  http://swcarpentry.github.io/sql-novice-survey/


## ResBaz mini-session Introduction to Python (Day2)

Notes:


## ResBaz mini-session Data Manipulation and Plotting in R (Day2)

Notes:

https://github.com/mikblacklab/ResBazLessons2017/tree/master/R_Data_Manipulation_and_Plotting


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


## ResBaz mini-session Jupyter Notebooks (Day2)

Notes:



## ResBaz mini-session Jupyter Notebooks Python session (Day2)

Make sure that your Python environment is set up as documented on http://swcarpentry.github.io/python-novice-inflammation/setup/

(You can use a cloud-based Jupyter notebook, but will need to handle your files differently for that to work.)

https://jupyter.org
Try it in your browser
Top right: make new Python3 notebook
(You can use a cloud-based Jupyter notebook, but will need to handle your files differently for that to work.)
