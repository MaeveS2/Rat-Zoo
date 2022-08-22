# SkyblockExtrasCrack-2.1.10.1
* **Source:** `https://www.youtube.com/watch?v=wmCZhnXQha8`, which links to `https://www.mediafire.com/file/ocrb9aawktt3zwb/SkyblockExtrasCrack-2.1.10.1.jar/file`
* **Files:** `SkyblockExtrasCrack-2.1.10.1.jar`
* **Author:** CustomPayload
* **Platforms:** Most of the data grabbing will only work on Windows

## Structure
Important files and classes:
* `run.hypixel.dupe.DupeMod.java`: the main class of the mod which is loaded, sends most data to the webhook [1]
* `run.hypixel.dupe.Hooks374.java`: contains the webhook url, in this case a pastebin url leading to the webhook url [2]
* `run.hypixel.dupe.utils.Methoods.java`: gets the mineraft token, ign and UUID and sends it to the webhook along with the SkyCrypt page
* `run.hypixel.dupe.scripts.Scripts.java`: contains information on whether the rat should do certain things, like downloading other malware, encrypting files and asking for ransom [3], or creating spam files.


File structure (some excuded):
```
run/
├─ hypixel/
│  ├─ dupe/
│  │  ├─ exception/
│  │  │  ├─ WebhookExce.java
│  │  │  ├─ WebhookException.java
│  │  ├─ hooks/
│  │  │  ├─ DiscordDuper.java
│  │  │  ├─ ...
│  │  │  ├─ Hooks374.java
│  │  │  ├─ Junk.java
│  │  ├─ json/
│  │  │  ├─ JSON.java
│  │  │  ├─ JSONArray.java
│  │  │  ├─ JSONExcetion.java
│  │  │  ├─ JSONObject.java
│  │  │  ├─ JSONStringer.java
│  │  │  ├─ JSONTokener.java
│  │  ├─ scripts/
│  │  │  ├─ Scripts.java
│  │  ├─ utils/
│  │  │  ├─ DuperUtils.java
│  │  │  ├─ Methods.java
│  │  ├─ DupeMod.java
```

## Description
This rat is very generic and I found it a few times already, I won't be posting any other ones of this type.

[2] The webhook is obtained from a pastebin url, but other rats of this type have it inside the code. The webhook from this one was still intact however I nuked it. The webhook is used to send the minecraft and discord information, and anonfiles links to the files that have been grabbed.

[3] The ransom mechanism is quite disappointing honestly. The ransom screen consists of a JFrame in full screen mode with the text "Your computer has been hacked and if you do not pay 30$ in BTC your files will be wiped." (it doesn't include a BTC wallet to which said 30$ should be transferred). The ransom screen can easily be exited by going into windows security screen and killing the process (or just clicking the little X in the task bar). The "encryption mechanism" consisty in overwriting the content of files with "Your files are crypted.". Very advanced "encryption".

Data grabbed: 
* Computer/OS: OS, IP (from AWS), login username, HWID
* Minecraft: token, UUID, ign, potential alt accounts
* Discord: token (Discord, Chrome, Opera), email phone number, has nitro, has billing information (Discord API)
* Files with interesting names (`accounts.txt`, `passwords.txt`, ...)
* Screenshot

Rating: 5/10