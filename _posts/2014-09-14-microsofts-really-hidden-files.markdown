---
author: Aniket
comments: true
date: 2014-09-14 17:33:59+00:00
layout: post
slug: microsofts-really-hidden-files
title: Microsoft's Really Hidden Files
wordpress_id: 62
categories:
- D.D.O.C.
tags:
- fuckmicrosoft.com
- Microsoft
- Microsoft Internet Explorer
- Microsoft Outlook
- Microsoft's Really Hidden Files
- why not believe on microsoft
---

A detailed post on Microsoft's dark secrets. Why should you not trust Microsoft ? Read on to find out.

<!-- more -->

DISCLAIMER:
I will not be liable for any damage or lost information, whether due to reader's error, or any other reason.

From http://fuckmicrosoft.com/ (you can visit this site from Archive.org)
Long and interesting read - makes you wonder what else they hide about you on your PC?
Read the disclaimer though - I nearly deleted everything on my computer by mistake.
(Try looking through User.Dat files as well using notepad as well - search for incriminating words using the find command -
Cant just delete these references though)
Microsoft's Really Hidden Files v2.0
by **_The Riddler_**
May 16, 2001
(v1.0 written on June 11, 2000)

SUMMARY:
There are folders on your computer that Microsoft has tried hard to keep secret. Within these folders you will find two
(major) things: Microsoft Internet Explorer has been logging all of the sites you have ever visited -- even after you've
cleared your cache, and Microsoft's Outlook and Outlook Express has been logging ALL of your e-mail correspondence --
even after you've erased them from your trashbin. (This also includes all incoming and outgoing e-mail attachments.) And
believe me, that's not even the half of it.
When I say that these files are hidden well, I really mean it. If you don't have any knowledge of DOS, then don't plan on
finding these files on your own. I say this because some of these files will only be found in DOS while some of these folders
can only be found in Windows Explorer. Additionally, there are some folders that will not be displayed by neither DOS nor
Explorer -- but can only be found using a workaround. Basically what I am saying is if you didn't know these files existed
then the chances of you running across them is slim to slimmer.
To give you an example of how sneaky this is, there are three hidden folders that may contain your name, address, phone,
all the sites you've visited, every single e-mail you've sent/received, every attachment you've ever sent/received, everything
you've searched for in a search engine, every filename you've downloaded, names of documents containing "sensitive"
information, copies of all your cookies, full readable e-mail from your hotmail account, your PGP keys, and more.
Funny that Microsoft would make no mention of this on microsoft.com.
FORWARD:
I know there are some people out there that are already aware of some of the things I mention. I also know that most people
are not. The purpose of this tutorial is teach people what is really going on with Microsoft's products and how to take
control of their privacy again.
Thanks for reading.
INDEX
1. DEFINITIONS AND ACRONYMS
2. WHY YOU SHOULD ERASE THESE FILES
3. HOW TO ERASE THE FILES ASAP (Recommended for the non-savvy.)
3.1) If You Own Microsoft Internet Explorer
3.2) Clearing Your Registry
3.3) If You Own Outlook Express
3.4) Slack files
3.5) Keeping Microsoft Internet Explorer (Not recommended at all.)
4. STEP-BY-STEP GUIDE THROUGH YOUR HIDDEN FILES (For the savvy.)
5. A LOOK AT OUTLOOK
6. HOW MICROSOFT DOES IT
7. +S MEANS [S]ECRET NOT [S]YSTEM 8. THE TRUTH ABOUT FIND FAST
8.1) Removing Find Fast
9. HOW HARD MICROSOFT TRIED TO KEEP PEOPLE FROM FINDING ABOUT IT
10. FINAL NOTE AND CONTACT INFORMATION
10.1) Recommended reading
11. SPECIAL THANKS
12. REFERENCES
Coming Very Soon:
mailbox.pst
pstores
Related Windows Tricks.
Reflection of why they use alphanumeric folders (9J3X7QZF4.)
Everything you didn't want to know about Find Fast.
The NSA-Key.
The [Microsoft Update] button.
Why the temp folders aren't intended to be temporary at all.



