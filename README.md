Zach Miller, Safer Muhammet, Jason Rummel, Muhammad Habib

This zipped folder includes: APK, Unit Tests, This Readme file and our repository.
This document contains details our source code, github repositories, User Manual and Team Member contributions.


The source code:
All needed files are under directory Android-Gui-Test. There are directions in the repository to where each file is needed to be added to run smoothly.
	MainActivity
	Events
	MySimpleArrayAdapter
	Layout Directory:
		activity.xml
		custom.xml
		custom2.xml
	Anim Directory:
		slide_in_from_left
		slide_in_from_right
		slide_out_to_left
		slide_out_to_right


	
Repositories:
The final product is under Dallaskurd's profile, but there was a fork and some commits to the second link as well.
https://github.com/dallaskurd/Software-Engineering-Project.git
https://github.com/zmiller2015/Calendar.git



Scope of Project:
	To display a working calendar that features month, week and day view. The Calendar features a add event method that will record and save events.

User Manual:
	The app is coded in Java through Android Studio. The layout of the app is written in XML which links up views associated with our calendar: monthly, weekly, and day. We imported the calendar utility from Java to generate calendar objects to build views on app start and to compare dates for loading events. 
Navigating the Calendar:
	The calendar has three views: month, week and day. The default view is month. The user can navigate between each view with swipe gestures. Month view is the farthest to the left and can only be navigated away from by swiping left. The Day view is farthest to the right and can only be navigated away from by swiping to the right. The Week view is in the middle of Month and Day. To view a Day from the Month or Week views the user must click on that day and the day's events will be presented in a pop up window. 
Add Events:
	There are three options to adding events for the user. There is a 'Add Event' Button in the top left corner of the app which is visible in both month view, week view and day view. A pop up menu will prompt the user with the necessary fields to create an event. Additionally, while in month or day view the user can click on a day and a pop-up window will prompt the user to view that days events and there is an option to create a new event at the bottom of the prompt.
Delete Events:
	To delete an event the user must click on the day with the event in either month or week view. After clicking a pop-up window will prompt the user with the events of that day. Then the user must click on the an event and at the bottom of this pop up window will be a button labeled 'delete'.
Adding Categories:
	To add a category click the add category button in the upper right corner and create a new category by name and color type. If a category is created that already exists nothing will happen and the original category will persist.

Team Contributions:

Jason did most if not all of the implementation to the Final Product of the Calendar. After a certain point in the progress, the team felt most comfortable designing a process or method then handing it off to Jason to integrate into the App. He piloted the design and look of the final product. He also guided other team members to completion with methods they were having difficulty completing. 

Safer also created a Calendar App that we did not end up using but built into a functing month view. Safer provided a substancial amount of information and knowledge about how best to implement methods and save information in the App. He completed the conflict code and worked with other team members to do this is a concise way. 

Muhammet completed the add event code which Jason implemented in the beginning versions of the app. Muhammet also wrote the Javadoc.

Zach wrote the code for the Holidays, the readme and the user manual. He tried the event categories with Jason and Safer's help but failed. Zach also organized meetings with the group. 

All team members attended meetings and provided meaningful input to the implementation and the progress of the app.


