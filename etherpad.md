A combination of notes from all Otago ResBaz2017 etherpads:
- http://pad.software-carpentry.org/resbaz-dunedin-2017-201
- http://pad.software-carpentry.org/resbaz-dunedin-2017-202
- http://pad.software-carpentry.org/resbaz-dunedin-2017-203

Welcome to Software Carpentry Etherpad!

This pad is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

Use of this service is restricted to members of the Software Carpentry and Data Carpentry community; this is not for general purpose use (for that, try etherpad.wikimedia.org).

Users are expected to follow our code of conduct: http://software-carpentry.org/conduct.html

All content is publicly available under the Creative Commons Attribution License: https://creativecommons.org/licenses/by/4.0/


Welcome to Room 201,202,203!

Welcome to the Research Bazaar Dunedin

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




##SWC Shell (Day1)

Notes:
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
    # - comment symbol, can add notes to scripts (these lines won't run)
    


##SWC R (Day2)

Notes:  

    http://swcarpentry.github.io/r-novice-inflammation/
    
    http://swcarpentry.github.io/r-novice-inflammation/files/r-novice-inflammation-data.zip
    
    git clone https://github.com/swcarpentry/r-novice-inflammation.git

    getwd() = It will give you information where you are or what is your PATH (in R studio).
    Assigning value to some variable use "<-" sign.
    e.g: to assign 123 to weight  write it in a way weight  <-  123
    use # to write any comment in R studio


    


##SWC Git (Day3)

Notes:
 
    
# Advanced Morning Sessions

##ResBaz R Packages (Day1)

Notes:
    
https://github.com/mikblacklab

https://github.com/mikblacklab/ResBazLessons2017/tree/master/R_Packages_Functions


##ResBaz R Reproducible Research (Day2)

Notes:

https://github.com/mikblacklab/ResBazLessons2017

http://www.markdowntutorial.com/
    
   

##ResBaz R Shiny (Day3)

Notes:

# Afternoon Sessions   

##ResBaz mini-session Advanced Shell (Day1)

Notes:
    
##ResBaz mini-session parallel computing and scripting in R (Day1) with the New Zealand eScience Infrastructure

Notes:
    
##SWC SQL (Day1)

Notes:

setup: https://swcarpentry.github.io/workshop-template/

lessons  http://swcarpentry.github.io/sql-novice-survey/
      
    

##ResBaz mini-session Introduction to Python (Day2)

Notes:
    

##ResBaz mini-session Data Manipulation and Plotting in R (Day2)

Notes:

https://github.com/mikblacklab/ResBazLessons2017/tree/master/R_Data_Manipulation_and_Plotting

    

##ResBaz mini-session Introduction to Command-line tools (Day2)

https://www.cog-genomics.org/plink2

https://vcftools.github.io/examples.html
mkdir MyTools
mkdir bin
ln -s /c/Users/whoyouare/MyTools/Plink/plink bin/plink2    
    

##ResBaz mini-session Jupyter Notebooks (Day2)

Notes:
   
    
## ResBaz mini-session Jupyter Notebooks Python session (Day2)

Make sure that your Python environment is set up as documented on http://swcarpentry.github.io/python-novice-inflammation/setup/

(You can use a cloud-based Jupyter notebook, but will need to handle your files differently for that to work.)

https://jupyter.org
Try it in your browser
Top right: make new Python3 notebook
(You can use a cloud-based Jupyter notebook, but will need to handle your files differently for that to work.)