## What's in those .dbx files?







  1. DEFINITIONS AND ACRONYMS
Well, the best definition I have been able to come up with is the following:
I) A "really hidden" file/folder is one that cannot be seen in Windows Explorer after enabling it to view all files, cannot be
seen in MS-DOS after receiving a directory listing, and cannot be searched through using the "Find" utility.
a) There is at least one workaround to enabling Explorer to see them.
b) There is at least one workaround to enabling MS-DOS to see them.
c) There is at least one workaround to enabling the "Find" utility to search through them.
d) They are hidden intentionally.
II) Distinguishes "really hidden" file/folders from just plain +h[idden] ones, such as your "MSDOS.SYS" or "Sysbckup"
folder.
III) Distinguishes from certain "other" intended hidden files, such as a file with a name of "šŸëœx¥."
DOS = Disk Operating System
MSIE = Microsoft Internet Explorer
TIF = Temporary Internet Files (folder)
HD = Hard Drive





## OS = Operating System







  1. WHY SHOULD I ERASE THESE FILES?
1) Besides the glaring privacy risks.
2) Besides the fact that Microsoft is keeping these logs intentionally. (For reasons I can only imagine.)
3) These files can take up huge amounts of disk space. I've personally inspected a computer with almost 200 megs of this
stuff, so you can imagine how much this can slow your computer down. After following these instructions you will
probably notice a great improvement in performance.
--------------------------------------------------------------------------------3. HOW TO ERASE THE FILES ASAP
Step by step information on how to erase these files as soon as possible. This section is recommended for the non-savvy.
Further explanation can be found in Section 4.0. Please note that following these next steps will erase all your cache files,
all your cookie files, and all of your e-mail correspondence. If you use the offline content feature with MSIE, following





## these next steps will remove this as well.



3.1. IF YOU OWN A COPY OF MICROSOFT INTERNET EXPLORER
1) Shut your computer down, and turn it back on.
2) While your computer is booting keep pressing the [F8] key until you are given an option screen.
3) Choose "Command Prompt Only" (This will take you to true DOS mode.)
4) When your computer is done booting, you will have a C:\> followed by a blinking cursor. Type in this hitting enter after
each line.
CD\WINDOWS\TEMPOR~1\
DELTREE/Y CONTENT.IE5
(If that didn't work then type this:)
CD\WINDOWS\APPLIC~1\TEMPOR~1
DELTREE/Y CONTENT.IE5
(If that didn't work then type this:)
CD\WINDOWS\LOCALS~1\TEMPOR~1
DELTREE/Y CONTENT.IE5
(If this still does not work, and you are sure you are using MSIE5, then please e-mail me. Finding the location of these is a
mission, and I'd certainly like to know where else MSIE likes to hide its cache. I believe older versions of MSIE keep them
under "c:\windows\content\".)
5) This will take a ridiculous amount of time to process. The longer it takes, the more records Microsoft had stored about
you. When it gets done erasing that folder, then type this:
CD\
DELTREE/Y TEMP
DELTREE/Y WIN386.SWP
CD WINDOWS
DELTREE/Y COOKIES
DELTREE/Y TEMP
DELTRE/Y WIN386.SWP



## DELTREE/Y HISTORY



3.2. CLEARING YOUR REGISTRY
Reboot your computer and wait for Windows to load back up.
1) Drop to DOS ("Start" > "Program Files" > "MS-DOS Prompt") and type this at prompt: regedit
2) Your Registry Editor will pop up. Go to "Edit" > "Find"
3) Type in "TypedURLs" and then hit [Find Next]. You will be taken to all the places you've typed in URLs manually. 4)
Erase any URLs that you find. Do not erase the folders. (They will be called "01," "02," "03," etc...) Double click on them to
make sure they are URLs. I found mine here:
HKEY_USERS/Default/Software/Microsoft/Internet Explorer/TypedURLs/
HKEY_CURRENT_USER/Software/Microsoft/Internet Explorer/TypedURLs/
5) and while you're in here you might as well go here:
HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/Current
Version/Explorer/RemoteComputer/NameSpace/
{d6277990-4c6a-11cf-8d87-00aa0060f5b5}
6) Delete the {d6277990-4c6a-11cf-8d87-00aa0060f5b5} key. This will make the "Find: Files or Folders" utility perform



