---
title: Ticket System
description: 
published: true
date: 2023-01-07T17:35:00.844Z
tags: ticket system, dashboard, settings
editor: markdown
dateCreated: 2020-09-16T11:55:20.155Z
---

# Ticket System
## What is a ticket system?
A ticket system is the *connector* between your ticket creation method and the ticket settings.
This allows you to have very customizable tickets by having for instance:

> • Pointing every ticket panel to a different category with a different ticket greeting message. 
> • The same for channels when using the command by restricting the ticket system to a channel.
{.is-info}

### Category
The category where tickets will be created in.

### Transcript Channel
Ticket transcript will be sent into this channel.

### Role on create
When creating a ticket the user will be added to this role. Can be useful for displaying users in a different color to indicate they have a ticket opened.

### Require Role
In order to create a ticket, the user needs to have this role for this ticket system.

### Ticket Name
Displayed as [Name]-0001
Insert:
- `:user:` to display the users name in the ticket name

### Restricted Channels
Restricts this ticket system to a channel. This is only used when creating tickets via command.

### ⭐ Claimed ticket category
If you claim a ticket, this option allows you to ***optionally*** move this ticket to another category.

### ⭐ Default Ticket Auto Close in Hours
The default hours a ticket should be closed after the last message has been send.

### Message ID (Ticket greeting message)
This will be the ticket greeting [Message](/Dashboard/Messages) for this ticket system.

### Ticket creation requires a subject?
Whether the command to create a ticket needs a subject or not.
![createcommandsubject.png](/createcommandsubject.png)
### Delete Ticket create message?
Whether the ticket create command should be deleted or not after 20 seconds.
![createcommand.png](/createcommand.png)
### Users can create tickets?
Enables / Disables the ability to create tickets for this ticket system.

### Send "@User your requested ticket has been created" confirm messages
Notifies the user that his ticket has been created.
![yourrequestedtickethasbeencreated.png](/yourrequestedtickethasbeencreated.png)

### ⭐ Activate steam authentication 
Whether a steam authentication button should be attached to the ticket create message. The authenticated information will look like:
![steam_auth.png](/steam_auth.png)