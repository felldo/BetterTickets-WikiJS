---
title: Commands
description: Explanation of commands
published: true
date: 2021-08-08T14:56:38.336Z
tags: commands
editor: markdown
dateCreated: 2021-01-21T12:06:50.536Z
---

# Commands
> Arguments inside `<>` are optional and do not have to be present.
Argument inside `[]` have to be provided for the command to work.<br>
To get the ID of something:<br>Settings -> Appearance -> Scroll all the way down -> Activate Developer mode. <br>Then just right click a role, channel, category or user and copy its ID
{.is-info}

## Commands for everyone
- ### General commands
|       Command        	|    Example	| Description 									|
|:-------------------   |:--------- 	|:-----------			  						|
| dash						    	| `-dash` 	 	| Link to the dashboard        	|
| help    							| `-help`    	| Shows the available commands  |

- ### Ticket commands
|       Command        	|    Example           	| Description 																																																														|	
|:-------------------  	|:------------------- 	|:--------------------------------------------------------------------------------------------------------------------------------------	|
| new	\<Subject>			  | `-new I need help` 		| Creates a new Ticket.<br>Moderators can supply a user as 2nd argument (-new @Domme) to create a ticket for the mentioned user    				|
| close \<Reason>     	| `-close Solved`    		| Closes the ticket. Write this command twice to close a ticket or optionally supply a reason to instantly close the ticket								|

## Moderator commands
> The following commands are only usable by users which have the setup moderator/admin role or are Administrators / Owner of the server
{.is-info}
- ### Usable only inside a ticket
|       Command        	|    Example                  	| Description 	|
|:-------------------  |:--------------------------- 	|:-----------	|
| <nobr>add [@User / ID]</nobr>   	  | `-add @Domme`               	| Adds the given user to a ticket            																																			|
| <nobr>remove [@User / ID]</nobr> 	| <nobr>`-remove 186907597499138048`</nobr> 	| Removes the given user from a ticket            																																|
| <nobr>owner [@User / ID]</nobr>  	| `-owner @Domme`             	| Changed the owner of the ticket to the given user         																									   	|
| <nobr>rename [Name]</nobr>       	| `-rename `        			  		| Renames the ticket. Due to limitations from discord this is only twice every 10 minutes possible            		|
|⭐claim               	| `-claim`     						    	| Claims a ticket for a supporter. Optionally you can setup a category where the ticket will be moved to. Currently you can only setup this in the dashboard            	|
|⭐<nobr>autoClose [Number] \<Reason></nobr>  	| `-autoClose 48 Closing after 48hours of inactivity`						  	| Sets the (new) ticket auto close timer which will close the ticket according to [Number] hours after the last message was sent in this ticket. No argument to remove a current existing timer             	|

- ### Usable everywhere
|       Command         										|    Example                 					| Description 																																										|
|:----------------------------------------	|:---------------------------------- |:---------------------------------------------------------------------------------------------	  |
| blacklist [@User / ID] 										| `-blacklist @Domme`         				 	| (Un)blacklists a user for creating tickets        																				    	|
| blacklists          										  | `-blacklists`  												| Get a list of all blacklisted users          																										|
| ticket [@User / ID]    										| `-ticket @Domme`       	  			    	| Overview of all tickets of the user           																								 	|
| ticket [@User / ID] [Ticket ID]       	  | `-ticket @Domme 1` 										| Receive the transcript            																															|
|⭐closeAll <#Channels> 										  | `-closeAll #ticket-0001 #ticket-0003` | Closes all opened tickets. If an argument is provided only the mentioned tickets will be closed	|

## Admin configuration commands
> The following commands are only usable by users which have the setup admin role or are Administrators / Owner of the server.<hr>
The default value for **system ID** and **panel ID** is always `0` unless you have a premium subscription which allows you to have mutiple ticket systems and ticket panels
{.is-info}
- ### General
|       Command  							|    Example               	  	| Description 																																													            													|
|:--------------------------	|:---------------------------- |:-----------------------------------------------------------------------------------------------------------------------------------------	  |
| autoSetup										| `-autoSetup`         				 	| An automatic setup of the bot (Recommended)        																																										    	|
| prefix [Prefix]							| `-prefix $`       				 		| Set a custom prefix        																				    																																			|
| devmode [#Channel / ID]			| `-devmode #devmode-channel`   | Sends messages with information for other bot developer to a channel																																		    |
| modRole [@Role / ID]				| `-modRole @botModRole`       	|  Set the mod role for ticket moderation        																				  																									  |
| adminRole [@Role / ID]			| `-adminRole @botAdminRole`   	| Set the admin role to configure the bot        																				  																									  |
| maxTickets [Number]					| `-maxtickets 10`        			| Sets the maximum amount of tickets one user can create        																																					    |
| restrictClose \<@Role / ID>	| `-restrictClose @SupportTeam` | Only ticket moderators or higher can close tickets. If a role is given the role will be mentioned that the user wants to close the ticket   |

- ### Ticket System
|       Command  															|    Example                 									| Description																																						            					|
|:------------------------------------------	|:------------------------------------------- |:---------------------------------------------------------------------------------------------------------	  |
| systemInfo 																	| `-systemInfo`        												 	| Shows all systems with their configurations        																				    							|


- ### Ticket Panel
|       Command  														|    Example                 																								  	| Description																					            					|
|:-----------------------------------------	|:----------------------------------------------------------------------------- |:-----------------------------------------------------------------------	  |
| ticketPanel [PanelID] 										| `-ticketPanel 0`      																							 				 		| An alternative to creating tickets with a command. Uses reactions on a message. **This command prints the ticket panel**        																				    	|
| panelInfo																	| `-panelInfo`        																												 		| Shows all ticket panels with their configurations  	|