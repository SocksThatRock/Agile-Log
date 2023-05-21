# Agile-Log

## Table of Contents

- [Description](#description)
- [Requirements](#requirements)
- [Installation](#installation)

## Description

A Power Automate flow that helps you remember to keep a logbook in your agile work environment and gives you a quick relevant update after each day.


![Initial Screen](https://github.com/SocksThatRock/Agile-Log/assets/118437480/09a2b654-f9c7-412b-8a35-83edd354c212)



![Log Input](https://github.com/SocksThatRock/Agile-Log/assets/118437480/c2e40aad-4a1b-44b4-a93b-ae66abfad0e9)



![Card update after submit](https://github.com/SocksThatRock/Agile-Log/assets/118437480/7ee7bef0-7014-4739-901f-f101620aba87)



![Elements explained](https://github.com/SocksThatRock/Agile-Log/assets/118437480/f4105781-51d0-460f-8167-b77c87f07145)






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

3. Your current backlog items in [Planner](https://tasks.office.com/)

4. The [images representing buttons](AdaptiveCard_Buttons) stored in your personal OneDrive




## Installation