## searches much faster.



3.3. IF YOU HAVE OUTLOOK OR OUTLOOK EXPRESS INSTALLED
1) Install another e-mail program like Eudora, or Pegasus Mail. Make sure everything is setup correctly.
2) Backup any e-mail that you wish to save. (Print them out, or forward them to another box.)
3) Uninstall Outlook.
Warning, this conveniently does not erase any e-mail correspondence. To double check drop back to your DOS prompt and
type this:
dir *.mbx /s/p
dir *.mbx /s/p/ah
The files you are looking for are:
INBOX.MBX
OUTBOX.MBX
SENTIT~1.MBX
DELETE~1.MBX
DRAFTS.MBX
If these files come up they will be listed in either of these folders:
C:\Windows\Application Data\Microsoft\Outlook Express\Mail\
C:\Program Files\internet mail and news\%USER%\mail\
(If the .mbx files are located anywhere else then you probably don't want to delete them since they aren't from outlook. If
they are from outlook, however, then please e-mail me.)
Now type either of the following (depending on the location of your .mbx files). Remember, this will erase all your e-mail
correspondence so backup what you want to keep by printing them out or forwarding them to another box. Hopefully by
now you have already set up Eudora or Pegasus Mail.
CD\WINDOWS\APPLIC~1\MICROS~1\OUTLOO~1
DELTREE/Y MAIL
or CD\PROGRA~1\INTERN~1\%USER%
(replace "%user%" with the proper name.)



## DELTREE/Y MAIL



3.4. SLACK FILES
As you may already know, deleting files only deletes the references to them. They are in fact still sitting there on your HD
and can be easily recovered by anyone.
BCWipe is a nice program that will clear these files.
For you DOS buffs, there's a program called FileDust that got a 5 star rating on ZDNET, if that matters.
If you are using PGP then there is a "Freespace Wipe" option under PGPtools.
Norton Utilities has a nice filewiping utility.
You might want to check out Evidence Eliminator's 30 day trial. This is probably the best program as far as your privacy



## goes.



3.5. KEEPING MICROSOFT INTERNET EXPLORER
If you insist on using Microsoft Internet Explorer then I strongly recommend that you check out at least one of these
programs:
PurgeIE
Anonymizer Window Washer
Cache and Cookie Washer for IE
I have already tried and tested some other programs and you'd be surprised on how many of them DON'T pass the tests. For



## example, HistoryKiller 2001 claims it erases all the files, but don't count on it.







  1. STEP-BY-STEP GUIDE THROUGH YOUR HIDDEN FILES
