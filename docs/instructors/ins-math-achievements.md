---
title: Custom Math Achievements
authors:
    - Michele Titcombe
date: 2022-11-17
tags:
    - instructors
    - optional modules
    - math achievements
---

# Custom Math Achievements

Math Achievements (or Mathchievements) are an optional WeBWorK module.
!!! quote

    Achievements (or Mathchievements) are gamification features designed
    to reward students for solving homework problems and for practicing good WeBWorK behavior.
    In a nutshell, students can earn achievements by meeting preset goals.
    For example, they might earn an achievement for solving 3 homework problems
    in a row without any incorrect submissions,
    or for solving a problem after taking an 8 hour break.
    Earning achievements and solving problems earns students points
    and after a student gets enough points they will be given a new Level.
    Depending on settings the math level may come with an Achievement Items.
    Students can view their current level and their progress towards various achievements
    by visiting the Achievements page.
    Instructors can modify and administer achievements by using the Achievement Editor page.  
    - [Achievements - WeBWorK Wiki][wiki]

This page is an introduction to writing custom Math Achievements.

!!! warning

    It is strongly suggested that you initially assign achievements to _no users_ and only assign achievements
    to the students once all of your customizations and configurations are done.

    Checking and tracking achievements can be resource intensive, be sparing with the achievemnts
    that you assign to your students.

## Enable Math Achievements

In your course, in **Course Configuration**, select the :material-tab: Optional Modules tab:

* :material-list-box: Enable Course Achievements (default False): :material-arrow-right: set to **True**
* Achievement Points Per Problem (default 5): can be left unchanged
* Enable Achievement Rewards (default False): can be left unchanged
* List of sets excluded from achievements (default - no sets excluded): can be left unchanged
* :material-button-cursor: _Save Changes_

## Use Achievements _Out of the Box_

Once Achievements are enabled in a course,
an **Achievements** summary is available to everyone in the course,
and an **Achievement Editor** is available to instructors.

In the **Achievement Editor**, select the :material-tab: Import tab:

* :material-list-box: _Import from where_ :material-arrow-right: `default_achievements.axp`
* :material-list-box: _Assign this achievement to which users?_ :material-arrow-right: no users
* :material-button-cursor: _Take Action_

## Create a New Achievement

### By modifying an existing achievement

In the **Achievement Editor**, :material-arrow-right: choose an existing achievement,
:material-arrow-right: select _Edit Evaluator_:

* :material-tab: select the _Save As_ tab
* :material-checkbox-marked-circle: _Use in new achievement:_
    - :material-form-textbox: Enter a new achievement ID in the text box, e.g. `MT_Bonus`
* :material-form-textbox: _Save as:_ Enter a filename (ending in `.at`) in the text box, e.g. `MT_Bonus.at`
* :material-button-cursor: _Take Action_

Now the new achievement evaluator can be modified as desired.

### Example - Specific questions on a specific set

The following code in an achievement evaluator gives credit for the achievement
if any of problem numbers 1, 3, or 5 in set _Custom_Math_Achievements_ are correct.

``` pg
# This problem checks to see if particular problems
# of a particular set have been solved

# Define valid problems using this nested hash
my %validproblems = (
       'Custom_Math_Achievements' => { 
           '1' => 1, 
           '3' => 1, 
           '5' => 1, }, 
       );

# Check and see if any of these problems were solved
if ($validproblems{$problem->set_id} &&
    $validproblems{$problem->set_id}{$problem->problem_id} &&
    $problem->status == 1 &&
    $problem->num_correct == 1) {
        return 1;
    }

return 0;
```

### Upload a custom achievement icon

In **File Manager**:

* Go up one level from _Templates_ by clicking the up-arrow to the left of _Templates_
* :material-subdirectory-arrow-right: Select the _html_ subdirectory,
* :material-subdirectory-arrow-right: then the _achievements_ subdirectory,
* :material-file-upload: upload an image file, for example `hanamaru.png`

### Edit the achievement

In the **Achievements Editor**, click the pencil icon :material-pencil: next to your new achievement ID:

* _Name:_ The achievement title displayed to students
* _Category:_ challenge, secret, level, etc
* _Points:_ The number of points gained by attaining this achievement
* _Description:_ The achievement explanation displayed to students.  For example, _Finish at least one of the odd-numbered challenge problems_.
* _Icon File:_ The file name of any of the icons in `/html/achievemnts/`.  `hanamaru.png` for example.

Remember to :material-button-cursor: press the _Take Action_ button to save your changes.

## More information

* [Introduction to Math Achievements][wiki]
* [Creating New Achievements](https://webwork.maa.org/wiki/Achievement_Evaluator#Creating_New_Achievements)
* [New Achievement Icons](https://openwebwork.org/2022/01/25/new-level-badges-and-achievement-icons-for-webwork/)

[wiki]: https://webwork.maa.org/wiki/Achievements
