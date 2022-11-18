---
Title: Create a WeBWorK Homework Set
Date: 2009-04-07
---

# Create a WeBWorK Homework Set

!!! warning "Caution - Outdated Instructions"

    These instructions were written for an instructors' workshop in 2009.
    Many things have changed in the WeBWorK system since then.
    Use them with caution.

## Create a new homework set

Select Hmwk Sets Editor (under Instructor Tools in the Main Menu on the left)

1. In the top list of choices select the radio button :material-radiobox-marked:Create a new set named:
2. Give your new set a name.
    * Some teachers like to prefix with set name with a sequence number, or some other identifier: _ASN_ or _Review_ etc.
3. Leave the default as a new empty set selected and press the :material-button-cursor: Take Action! button. WeBWorK reports the success (or failure) of the action at the top of the page (just under the header Hmwk Sets Editor).
4. Your new set will show up in the list of homework sets at the bottom of the page. It has zero questions and is assigned to zero users.

## Add problems to your set

Select Library Browser (from the Main Menu on the left).

1. In the Library Browser choose your set from the drop down box Add problems to Target Set:
1. Under the section of the screen where you just selected your set is the section where you choose which library to work in. You have various options - the default option, the National Problem Library, is the question library we will use today.
1. Choose a Subject, Chapter, and Section of the National Problem Library to search for questions.
1. Choose your preferred display mode. Any one should work for today. jsMath and LaTeXMathML are preferred, but both can have problems on slow computers or older browsers.
1. Now press the View Problems button.
You should see a list of problems, each in a box.
Generally you will proceed by marking problems to add to the set
then updating the set to add the problems that you have marked to the set.
    - Above the list of problems are a number of buttons:
    Mark All For Adding, Clear All Marks, and Update Set do what they say they do.
    Re-randomize will show you the same problems with a different random seed.
    Clear Problem Display will not undo any changes that you have made to the set with Update Set,
    but otherwise will reset the display back to before you pressed View Problems.
    - At the top of each problem box is the file name of the problem. This is followed by two check boxes. The first, Don't show this problem on the next update, you can select if you have definitely decided that you won't use this problem in this homework set. Select the second box, Add this problem to the target set on the next update, to add the problem to your set. Neither box has any effect until you press the Update Set button. At the right of each problem box are two links Edit it and Try it. Edit it allows you to edit a local copy of the source code for the problem. Editing the source code is not a topic for today's seminar (it can be complicated to randomize the problems properly), but you may want to take a peek at one to see what the source code looks like. The Try it link allows you try the problem from a student's point of view.
1. Select problems with the Add this problem to the target set on the next update box and add them to your set by pressing the Update Set button.

## Homework set detail

Once you are satisfied with the problems in the set go back to the Hmwk Sets Editor.

1. You should see your set listed at the bottom of the page. From here you can Edit Set Data (by clicking the pencil), you can edit the set detail (by clicking the number of problems under Edit Problems), or assign the set to students (by clicking the 0/15 under Edit Assigned Users).
2. Click the number under Edit Problems to go to the Set Detail page for your homework set. Under General Information set an opening date, due date, and answer display date for your assignment. The date format is MM/DD/YYYY. We don't know (yet) how to change this.
3. The defaults Visible to Students: Yes and Assignment type - homework are fine for us. Each homework set has two headers associated with it. One is displayed as part of the web page when the student views at the homework set on our WeBWorK site. The second is displayed at the top of the pdf page when the student prepares to print a hardcopy of the assignment. For now use the default headers.
4. The rest of the page allows you to fine tune the assignment by reordering problems or changing their weighting. You can also restrict the number of attempts allowed for a problem. Unlimited attempts is the default and this is what we recommend.
5. Choose Save Changes before you leave this page, else all your work here will be lost. Your set is ready to go. It only remains to assign the set to some students.

## Assign homework set to users

Go back to the Hmwk Sets Editor.

1. For your set, under Edit Assigned Users you should see 0/15 indicating that your set is assigned to none of the 15 students and professors in this course. Click on 0/15 to remedy this.
2. On the Users Assigned to Set ... screen you can either:
    - Click the button Assign to All Current Users, assigning the set to all users in the course or,
    - Assign the set to a subset of course users by checking the relevant boxes and pressing the Save button.

## Proofread the homework set

Before quitting, proofread your assignment.

1. Once you have assigned your set to yourself, you should see it listed in the Main Menu under Homework Sets. Clicking this link will take you to a display similar to what the students see.
2. Read the contents of the Set Info box on the right of the page ensuring that it says what you want to say.
3. Step through the problems as another check. You will see the problem source file name listed for your benefit. The students do not see this.
4. Go back up to the problem list and click Download a hardcopy of this homework set. Leave all of the options here alone, scroll to the bottom of the page and press the Generate hardcopy for selected sets and selected users button. Proofread this pdf file as well (it uses a second header file).
