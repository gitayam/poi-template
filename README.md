-   [Download Template](app://obsidian.md/index.html#Download%20Template)
-   [Update Template](app://obsidian.md/index.html#Update%20Template)
-   [Background of Process and Format](app://obsidian.md/index.html#Background%20of%20Process%20and%20Format)
    -   [Developing Training (Writing)](app://obsidian.md/index.html#Developing%20Training%20(Writing))
    -   [Teaching Developed Training (Reading)](app://obsidian.md/index.html#Teaching%20Developed%20Training%20(Reading))
-   [How to Use This Notebook](app://obsidian.md/index.html#How%20to%20Use%20This%20Notebook)
    -   [Obsidian](app://obsidian.md/index.html#Obsidian)
    -   [ELM](app://obsidian.md/index.html#ELM)
    -   [Academic Hour](app://obsidian.md/index.html#Academic%20Hour)
    -   [Templates](app://obsidian.md/index.html#Templates)
    -   [Comments](app://obsidian.md/index.html#Comments)
    -   [Tags](app://obsidian.md/index.html#Tags)
-   [Notes for Instructors](app://obsidian.md/index.html#Notes%20for%20Instructors)
    -   [NOTES](app://obsidian.md/index.html#NOTES)
    -   [Links](app://obsidian.md/index.html#Links)
    -   [Paraphrasing](app://obsidian.md/index.html#Paraphrasing)
    -   [Verbatim Quotes and Code](app://obsidian.md/index.html#Verbatim%20Quotes%20and%20Code)
    -   [Spacing and New Lines](app://obsidian.md/index.html#Spacing%20and%20New%20Lines)
    -   [Moving to Slides](app://obsidian.md/index.html#Moving%20to%20Slides)
-   [Troubleshooting](app://obsidian.md/index.html#Troubleshooting)
    -   [sed on MacOS](app://obsidian.md/index.html#sed%20on%20MacOS)
    -   [Replace a string in all documents](app://obsidian.md/index.html#Replace%20a%20string%20in%20all%20documents)
    -   [Run Git Commands on Multiple Directories](app://obsidian.md/index.html#Run%20Git%20Commands%20on%20Multiple%20Directories)

## Download Template
1. Graphical Option: Use the Download Button Above
1. Terminal Option (Recommended): 

```BASH
git clone https://gitlab.irregularchat.com/saclab/poi-development.git
```


## Update Template
You must navigate to be inside the directory poi-development and execute the following command:
```BASH
git pull
```

## Background of Process and Format
This structure has been developed after over a year of course development, instruction, and with TRADOC Doctrine, and the SWCS Course Developer Course referenced. Fair warining, there is a lot of reading.

The structure in this notebook diverts from Doctrine and SWCS Instruction where needed based on the unique unit limitations, requirements, and size of unit training compared to training at a center of excellence (CoE)

### Developing Training (Writing)
Start with "POI Development"  and use the provided "Developer Workbook" to analyse jobs, tasks, and the audience to be trained.

---
### Teaching Developed Training (Reading)
Start with "POI Training" and Find the Lesson Plans, the Audio Visual Content, the Evaluations and set up a training area for accordingly.

## How to Use This Notebook 
### Obsidian 
This markdown structure is best when used with [Obsidian](https://obsidian.md/) and the following plugins:
1. Advanced Tables
2. LanguageTool Integration (Spellcheck)

To expand or collapse sections/headers in a note Top Menu > Insert > {"Fold" or “Unfold”}  or configure a keyboard shortcut using the app preferences

### ELM
Training is designed largely based on the Experiential Learning Model (ELM) which is taught at SWCS Course Faculty Course and is a private sector standard as well.
 
If you have not been to the SWCS Course Faculty Course yet, study the following content:
##FIXME: add ELM content for Instructors who have not had formal training

### Academic Hour
50 minutes is used as an “hour” to allow students to take a 10-minute break or two 5-minute breaks. 

### Templates
Templates can be notes or entire folders. Duplicate templates as needed. 

### Comments
Comments are between percent symbols (\%%) and may describe. %%This is an inline comment%%

1. Why something is included, excluded, or modified 
2. How to properly use a section
%%This is a comment which... 

...is...
Comments can be single line or multi-line%%
### Tags
#Knowledge, #Skills, #Resources, and #SupportingTasks should be added as tags to allow for quick sorting and linking

## Notes for Instructors

### NOTES
NOTE is used when an instructor is supposed to perform an action or deliver instruction to students. 

### Links
Pages, Directories, and Files can be linked directly or using relative path formatting. 
![[]]
##FIXME: Add options for linking without absolute path

### Paraphrasing
> Quote Brackets are used to show instructor what needs to be paraphrased, a note will also provide this guidance


### Verbatim Quotes and Code
```md
Code Blocks are used for code 
Code Blocks are also used for verbatim requirments which should not be paraphrased. The code block allows an instructor to easily notice and to copy if needed.
```

### Spacing and New Lines

To Create New Lines , especially inside a table - use \<br\> which will create a line break and continue typing. 

Creating a Line Break with a Line can help when sorting content. Use three (3) - in a single line to create a line break such as this:

### Moving to Slides
`##### SLIDE`  should be used to show movement to new slide. This will allow collapsing and expanding slide instruction and will be represented on the table of contents

---

Spacing and newlines can cause a differences in how Obsidian renders markdown. It is important to include a new line after a "---" line break. 

## Troubleshooting

### sed on MacOS
- Problem: sed for mac is missing some options which limit cross compatibility when replacing a string. 
- Solution: Install gnu-sed and map the PATH as needed. `brew install gnu-sed`

### Replace a string in all documents 
in directory and sub-directories at once. This action should be its own commit to easily undo any unwanted changes. 
- Solution: 
```BASH
grep -RiIl 'Original_String';sleep 5;grep -RiIl 'Original_String' | xargs sed -i 's/Original_String/Replacement_New_String/g'
```

How to Use? Replace Original_String and Replacement_New_String above and input into Terminal inside the desired directory. 
[source](https://www.internalpointers.com/post/linux-find-and-replace-text-multiple-files)

### Run Git Commands on Multiple Directories
- Problem: Multiple git clones, it can be easy to forget which directories need to be updated using `git pull`
- Solution, finding ./git and running the git command on the enclosing directory
```BASH
find . -name .git -print -execdir git pull \;
```