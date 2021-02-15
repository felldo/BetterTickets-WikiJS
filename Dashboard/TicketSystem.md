---
title: Ticket System
description: 
published: true
date: 2021-02-15T18:09:33.246Z
tags: ticket system, dashboard, settings
editor: markdown
dateCreated: 2020-09-16T11:55:20.155Z
---

# Ticket System
## What is a ticket system?
A ticket system is the *connector* between your ticket creation method and the ticket settings.
This allows you to have very customizable tickets by having for instance:
> - Pointing every ticket panel to a different category with a different ticket greeting message
> - The same for channels when using the command by restricting the ticket system
{.is-warning}

###### Category
The category where tickets will be created in

###### Transcript Channel
Ticket transcript will be sent into this channel

###### Role on create
When creating a ticket the user will be added to this role. Can be useful for displaying users in a different color to indicate they have a ticket opened

###### Require Role
In order to create a ticket, the user needs to have this role for this ticket system

###### Ticket Name
Displayed as [Name]-0001
Insert:
- `:user:` display the users name

###### Restricted Channels
Restricts this ticket system to a channel. This is only used when creating tickets via command

###### Ticket Welcome Message
Configure the text of the greeting message when creating a ticket
- `:user:` get the mention of the user

***The footer, color and images are Premium only features***