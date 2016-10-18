# Lobby Info

Here you will be given info about the lobby.
(I SirJosh3917 aka ninjasupeatsninja did this :D )

TODO:

getBlockedUsres
getCampaigns
getCrewInvites
getInvitesToMe
getMails
getNotifications
getPending
getShop

## Messages

### Receive

[connectioncomplete](#rm-connectioncomplete)

[getFriends](#rm-getfriends)

[getMySimplePlayerObjet](#rm-getsimpleobj)

[getLobbyProperties](#rm-getlobby)

### Send

[getFriends](#sm-getfriends)

[getMySimplePlayerObjet](#sm-getsimpleobj)

[getLobbyProperties](#sm-getlobby)

## Receive

### <a id="rm-connectioncomplete">"connectioncomplete"</a>

Occurs when you are connected to the lobby.
Only after this message will you be able to send any messages

0 Entries.

### <a id="rm-getfriends">"getFriends"</a>

Occurs when you send "getFriends".
These items are repeated for every friend you have.

7 Entries for each friend you have.

| Id  | Type        | Name               | Description
| --- | ---         | ----               | -----------
| `0` | String      | Name               | The name of your friend
| `1` | Boolean     | Online             | If your friend is online
| `2` | String      | World Id           | The World Id of the world your friend is playing on ( Doesn't have a value if friend isn't online )
| `3` | String      | World Name         | The World Name of the world your friend is playing on ( Doesn't have a value if friend isn't online )
| `4` | Integer     | Smiley             | The smiley your friend has been wearing since the last world they played on
| `5` | Double      | Offline Time       | The amount of time they've been offline ( Divide by 86400000 to get how many hours )
| `6` | Boolean     | Gold Border        | If that friend has a gold border

### <a id="rm-getsimpleobj">"getMySimplePlayerObjet"</a>

Occurs when you send "getMySimplePlayerObjet" 

| Id   | Type     | Name                  | Description
| ---  | ---      | ----                  | -----------
| `0`  | String   | Name                  | The name of yourself
| `1`  | Integer  | Smiley                | The smiley you were last wearing on a world
| `2`  | Integer  | Aura Shape            | The shape of the aura you were last wearing on a world
| `3`  | Integer  | Aura Color            | The color of the aura you were last wearing on a world
| `4`  | Boolean  | Chat Banned           | If you're banned from using the chat
| `5`  | Boolean  | Can Chat              | If you can chat
| `6`  | Boolean  | Has Smiley Package    | If you have the smiley package of the smiley you're wearing ( Honestly this is not used in .swf so dont bother about this )
| `7`  | Boolean  | Administrator         | If you're an administrator
| `8`  | Boolean  | Moderator             | If you're a moderator
| `9`  | Boolean  | Gold Member           | If you're a gold member
| `10` | Boolean  | Gold Smiley Border    | If you're wearing a gold smiley border
| `11` | Double   | Remaining Time        | How long your gold time remains
| `12` | Double   | Remaining Time        | How long your gold time remains
| `13` | Boolean  | Gold Welcome          | If you just bought gold.
| `14` | String   | Beta Room             | The World ID of your beta room you got from buying beta
| `15` | String   | Beta Only Room        | The World ID of your beta only room you got from buying beta
| `16` | String   | World Payvault Ids    | The payvault IDs of your worlds, separated by a character ( 0x1399 hex, 5017 decimal, 1001110011001 binary )
| `17` | String   | World Ids             | The world Ids of your worlds, separated by a character ( 0x1399 hex, 5017 decimal, 1001110011001 binary )
| `18` | String   | World Names           | The world names of your worlds, separated by a character ( 0x1399 hex, 5017 decimal, 1001110011001 binary )
| `19` | Boolean  | Visible               | ( idk )
| `20` | Boolean  | Banned                | If you're banned
| `21` | Integer  | Accepted Terms        | The version of the terms you have accepted
| `22` | Integer  | Tutorial Version      | The version of the tutorial you have played
| `23` | String   | Badge                 | The badge your wearing ( See badge ids on README.md )
| `24` | Boolean  | Confirmed Email       | If you have confirmed your email.
| `25` | Integer  | Max Energy            | The maximum amount of energy you have
| `26` | Boolean  | Changed Name          | If you have changed your name, this will be true.
| `27` | String   | Favourite Worlds      | A lise of worlds you have favourited, separated by a character ( 0x1399 hex, 5017 decimal, 1001110011001 binary )
| `28` | String   | Favourite World Names | The name of the list of worlds you have favourited, separated by a character ( 0x1399 hex, 5017 decimal, 1001110011001 binary )

### <a id="rm-getlobby">"getLobbyProperties"</a>

Occurs when you send "getLobbyProperties".

It has 2 entries if the first entry is false.
It has 4 entries if the first entry is true.

| Id   | Type     | Name                  | Description
| ---  | ---      | ----                  | -----------
| `0`  | Boolean  | Not First Day         | If it's not your first day to login and get the streak. 
| `1`  | Integer  | Login Streak          | Your login streak, for how many days in a row you logged in.

This message repeats for each reward, which is only one ( usually )

| Id         | Type     | Name                  | Description
| ---        | ---      | ----                  | -----------
| `... + 0`  | Integer  | Amount of it          | How much of the reward your getting
| `... + 1`  | String   | Reward Type           | What you're getting ( Energy, Gems, e.t.c )

##Send

### <a id="sm-getfriends">"getFriends"</a>

You will recieve a message, [getFriends](#rm-getfriends)

This message has 0 entries to send.

### <a id="sm-getsimpleobj">"getMySimplePlayerObjet"</a>

You will recieve a message, [getMySimplePlayerObjet](#rm-getsimpleobj)

This message has 0 entries to send.

### <a id="sm-getlobby">"getLobbyProperties"</a>

You will recieve a message, [getLobbyProperties](#rm-getlobby)

This message has 0 entries to send.
