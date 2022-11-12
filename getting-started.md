---
title: Getting Started
description: 
published: true
date: 2022-11-12T01:09:42.059Z
tags: installing
editor: markdown
dateCreated: 2021-02-02T23:01:29.734Z
---

# Getting started

## Fundamentals
1. Invite the bot via the following link: [Invite](https://discord.com/oauth2/authorize?client_id=553610702439579669&scope=applications.commands%20bot&permissions=2953178200).

2. Create necessarities in Discord
		1. Create a category where the ticket will be created in.
  	2. If you do no already have a support role, create one.

3. Visit the [Dashboard](https://better-tickets.de/), login with your Discord account and select your server in the server overview.

4. Configure your server
		1. Select your previously created supporter role.
    2. Optional: Select a role which should be able to configure the bot besides the owner and server administrators.
    3. Submit your changes.
![getting_started_fundamentals_1_edited.png](/getting_started_fundamentals_1_edited.png)

5. Configure your Ticket System
		1. Go to the `Ticket System` tab in the sidebar
		2. Select your previously created ticket category where the tickets will be created in.
    3. Submit your changes.
![getting_started_fundamentals_2_edited.png](/getting_started_fundamentals_2_edited.png)

6. Go to your server in the Discord Client App.
		1. Go to the server settings
    2. In the category `APPS` click on `Integrations`
    3. Select `Better Tickets`
    4. For the slash commands `/blacklist`, `/ticket` add your supporter role so that they can use these commands
    5. For the slash command `/settings` only allow the admin role if you have configured any in the dashboard

7. You have now setup the most essential settings to get started. You can now start creating tickets with the slash command `/new` and a ticket will show up in your ticket category

## Setup a Ticket Panel

1. Go to the `Message` tab in the sidebar
		1. Add a new Message which will be what our Ticket Panel will look like when you send it to a channel. So make sure it contains everything user need to know **before** they create a ticket
    2. Configure the message how you would like it to look like
    3. Submit your changes
![getting_started_ticket_panel_1_edited.png](/getting_started_ticket_panel_1_edited.png)
1. Go to the `Ticket Panel` tab in the sidebar
		1. Select the `Ticket Panel Mode`. This can be either `reactions`, `buttons` or a `select menu`
    2. Click on the edit button right to the `Ticket Panel Mode` field to configure your the settings for your selected mode
    3. Select the ID of the emssage you have previously added of how the Ticket Panel will look like. Usually this is `#1` if you have followed this tutorial
    4. Submit your changes
    5. Select the channel where you want to send the Ticket Panel to.
    6. Click on the send button to actually send your Ticket Panel to this channel
    7. If the Ticket Panel does not show up, make sure you have setup the `Ticket Panel Mode` properly (step 2)
![getting_started_ticket_panel_2_edited.png](/getting_started_ticket_panel_2_edited.png)