This next section is for those of you who are more interested in learning the ins and outs of your computer. This section is
intended for the savvy user.
1) First, drop to DOS and type this at prompt (in all lower-case):
c:\windows\explorer /e,c:\windows\tempor~1\content.ie5\
You see all those alphanumeric names listed under "content.ie5?" (left-hand side) That's Microsoft's idea of making this
project as hard as possible. (Earlier versions of Internet Explorer simply called them "cache#.") These are your
alphanumeric folders that MSIE has created to keep your cookies and cache. Write these names down. (They should look
something like this: 6YQ2GSWF, QRMTKLWF, U7YHQKI4, 7YMZ516U, WQK6Z9UV, etc...) If you click on any of
these folders then nothing will be displayed. Not because there aren't any files here, but because Windows Explorer has lied
to you. If you want to view the contents of these alphanumeric folders you will have to do so in DOS. (Actually, there is a
workaround that Skywalker taught me, but it's a little bit harder to explain. I promise to cover this tip in the next version.)
2) Restart in MS-DOS mode. (You must restart because windows has "locked" down some of the files.)
3) Type this in at prompt: CD\WINDOWS\TEMPOR~1\CONTENT.IE5
CD %alphanumeric%
(replace the "%alphanumeric%" with the first name that you just wrote down.)
DIR/P
Note: Not only are you in a folder that DOS claims does not exist, but you are now looking at cache/cookies that Windows
Explorer claims do not exist.
These folders are directly responsible for the mysterious erosion of hard drive space you may have been noticing. Just a
couple interesting things you can find in here:
Pictures from all those porn sites you've visited.
Other internet cache files completely wasting your disk space.
If you use Hotmail (or any webmail service) you can probably see some of your old messages laying around here. To see
them for yourself, copy them into another directory and open them with your browser.
Retrieving your personal information from these cookies is a snap. For example if you've ever shopped at Amazon.com then
there's access to your name and e-mail. If you're a user on Hollywood.com then there's your city, state, and zip. MP3.com
keeps some goodies as well.
Feel free to check out all your alphanumeric folders, before going on to the next step.
5) Type this in:
CD\WINDOWS\TEMPOR~1\CONTENT.IE5
EDIT /75 INDEX.DAT (or "EDIT /16 index.dat")
You will be brought to a blue screen with a bunch of binary.
6) Press and hold the [Page Down] button until you start seeing lists of URLs. These are all the sites that you've ever visited
as well as a brief description of each. You'll notice it records everything you've searched for in a search engine in plain text,
in addition to the URL.
7) When you get done searching around you can go to "File" > "Exit."
8) Next you'll probably want to erase these files by typing this:
DELTREE/Y C:\WINDOWS\TEMPOR~1\
(replace "c:\windows\tempor~1\" with the location of your TIF folder if different.)
This will take a seriously long time to process. Then go check out your History.
9) Type this:
CD\WINDOWS\HISTORY\HISTORY.IE5
EDIT /75 INDEX.DAT (or "EDIT /16 index.dat")
You will be brought to a blue screen with more binary.
10) Press and hold the [Page Down] button until you start seeing lists of URLS again.
This is another recording of the sites you've visited. There also may be some other things in here. E-mail me if you find
anything interesting. I will share with you a snippet of what I found in my index.dat file. Client UrlCache
MMF Ver 5.2@#
@#3#yiâ
€
#àOÐ ê:+0
0 # �
'¶#
}*Á 5.t �
xt##
59
####
MS6C:\%
#
#\DAVE'S
HD.TXT#
\MSIE5.
C:\
Did you note the "C:\" and "\DAVE'S HD\MSIE5.TXT"?
"Dave" is the fictitious name that I use on my computer. "Dave's HD" is the name of my root folder on my LAN.
"MSIE5.TXT" is the name of a text file that I've been saving on my computer. It contains research from THIS project that
I've been working on. Mostly URLs and notes.
Do you see anything wrong with this picture? It took notice on a file on my HD, folks. MY HARD DRIVE. Not only that,
but it is saving it in a folder that cannot be seen by neither DOS nor Windows Explorer. Is it a coincidence that this file was
related to the research of this tutorial?
Obviously, my first suspicion was that Microsoft was scanning my HD and logging any "sensitive" information. In this
case, my msie5.txt probably had something in it that Microsoft didn't like. To read more about my findings read "THE
TRUTH ABOUT FIND FAST" in section 8.0.
1) If you're still with me, type this:
CD\WINDOWS\HISTORY
2) check out the mmXXX.dat files (and delete them), then type:
CD\WINDOWS\HISTORY\HISTORY.IE5
CD MSHIST~1
EDIT /75 INDEX.DAT (or "EDIT /16 index.dat")
More URLs from your internet history. Note there are probably other mshist~x folders here. 3) You can repeat these steps
for every occurrence of the mshistxxxxxxxx file.
4) By now you'll probably want to type in this:
CD WINDOWS
DELTREE/Y HISTORY
This is about it as far as I know. You may also want to take a look at your *.mbx files if you own Outlook. (dir *.mbx/s)





