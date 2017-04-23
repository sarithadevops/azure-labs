# Wunderlist - Logic App

## Objective & Audience

Add a task in Wunderlist, and have the due date blocked in your calendar and an email sent to you.

This lab gives you a hands-on experience how Azure Logic Apps work, you do not have to be a software developer to carry out the exercise.

## What you need

1. A modern web browser - all tasks can be performed there
2. Access to [Microsoft Azure](http://portal.azure.com) and the ability to provision resources there
3. [Google Account](http://www.gmail.com) - for email and calendar
4. A free account at [Wunderlist](http://www.wunderlist.com) - a great task manager for you and your team

## 1 - Create Accounts

Make sure you can access the Azure portal at [http://portal.azure.com](http://portal.azure.com), then create a GMail account (if you don't want to use your personal one.

Head over to [Wunderlist](http://www.wunderlist.com) and create a free account, they also offer a mobile app for IOS and Android to make task management easy!

## 2 - Create Logic App

In the [Azure Portal](http://portal.azure.com) cick on the + button and click 'Logic App' from the 'Web + Mobile' secion. Name the logicapp `wunderlist` and put it in a new resource group with the same name `wunderlist` in a region of your choice. Click 'Create' and wait until the deployment has succeeded.

![](/img/wl-lab-01?raw=true "")
