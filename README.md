# Agile-Log

## Table of Contents

- [Description](#description)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)


## Description

A Power Automate flow that helps you remember to keep a logbook in your agile work environment and gives you a quick relevant update after each day.


![Initial Screen](https://github.com/SocksThatRock/Agile-Log/assets/118437480/09a2b654-f9c7-412b-8a35-83edd354c212)



![Log Input](https://github.com/SocksThatRock/Agile-Log/assets/118437480/c2e40aad-4a1b-44b4-a93b-ae66abfad0e9)


![Day Off Input](https://github.com/SocksThatRock/Agile-Log/assets/118437480/4a8c7216-b9ac-46bc-b37c-b3bf73587ede)


![Card update after submit](https://github.com/SocksThatRock/Agile-Log/assets/118437480/161a6bc1-7efc-40cc-a689-ab2f08bbfdc1)



![Elements explained](https://github.com/SocksThatRock/Agile-Log/assets/118437480/f4105781-51d0-460f-8167-b77c87f07145)



## Features


The flow will help you remember to record your logbbok every day

It will keep you informed about the upcoming day's schedule

It will keep you informed about tasks that are soon due

The repository contains images matching every textcolor in [adaptivecards](https://adaptivecards.io/) for Teams, both for Light and Dark mode.




## Requirements

1. A [list](Lists/Logbook.csv) in [Microsoft Lists](https://www.microsoft.com/en-us/microsoft-365/microsoft-lists) to store the log.
+ When importing the list use the following column types:
  - Date = Date and time
  - Task = Choice
  - Progress = Multiple lines of text
  - Thoughts = Multiple lines of text
  - Rating = Choice
  - Day Off = Choice
  - Title = Title
  
  
2. A [list](Lists/InspirationalQuotes.csv) in [Microsoft Lists](https://www.microsoft.com/en-us/microsoft-365/microsoft-lists) to retrieve the quotes 
+ When importing the list use the following column types:
  - Originator = Title
  - Quote = Multiple lines of text
  - Wikilink = Hyperlink

When you have created these lists, go into settings and copy the URL up to the "Lists" part. As such: 	https://YOUR_DOMAIN-my.sharepoint.com/personal/YOUR_USER/Lists


3. Your current backlog items in [Planner](https://tasks.office.com/)

4. The [images representing buttons](AdaptiveCard_Buttons) stored in your personal OneDrive

5. In Power Automate you need to establish connections for the following applications:

   - Office 365 Users
   - Sharepoint
   - Microsoft Teams
   - Planner
   - Office 365 Outlook

![image](https://github.com/SocksThatRock/Agile-Log/assets/118437480/740f9cf6-8787-429b-bc03-9382f885ecf3)


## Installation

When all requirements have been met, import [Agile_Logbook_Pt1](Power_Automate_Flows/Agile_Logbook_Part1.zip) to Power Automate. 

You can adjust when you want to be reminded about the logbook and during which days in the first step of the flow
![image](https://github.com/SocksThatRock/Agile-Log/assets/118437480/4c571504-1881-487c-9f8b-24a967e57a3d)

The JSON for the adaptive card needs to be updated with your own URLs for the four images.
![Default Image URL](https://github.com/SocksThatRock/Agile-Log/assets/118437480/492418a9-7f59-45c6-be4f-201d5b673fe9)

You can use the [Adaptive Card Designer](https://adaptivecards.io/designer/) to make sure that the URLs are working correctly. 

When you are happy with the changes, copy the JSON from the designer into the Adaptive Card step, keep the designer open still because you will need to copy/paste this code a second time.

![image](https://github.com/SocksThatRock/Agile-Log/assets/118437480/139de73a-52a8-412f-8b15-4673ed1d79df)

Show advanced settings and make sure the Card Type ID is "Logbook"
![image](https://github.com/SocksThatRock/Agile-Log/assets/118437480/6c6e3c12-3bc3-4ec3-97f6-ee899e6e5568)

Save the flow.


Import [Agile_Logbook_Part2](Power_Automate_Flows/Agile_Logbook_Part2.zip) into Power Automate.


Replace "My Site" with the URL you copied in step 2 of requirements and then you will be able to choose the Logbook list from the dropdown menu.

![image](https://github.com/SocksThatRock/Agile-Log/assets/118437480/6bd95b5b-0a58-40ca-a052-6b563048f6a6)


Fill out the fields in the list with the corresponding dynamic fields
![image](https://github.com/SocksThatRock/Agile-Log/assets/118437480/c5f31057-d78a-4689-ad7e-9a605093c7a7)

Same as the prior step, replace "My Site" with the correct URL and the Quote list should become avaliable in the dropdown.
![image](https://github.com/SocksThatRock/Agile-Log/assets/118437480/247d54f4-af9a-4067-aefa-e74945983885)

Remove "Calendar" and replace it with the calendar of your choice from the dropdown
![image](https://github.com/SocksThatRock/Agile-Log/assets/118437480/fb5798f6-7f23-4edb-9f25-c03c2f71a2dd)

Finally, copy the JSON from Part 1 into the first step of the Part 2 flow.

Save both flows, and initiate a manual test for Part1, you should get a message in Teams, fill out the inputs and submit, this should trigger Part2.