## More detailed information is covered in the next chapter.







  1. A LOOK AT OUTLOOK EXPRESS Would you think twice about what you said if you knew it was being recorded? E-mail correspondence leaves a permanent
record of everything you've said -- even after you've told Outlook to erase it. You are given a false sense of security sense
you've erased it twice, so surely it must be gone. The first time Outlook simply moves it to your "Deleted Items" folder. The
second time you erase it Outlook simply "pretends" it is gone. The truth is your messages are still being retained in a "really
hidden folder."
Furthermore, as if that wasn't disturbing enough, Outlook Express also keeps records of EVERY SINGLE file attachment in
an ENCRYPTED database. Can you believe this, folks?
For example, I attached this zip file and sent it to myself.
PK####'...Ž_} (tm)##P#AAA � À € Öø)-8³PK####+...Ž_8øM3#P �
#BBBÀ € ×ø%-8³PK####....Ž_ÄÖ. #P#CCC � � À € Øø!-8³PK# �
###2...Ž_²#å`#P#DDDÀ € Ùø#-8³PK#####'...Ž*} (tm)##P# � �





# AAAPK#####+...Ž*8øM3#P## 1BBBPK



##....Ž_ÄÖ. #P## bCCCPK#####2...Ž_²#å`#P# �



# "DDDPK####ÄÄ



