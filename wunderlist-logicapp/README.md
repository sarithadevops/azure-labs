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

In the [Azure Portal](http://portal.azure.com) cick on the + button and click 'Logic App' from the 'Web + Mobile' section.

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-01.png)

 Name the logicapp `wunderlist` and put it in a new resource group with the same name `wunderlist` in a region of your choice.

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-02.png)

Click 'Create' and wait until the deployment has succeeded.

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-03.png)

Locate your `wunderlist` logic app in the Azure resources or open it by clicking on the "deployment successful" message. The Logic App Editor opens, scroll down and select "Blank Logic App" to start with an empty canvas.

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-04.png)

Explore the connectors and triggers in the list, we're looking for `Wunderlist->When a task is created`.

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-05.png)

When you click on that, you're prompted to create a connection to Wunderlist. A popup should open and - assuming you're already logged in into Wunderlist with your browser - it should be a very quick and easy task to complete.

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-06.png)

Now you will set the parameters for the task, select `inbox` as the task list, and set the `How often do you want to check for items?` to 10 seconds. This will be the frequency of your worklow.

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-07.png)

That was good - let's add another action! Look for `Gmail - Send email`, we want to email the details from the Wunderlist task to you.

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-08.png)

You'll have to create a connection to Google so your logic app can use to the service:

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-09.png)

In the popup please `Allow` access so we can continue the exercise.

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-10.png)

Now we can populate the fields for the `Send email` action, you will see that there are many of them - at this time we only work with `To:` and `Subject:`. You will see that when you click inside one of the fields you are able to select data elements from the previous action. Fill out both fields so they look like the exmple here, and use an email address that you have access to.

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-11.png)

As a last step we would like to add a calendar entry in Google Calendar exactly on the day of the due date of the task. Add a new action and look for `Google Calendar->Create an event`, you'll have to connect the service to your logic app:

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-12.png)

Select the correct calendar from the drop-down list once you click inside the `Calendar ID` field, then populate the `start`, `end` and `summary` fields as shown below. `Due Date` from the `Wunderlist` action is just a calendar date like 2017-05-11, Google Calendar, however, expects a full timestamp so we're adding a time as well.

Save the flow, now let's go test it.

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-13.png)

## Test your flow

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-14.png)

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-19.png)

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-20.png)


![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-15.png)

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-16.png)

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-17.png)

![](https://raw.githubusercontent.com/u1i/azure-labs/master/wunderlist-logicapp/img/wl-lab-18.png)




