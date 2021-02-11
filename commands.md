---
title: Commands
description: Explanation of commands
published: true
date: 2021-02-11T16:25:43.859Z
tags: commands
editor: markdown
dateCreated: 2021-01-21T12:06:50.536Z
---

# Commands
    

## Commands for everyone

- ### General commands
|       Command        	|    Example	| Description 									|
|:-------------------  |:--------- 	|:-----------									|
| dash						    	| `-dash` 	 	| Link to the dashboard        	|
| help    							| `-help`    	| Shows the available commands  |

- ### Ticket commands
|       Command        	|    Example           	| Description 																																																															|	
|:-------------------  |:------------------- 	|:--------------------------------------------------------------------------------------------------------------------------------------		|
| new	\<Subject>			  | `-new I need help` 		| Creates a new Ticket.<br>Moderators can supply a user as 2nd argument (-new @Domme) to create a ticket for the mentioned user     				|
| close \<Reason>     	| `-close Solved`    		| Closes the ticket. Write this command twice to close a ticket or optionally supply a reason to instantly close the ticket									|



## Moderator commands
> The following commands are only usable by users which have the setup moderator/admin role or are Administrators / Owner of the server
{.is-info}
- ### Usable only inside a ticket
|       Command        	|    Example                  	| Description 	|
|:-------------------  |:--------------------------- 	|:-----------	|
| add [@User / ID]   	  | `-add @Domme`               	| Adds the given user to a ticket            																																			|
| remove [@User / ID] 	| `-remove 186907597499138048` 	| Removes the given user from a ticket            																																|
| owner [@User / ID]  	| `-owner @Domme`             	| Changed the owner of the ticket to the given user         																									   	|
| rename [Name]       	| `-rename `        			  		| Renames the ticket. Due to limitations from discord this is only twice every 10 minutes possible            		|
| claim               	| `-claim`     						    	| Claims a ticket for a supporter. Optionally you can setup a category where the ticket will be moved to. Currently you can only setup this in the dashboard            	|
| autoClose \<Number>  	| `-autoClose 48`						  	| Sets the (new) ticket auto close timer which will close the ticket according to [Number] hours after the last message was sent in this ticket. No argument to remove a current existing timer             	|

- ### Usable everywhere
|       Command         										|    Example                 					| Description 																																										|
|:----------------------------------------	|:---------------------------------- |:---------------------------------------------------------------------------------------------	|
| blacklist [@User / ID] 										| -blacklist @Domme         				 	| (Un)blacklists a user for creating tickets        																				    	|
| blacklists          										  | -blacklists  												| Get a list of all blacklisted users          																										|
| ticket [@User / ID]    										| -ticket @Domme       	  			    	| Overview of all tickets of the user           																								 	|
| ticket [@User / ID] [Ticket ID]       	  | -ticket @Domme 1 										| Receive the transcript            																															|
| closeAll <#Channels> 										  | -closeAll #ticket-0001 #ticket-0003 | Closes all opened tickets. If an argument is provided only the mentioned tickets will be closed	|

## Admin commands
> The following commands are only usable by users which have the setup admin role or are Administrators / Owner of the server
{.is-info}
## Configuration commands
### General
### Ticket System
### Ticket Panel