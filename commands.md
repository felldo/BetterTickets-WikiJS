---
title: Commands
description: Explanation of commands
published: true
date: 2021-02-16T00:22:01.019Z
tags: commands
editor: markdown
dateCreated: 2021-01-21T12:06:50.536Z
---

# Commands

## Commands for everyone
> Arguments inside `<>` are optional and do not have to be present.
Argument inside `[]` have to be provided for the command to work.
{.is-info}

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
|⭐<nobr>autoClose \<Number></nobr>  	| `-autoClose 48`						  	| Sets the (new) ticket auto close timer which will close the ticket according to [Number] hours after the last message was sent in this ticket. No argument to remove a current existing timer             	|

- ### Usable everywhere
|       Command         										|    Example                 					| Description 																																										|
|:----------------------------------------	|:---------------------------------- |:---------------------------------------------------------------------------------------------	  |
| blacklist [@User / ID] 										| `-blacklist @Domme`         				 	| (Un)blacklists a user for creating tickets        																				    	|
| blacklists          										  | `-blacklists`  												| Get a list of all blacklisted users          																										|
| ticket [@User / ID]    										| `-ticket @Domme`       	  			    	| Overview of all tickets of the user           																								 	|
| ticket [@User / ID] [Ticket ID]       	  | `-ticket @Domme 1` 										| Receive the transcript            																															|
|⭐closeAll <#Channels> 										  | `-closeAll #ticket-0001 #ticket-0003` | Closes all opened tickets. If an argument is provided only the mentioned tickets will be closed	|

## Admin commands
> The following commands are only usable by users which have the setup admin role or are Administrators / Owner of the server.<hr>
The default value for **system ID** and **panel ID** is always `0` unless you have a premium subscription which allows you to have mutiple ticket systems and ticket panels
{.is-info}

## Configuration commands
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
| requiredRole [SystemID] [@Role / ID]				| `-requireRole 0 @VIP`        								 	| Users need this role to be able to create a ticket for the system 																					|
| setCategory [SystemID] [Category Name / ID] | `-setCategory 0 TICKETS`        						 	| Sets the category for the tickets        																				    												|
| setTranscript [SystemID] [#Channel / ID] 		| `-setTranscript 0 #transcripts`        			 	| Sets the channel which the transcript will be created in      																				    	|
| setRoleOnCreate [SystemID] [@Role / ID] 		| `-setRoleOnCreate 0 @TicketUser`        		 	| Sets a role which the user will be added to when creating a ticket(This is not required for anything!)    	|
| ticketName [SystemID] [Name] 								| `-ticketName 0 myNewTicketName`        			 	| Sets the name for the ticket e.g. NAME-123 | :user: to get the user name        													 	|
| delMsg [SystemID] 													| `-delMsg 0`        													 	| Deletes the message when creating a ticket        																				    							|
| reqSubject [SystemID] 											| `-reqSubject 0`        				 								| Determines if the ticket requires a subject to be created        																				   	|
| restrict [SystemID] [#Channel/ID]  					| `-restrict 0 #ChannelToRestrictTo`      		 	| Restrict ticket creation within this Channel (Multiple channels are possible) (Only needed when creating a ticket with command)        	|
| setOpen [SystemID] 													| `-setOpen 0`        												 	| Turn ticket creation on / off        																				    														|
| systemInfo 																	| `-systemInfo`        												 	| Shows all systems with their configurations        																				    							|
|⭐addSystem 																	| `-addSystem`        												 	| Create a new configurable System        																				    												|
|⭐removeSystem [System ID] 										| `-removeSystem 1`        				 							| Deletes the system with the given id        																				    										|
| setMsg [SystemID] [Message] 								| `-setMsg 0 Welcome :user:`        						| Sets the ticket message.<br>Special: {{ }} for text outside the embed | :user: to mention the user	    		|
|⭐systemFooterMsg [SystemID] [MESSAGE] 				| `-systemFooterMsg 0 Footer Message in embed`	| Sets the footer message of the ticket welcome message.        																				    	|
|⭐systemFooterUrl [SystemID] [URL] 						| `-systemFooterUrl 0 https://link.jpg`   		 	| Sets the footer image of the ticket welcome message. Valid URL's end with: .png | .jpg | .gif.    		    	|
|⭐systemUrl [SystemID] [URL]  								| `-systemUrl 0 https://link.gif`        			 	| Sets the image of the ticket welcome message. Valid URL's end with: .png | .jpg | .gif.        					   	|
|⭐systemColor [SystemID] [HEX color code] 		| `-systemColor 0 FF5733`       				 				| Sets the color of the ticket welcome message. Color has to be a hex color code e.g.: #1C455F . The color code is everything after the #        |

- ### Ticket Panel
|       Command  														|    Example                 																								  	| Description																					            					|
|:-----------------------------------------	|:----------------------------------------------------------------------------- |:-----------------------------------------------------------------------	  |
| ticketPanel [PanelID] 										| `-ticketPanel 0`      																							 				 		| An alternative to creating tickets with a command. Uses reactions on a message. **This command prints the ticket panel**        																				    	|
|⭐setSystem [Ticket panel id] [System id] 	| `-setSystem 1 1`        																										 		| Sets the system for the given ticket panel id to the given system id        																				    	|
|⭐addTicketPanel 														| `-addTicketPanel`        																										 		| Create a new ticket panel         																				    	|
|⭐removeTicketPanel [Ticket panel id] 			| `-removeTicketPanel 1`        																							 		| Removes the ticket panel with the given id        																				    	|
| panelInfo																	| `-panelInfo`        																												 		| Shows all ticket panels with their configurations
‎        																				    	|
| ticketPanelMsg [PanelID] [MESSAGE] 				| -ticketPanelMsg 0 React to create a ticket <br>0️⃣ Subject 1 <br>1️⃣ Subject 2 	 | Sets the message of the ticket panel. Emoji numbers from :zero: to :nine: are reserved. You can use them to specify different ticket subjects. **The text after the numbers will be the subject of the ticket until you insert a new line!** If this message has been updated you have to re-use the ticketPanel command        																				   		 	|
|⭐panelFooterMsg [PanelID] [MESSAGE] 				| `-panelFooterMsg 0 Message in the footer`        				 												|	Sets the footer message of the ticket panel.         																				    	|
|⭐panelFooterUrl [PanelID] [URL]  					| `-panelFooterUrl 0 https://link.jpg`        																	 	| Sets the footer image of the ticket panel. Valid URL's end with: .png | .jpg | .gif.        																				    	|
|⭐panelUrl [PanelID] [URL] 									| `-panelUrl 0 https://link.gif`        																				 	| Sets the image of the ticket panel. Valid URL's end with: .png | .jpg | .gif.        																				    	|
|⭐ panelColor [PanelID] [HEX color code] 		| `-panelColor 0 FF5733`        																							 		| Sets the color of the ticket panel. Color has to be a hex color code e.g.: #1C455F . The color code is everything after the #        																				    	|
  
  