And it recorded this in both my inbox.mbx file and outbox.mbx file:
UEsDBBQAAAAIACeFjip9jZkaEAAAAFAAAAADAAAAQUFBrcCBAAAAAIAg1vgpljizAFBLAwQUAAAA
CAArhY4qOPhNMxAAAABQAAAAAwAAAEJCQq3AgQAAAACAINf4JZY4swBQSwMEFAAAAAgALoWOKsTW
Lp0QAAAAUAAAAAMAAABDQ0OtwIEAAAAAgCDY+CGWOLMAUEsDBBQAAAAIADKFjiqyEuVgEAAAAFAA
AAADAAAARERErcCBAAAAAIAg2fgdljizAFBLAQIUABQAAAAIACeFjip9jZkaEAAAAFAAAAADAAAA
AAAAAAEAIAAAAAAAAABBQUFQSwECFAAUAAAACAArhY4qOPhNMxAAAABQAAAAAwAAAAAAAAABA
CAA
AAAxAAAAQkJCUEsBAhQAFAAAAAgALoWOKsTWLp0QAAAAUAAAAAMAAAAAAAAAAQAgAAAAYgAAA
END
Q1BLAQIUABQAAAAIADKFjiqyEuVgEAAAAFAAAAADAAAAAAAAAAEAIAAAAJMAAABERERQSwUGAAA
A
AAQABADEAAAAxAAAAAAA
Cheers to the first person to discover the algorithm.
Anyway, by now you are probably wishing you knew where these records were kept. Don't worry they're right here:
c:\program files\internet mail and news\%user%\mail*.mbx
(replace %user% with the name you use.)
Or, if you're lucky:
c:\windows\application data\microsoft\outlook\mail*.mbx
I found it odd that the first time I installed outlook, my e-mail data was saved automatically into "internet mail and news."
After I uninstalled and reinstalled, it changed its mind and put it into my "application data."
To erase these files simply type: (of course if you do this you will kill all of your e-mail messages, so backup what you want
to keep.)
Deltree c:\windows\intern~1\%user%\mail
or
Deltree c:\windows\applic~1\micros~1\outloo~1\mail--------------------------------------------------------------------------------
6. HOW MICROSOFT DOES IT
Ever wonder how Microsoft makes these folders invisible to both DOS and Windows Explorer? I was completely baffled by
how Microsoft was accomplishing this since even using a DOS 6.2 boot disk wouldn't work for me. I was honestly pretty
upset that the answer escaped me for so long, but after wondering around in the folders I finally figured it out.
The "desktop.ini" is a standard text file that can be added to any folder to customize certain aspects of the folder's behavior.
In these cases, Microsoft utilized the desktop.ini file to make these files invisible. Invisible to Windows Explorer, invisible
to DOS, and even invisible to the "Find" Utility (so you wouldn't be able to perform searches in these folders!)
Here are a couple examples:
Found in the c:\windows\temporary internet files\desktop.ini and the c:\windows\temporary internet
files\content.ie5\desktop.ini contains this text:
[.ShellClassInfo]
UICLSID={7BD29E00-76C1-11CF-9DD0-00A0C9034933}
Found in the c:\windows\history\desktop.ini and the c:\windows\history\history.ie5\desktop.ini contains this text:
[.ShellClassInfo]
UICLSID={7BD29E00-76C1-11CF-9DD0-00A0C9034933}
CLSID={FF393560-C2A7-11CF-BFF4-444553540000}
The UICLSID line cloaks the folder in both DOS and Explorer. The CLSID line disables the "FIND" utility from searching
through the folder. Additionally, it gives a folder the appearance of the "History" folder. (You'll know what I mean if you
fiddle with them enough.)
Erasing these desktop.ini files will give DOS and Windows Explorer proper viewing functionality once again. The problem
with erasing them is windows will reconstruct them on your next bootup. The workaround is to edit the desktop.ini files and
remove everything except for the [.ShellClassInfo]. This will trick windows into thinking they have still covered their
tracks, so they won't think to reconstruct them again.
By the way, if you erase these keys from your Registry it will not un-hide these folders. Still, I'm sure somebody could play



## with this enough to figure out a way to completely disable Microsoft from ever hiding files on your computer again.







  1. +S MEANS [S]ECRET NOT [S]YSTEM
Here are three easy true or false questions regarding DOS. Play along like you needed to know the answers to get your A+
certification.
1) True or false: Executing the dir/s command in root will display all the "normal" files and directories on your hard drive.
The correct answer is 'true.'
2) True or false: Executing the dir/s/ah command in root will display all the "hidden" files and directories on your hard
drive.
Again, the correct answer is 'true.'
3) True or false: Executing the dir/s/as command in root will display all the "system" files and directores on your hard drive.
The correct answer is 'you wish.' When DOS tries to get a list of the subdirectories of any +s[ystem] folder it hits a brick wall. Not only does this mean
Microsoft has taken extra precautions to keep people from finding these files, but it defeats the whole purpose of the "/s"
switch in the first place. Nice one.
In case you didn't understand, here's a small experiment that will show you what I mean.
Since the content.ie5 and history.ie5 subfolders are both located within a +s[ystem] folder, we will run the experinment with
them. The proper command to locate them should be this:
CD\
DIR *.IE5 /s/as
The problem is that you will receive a "No files found" error message.
This proves that all subfolders/files that are located within a system folder will not be listed. But believe me, it's there.
Now, the really interesting thing is that you (luckily) can get around this brick wall. That is, once you are in the system
folder, then the brick wall no longer has an effect on the directory listings. For example:
CD\WINDOWS\TEMPOR~1
DIR *.IE5 /as
1 folder(s) found.
Oh good, now you can see them. (But only after you knew the exact location.) In other words, if you didn't know the folders





## existed then finding them would be almost impossible.







  1. THE TRUTH ABOUT FIND FAST
