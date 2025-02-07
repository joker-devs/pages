# POSSIBLE FIX: Fatal error Early-exit trap

Firstly, hello people!

I recently came across a very annoying problem, which I did not find any solution to after a vast search on the internet. Of course, I entered some solutions. But they did not work.

Today I want to record what I did to solve this problem and I hope to help you who are going through the same situation that I also went through.

<img src="https://i.ibb.co/ynkRQc1Z/9defb65acd96f6eb72b732013be7e4925eee8082.png">

---

## First attempt

First, in a search I saw reports of people who solved this problem by simply deleting the `CitizenFX` folder.

- **Folder directory**: `%AppData%\CitizenFX`

So I did this, I deleted the `CitizenFX` folder.

---

However, it didn't work. So I continued my search and realized that there were no definitive solutions to this problem. I saw that it was a problem that had been going on for some time and that it didn't seem to receive the attention it deserved.

I've also seen other reports that formatting Windows can solve the problem. You could format while keeping your personal files if you wanted and that apparently solved the problem.

However, I didn't do that. Because I couldn't format my PC.

Then I remembered that my Windows had recently been updated to a recent version.

-> *It is worth mentioning that my system is Windows 11 Pro Insider Preview. It was updated to version 24H2 with Build 26120.3073.*

-> *Uninstalling and reinstalling FiveM apparently doesn't solve the problem (I haven't tried it).*

---

## Second attempt

So I used a good old application ([CCleaner](https://www.ccleaner.com/ccleaner/download?ref=jokerdevs_post&reftitle=early-exit%20trap%20on%20fivem)) to clean and repair Windows registries.

And finally I restarted the PC.

When I turned it on I located the file `CitizenFX.ini` in the directory `C:\Users\%userprofile%\AppData\Local\FiveM\FiveM.app` and added the following line:
- `PathCL2=D:\SteamLibrary\steamapps\common\Grand Theft Auto V`

<img src="https://i.ibb.co/Vc7L06mt/image.png">

- Which in the image above is located on line 7.

So basically what was done in this file was to take the value of the `IVPath` variable and create another variable called `PathCL2` with the same value.

-> *Remembering that the value of `IVPath` and `PathCL2` is the folder where the GTA V executable is located.*

Afterwards, I copied the GTA V executable and placed it in the FiveM plugins folder.

- **FiveM plugins folder**: `C:\Users\%userprofile%\AppData\Local\FiveM\FiveM.app\plugins`
- **GTA V executable**: Your GTA V folder with the executable GTAV.exe

---

#### And finally IT WORKED! Of course, it worked for me and I really hope it works for you :)

:tada:

*Please do not hesitate to leave your questions and suggestions here.*
