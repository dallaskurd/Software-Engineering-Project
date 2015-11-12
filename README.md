Zach Miller, Safer Muhammet, Jason Rummel, Muhammad Habib

Calendar Read Me

Scope of Project:
	To display a working calendar that features month, week and day view. The Calendar features a add event method that will record and save events.

Manual:
	The app is coded in Java through Android Studio. The layout of the app is written in XML which links up views associated with our calendar: monthly, weekly, and day. We imported the calendar utility from Java to generate calendar objects to build views on app start and to compare dates for loading events. 
Navigating the Calendar:
	The calendar has three views: month, week and day. The default view is month. The user can navigate between each view with swipe gestures. Month view is the farthest to the left and can only be navigated away from by swiping left. The Day view is farthest to the right and can only be navigated away from by swiping to the right. The Week view is in the middle of Month and Day. To view a Day from the Month or Week views the user must click on that day and the day's events will be presented in a pop up window. 
Add Events:
	There are three options to adding events for the user. There is a 'Add Event' Button in the top left corner of the app which is visible in both month view, week view and day view. A pop up menu will prompt the user with the necessary fields to create an event. Additionally, while in month or day view the user can click on a day and a pop-up window will prompt the user to view that days events and there is an option to create a new event at the bottom of the prompt.
Delete Events:
	To delete an event the user must click on the day with the event in either month or week view. After clicking a pop-up window will prompt the user with the events of that day. Then the user must click on the an event and at the bottom of this pop up window will be a button labeled 'delete'.
Adding Categories:
	To add a category click the add category button in the upper right corner and create a new category by name and color type. If a category is created that already exists nothing will happen and the original category will persist.