Have you ever wondered what that "Find Fast" program was under your control panel? I've spent about an hour on
microsoft.com reading help files and I STILL have no clue of what it's good for. Here's the most informative snippet I found
on microsoft.com.
"The Find Fast Indexer is a utility that builds indexes to speed finding documents using the Open and Open Office
Documents commands in Microsoft Office programs, including Microsoft Outlook."
So what does that mean? Well, if you read it carefully you'll see that Microsoft never mentions that it will speed up your
searches. In fact it has nothing to do with the "Find: Files or Programs" utility. I think what Microsoft is really trying to say
is that when you go to "File" > "Open" under Microsoft Word, then your list of documents will be displayed quicker.
If that is what they are saying then it is a lie. I hope you don't think I am taking Microsoft's quote out of context here. I'm
only trying to show you all the methods that Microsoft went through to make it appear that the Find Fast utility speeds up
searches.
For example if you go to "Edit" (under Microsoft Word), you will notice there is a "Fast Find" icon next to it. (Binoculars
icon.) This is usally a clear indication that it is related to the Find Fast program. However, if you re-read that quote, it
doesn't mention anything about finding words "within" a document, but only the document itself. Here are some more
quotes from Microsoft:
"The Find Fast Indexer tool tracks the location on the hard disk of all Microsoft Word for Windows documents by default.
When one of these files is moved, the Find Faster Indexer tool updates its index."
"Indexes are used to make file searches faster in Office programs." "The Find Fast Indexer is installed on your computer when you install Microsoft Office 97. Find Fast builds an index to
speed up finding documents from the Open dialog box in Microsoft Office programs."
I wasn't able to find one single shred of evidence that it helped you "search" faster. Yet, Microsoft insisted on calling the
program "Find Fast." THEN they decided to add the Find Fast icon next to the [Search Document], as if Find Fast had
anything to do with searching the document.
So now do you think you know the truth?
What would you say if I told you that Find Fast was scanning and indexing every single file on your hard drive? Did you
know that in Office 95, the Find Fast Indexer had an "exclusion" list comprised of .exe, .swp, .dll and other extensions, but
the feature was eliminated? If you were a programmer, would you program Find Fast to index every single file, or just the
ones with Office extensions?
Here are some other interesting facts:
Find Fast automatically loads on every boot (because it added to your Startup folder.)
If you have ever had problems with scandisk (restarting due to "disk writes."), it is because Find Fast was indexing your
hard drive in the background.
Now here is a good example of the lengths Microsoft has gone through to keep people from finding out Find Fast indexes
their hard drives. (Always good to have an alibi.) And I quote:
"When you specify the type of documents to index in the Create Index dialog box, Find Fast includes the document types
that are listed in the following table.
Doc Type File Name Extension
Microsoft Office files All the Microsoft Excel, Microsoft Web documents PowerPoint, Microsoft Project, and Microsoft
Word document types listed in this table. Microsoft Binder (.odb, .obt) and Microsoft Access (.mdb) files. Note that in .mdb
files, only document properties are indexed.
Microsoft Excel workbooks .xl* files
Microsoft PowerPoint files .ppt (presentation), .pot (template), .pps (auto-running presentation) files
Microsoft Project files .mpp, .mpw, .mpt, .mpx, .mpd files
Microsoft Word documents .doc (document), .dot (template), .ht* (Hypertext Markup Language document), .txt (text
file), .rtf (Rich Text Format) files
All files _._ files
Did you get that last part? If you were a wealthy man and you decided to buy every single car in the car lot, would you
a) Say, "I'll take the red ones, the blue ones, the silver ones, the white ones, the champagne ones, and all of them," or
b) "I'll take them all sir."
As you can see, they don't want people to realize that Find Fast is keeping an index of your entire hard drive. They walk
around the car lot saying "I'll take the red ones, the blue ones, the silver ones,..."
I personally witnessed the Find Fast Indexer "creep" its way back into my Startup folder after I removed it. There's no
possible way I could have done this on purpose. In fact the only way I could have done it is if I created a shortcut to Find
Fast and then moved the shortcut into Startup manually. There's no option on the Find Fast program to add it to Startup.
Am I making this up? Did I imagine it? Well, even if I am, then that doesn't change the overwhelming amount of
inconsistencies. For example:
1) Drop to DOS
2) CD\
3) DIR FF_._ /AH (This will bring up a listing of ffast-related files.)
4) edit /75 %ff% (insert %ff% with any of the names that were listed.) Notice the incredible amount of disk accesses to your "really hidden" "Temporary Internet Files" folder? What is the





