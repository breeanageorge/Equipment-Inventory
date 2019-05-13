# Equipment-Inventory

For this project, I recreated/updated an existing equipment tracking webpage. This application allows users to view and change information for technology/equipment. The goal of this project was to maintain functionality, fix data inconsistencies, track consumable items, create a change log, and simplify searching. This application was programmed using PHP, MySQL, JavaScript, JQuery, HTML, and CSS.

## Goals and Challenges

A feature from the previous page that we wanted to maintain was the ability to make changes on the "table view"/main page of the application without page refreshes. I accomplished this using JavaScript, AJAX calls, and a PHP handler page.

One of the goals of this project was to clean up data inconsistencies in the MySQL tables. These inconsistencies were caused by users inputting all of the data for an item (such as item, make, model, etc.) which resulted in one model number having several item types and a plethora of typos. I tackled this issue in two ways. The first was to create a new table that contained all of the general information for a piece of equipment (item, make, model, part-number, etc.), using the model as the common data between the new and existing tables. This fixes the issue of conflicting information for the same equipment models. The second step was to remove the possibility of entering a typo, I fixed this by restricting the user to a fixed select input list.

Another goal of this project was to better track quantities of consumable items, which were items we deemed not worth tracking their location (cables, connectors, etc.). These items required much less information than our other equipment, so I created a new MySQL table and separate webpage.

We also wanted a system that tracked changes made on either page so we could have a better idea of the history of a piece of equipment. I created another new table that would act as a change log. When a change on either page is submitted, it updates the correct table with the new information and it adds a new entry to the change log.

I also wanted to make it easier for users to search through all of the equipment we track. Previously we used a select input that you had to scroll through to find the desired search input. With some searching, I found the new HTML5 input datalists. Datalists allow users to search using direct typing input, as a regular select input, and/or by typing part of the desired search narrowing down the list of the select input.

## New Look

Initial landing page:\
![Application landing page picture](/EI_1.PNG)

Searching with datalists:\
![Searching with datalists picture](/EI_2.PNG)

Clicking the ID number button for more information:\
![More information picture](/EI_3.PNG)

Consumable counter page:\
![Consumable counter picture](/EI_4.PNG)
