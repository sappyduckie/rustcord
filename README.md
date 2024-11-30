# rustcord
A small open-source project written in rust as a discord mock using pure SMS, RCS and MMS and no server, only local storage. Starting with Android first, porting to iOS later.

The roadmap follows:
- Interception of SMS/RCS/MMS messages
- Store messages in a local database using SQLite
- Simple UI
- Send and receive contacts as 'profiles' through a hidden header message in MMS
- Possibly add usernames to be used instead of phone numbers for privacy, though the messaging will still occur through text
- Encryption of messages and contacts, stored locally
- Discord functionality: create "servers" which will be sets of groupchats listed as 'channels' in the UI
- Flesh out UI
- Come up with a better name than rustcord