## obsession that Find Fast has with these hidden folders, anyway?



8.1. REMOVING THE FIND FAST PROGRAM
1) Reboot your computer in MS-DOS Mode.
2) Delete the FindFast.CPL file from c:\windows\system\
3) Delete the shortcut under c:\windows\start menu\programs\startup\
4) Delete the FindFast.EXE file from c:\progra~1\micros~1\office\
Other related files that are safe to erase:
5) FFNT.exe, FFSetup.dll, FFService.dll, FFast_bb.dll, "c:\>ff_._"



## Notice you will loose no functionality after erasing these files? Actually, you will gain functionality.







  1. HOW HARD MICROSOFT TRIED TO KEEP PEOPLE FROM FINDING ABOUT IT
In case the desktop.ini file wasn't enough proof. ("Whoops, we didn't know the desktop.ini file would turn folders
invisible?") And in case you thought disabling DOS's "/s" switch for system folders was just a "bug." And in case you
thought Microsoft disabled the Find utility from searching through the folders just to save you time (uh huh) -- then feel free





## to check out this thread on the Hackers.com BBS.







  1. FINAL NOTE AND CONTACT INFO
This tutorial is being updated ALL THE TIME. If you have any input then please e-mail me so I can compile it into future
versions. You may have noticed many requests to contact me throughout this tutorial. This is because I am very eager to
find out everything there is to know about this. But just so I am not swamped with old updates, please make sure you are
reading the most current version.
My e-mail address is located below. Although it may not be done in a timely fasion, I always reply to all of my e-mail. By
the way, I deleted my PGP due to security reasons. So if you want to contact me privately, then I'm sure we can work out
something else.
Thanks for reading, -- The Riddler
e-mail: mailto:ther1ddler@fuckmicrosoft.com?Subject=Feedback from fuckMicrosoft.com Article





## hangout: http://www.hackers.com/bulletin/



10.1. RECOMMENDED READING
And if you aren't already paranoid enough here's some sites/articles that I definitely reccomend:
http://www.theregister.co.uk/content/4/18002.html
http://www.findarticles.com/m0CGN/3741/55695355/p1/article.jhtml
http://www.mobtown.org/news/archive/msg00492.html
http://194.159.40.109/05069801.htmhttp://www.yarbles.demon.co.uk/mssniff.html
http://www.macintouch.com/o98security.html
http://www.theregister.co.uk/content/archive/3079.html
http://www.fsm.nl/ward/
http://slashdot.org/
http://www.peacefire.org/
http://stopcarnivore.org/
http://nomorefakenews.com/



## http://grc.com/steve.htm#project-x







  1. SPECIAL THANKS
Thank you Skywalker, for being in the right place at the right time. You were the only one who seemed interested in helping
me further my research.
Thank you to everybody who has e-mailed me specifically just to thank me. The kind words mean a lot to me and played a
big motivator to get this text finished.
And thank you to Hackers.com, for developing a fantatsic site with a great community feel, without which, this tutorial





## would never have existed.







  1. REFERENCES
http://support.microsoft.com/support/kb/articles/Q137/1/13.asp
http://support.microsoft.com/support/kb/articles/Q136/3/86.asp
http://support.microsoft.com/support/kb/articles/Q169/5/31.ASP
http://support.microsoft.com/support/kb/articles/Q141/0/12.asp
http://support.microsoft.com/support/kb/articles/Q205/2/89.ASP
http://support.microsoft.com/support/kb/articles/Q166/3/02.ASP
http://www.insecure.org/sploits/Internet.explorer.web.usage.logs.html
http://www.parascope.com/cgi-bin/psforum.pl/topic=matrix&disc=514&mmark=all
http://www.hackers.com/bulletin/
http://slashdot.org/articles/00/05/11/173257.shtml
http://peacefire.org/


