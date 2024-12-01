# rustcord
A small open-source project written in rust as a discord mock using pure SMS/MMS, RCS and no server, only local storage. Starting with Android first, porting to iOS later.

The roadmap follows (❌ for incomplete / ✅ for complete / 🔲 for TODO):
## 1. Interception of SMS/MMS and RCS messages ❌
## 2. Store messages in a local database using Rusqlite ❌
## 3. Simple UI ❌
- 🔲 view and send messages
- 🔲 receive and display read receipts (optional?)
- 🔲 attach emoji reactions as chars
- 🔲 allow pings (notifications)
- 🔲 view contacts
## 4. Add your own profile into your local database ❌
- 🔲 username (single string UTF-8, attaches a chosen four digit u8 as a usertag)
- 🔲 profile picture (128x128, 8MB max) allows .gif and .png and conversion to either -TBA-
- 🔲 banner (1280x720, 8MB) allows .gif and .png and conversion to either -TBA-
- 🔲 pronouns (list of three string values, UTF-8, last value optionally None)
- 🔲 bio (UTF-8 string, 256 char)
## 5. Send and receive contacts as 'profiles' ❌
- 🔲 through an invisible header message in MMS at the start of any chat or added number/username to contacts
## 6. Possibly add usernames to be used ❌
- 🔲 instead of phone numbers for privacy, though the messaging will still occur through text
## 7. Encryption/Decryption of messages and contacts via AES-256 ❌
- 🔲 Obfuscate strings with a random number generator, send keys within the invisible header, store within userinfo
- 🔲 Obfuscate information sent through RCS (IMEI, IMSI, current IP address)
## 8. Discord functionality ❌
- 🔲 send alongside the invisible MMS header a message informing the endpoint that the currently spoken to user is using rustcord
- 🔲 warn user if a user is being added to a "server" and you have not received the MMS header indicating they are using rustcord
- 🔲 a server will be simply a folder of groupchats being "channels"
- 🔲 include created emojis, (32x32 images with max 512KB) as embeddable images within strings, possibly use unused UTF-8 values to encode them and send the image as sort of texture pack within the message to replace the values
- 🔲 (Optional) set up something like game pidgeon
- 🔲 Group calls, VOIP + cellular will be hard without a server
## 9. Flesh out UI ❌
- 🔲 Make a cute design
- 🔲 Use the image-rs library to implement profile pictures, banners and icons
- 🔲 implement embedded links and media
## 10. Come up with a better name than rustcord ❌
