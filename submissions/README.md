## Submissions

There were five submissions to the DFRWS 2009 Forensics Challenge. This challenge was designed to be accessible to a wide audience, combined accessible forensic analysis tasks with some harder problems. We were pleased that the submissions this year came from not just researchers and developers, but also practitioners in the community.

Some aspects of the challenge could not be completed using existing tools and new techniques had to be developed. However, many of the questions could be answered without developing new approaches.

We thank all contestants for their efforts and their willingness to share their results and techniques with the community.

## The Winners

The winning submission for the DFRWS2009 Forensic Challenge was from **Wouter van Dongen and Alain van Hoof** at University of Amsterdam System & Network Engineering (PDF Report).

This submission provided a thorough analysis of the file system and network traffic, with some information extracted from the physical memory dump. The careful correlation of information from multiple data sources was a major strength of this submission. The results were presented in a very clear manner, and there is a particularly impressive timeline diagram.

## Other Contestants
**Byungkil Lee, Hongsuk Yang, and Hyeon Yu** provided concise analysis of available evidence to address the questions posed in this challenge, providing a rough timeline of events (PDF Report).

**Knut Kröger and Sven Wegner** at University of Applied Sciences Brandenburg used a variety of tools to extract information from the available evidence and address the questions posed in this challenge (PDF Report).

**Jewan Bang, JungHeum Park, Kwonyoup Kim, and Sangjin Lee** at Korea University Center for Information Security Technologies focused on the questions posed in this challenge, giving a concise overview of information obtained from the evidence (PDF Report).

**Erik Hjelmvik** concentrated on analysis of network traffic, presenting details relevant to the investigation (PDF Report).

## Judging Process
Submissions were evaluated based on the completeness and accuracy of the findings, and on effort developing new techniques and tools. The highest scores were awarded to the submissions that produced the most complete and accurate results, and that contributed significant new tools and techniques.

## Memory Analysis
None of the submissions focused on the analysis of memory in this challenge. The creators of this challenge at the University of New Orleans developed a memory analysis tool to extract details from memory dumps from PS3 running Ubuntu as shown here.

## Background of Scenario Execution
The following details about the challenge creation process are provided for future reference.

After meeting on the PS3 HOME network, nssal offers jhuisi an annual subscription to a live Mardi Gras picture and video library in exchange for a recipe collection based primarily on snake oil and other natural ingredients.

### Equipment Setup
- Jhuisi (J): PS3 (ps3.isi.jhu.edu, 128.220.249.83; goatboy:G04tB0y!) dual bootable (game/ubuntu); sniffer listening on SPAN port
- Nssal (N): PS3 (137.30.123.40; nssal:nssal, jhuisi:mac); PSP; sniffer listening on SPAN port; external USB drive

### Scenario Playbook

First nssal network capture contains PSP <-> PS3 traffic with PS3 in remote control mode. Images viewed, PS3 forced to web surf through remote control. Independent direct PS3 web surfing for Mardi Gras images. This was captured on 3/5/2009. Thumb drive contains shredded copies of Mardi Gras images. USB drive imaged on 3/6/2009.
- March 11, 2009 @ 11:30am – 1:30pm Eastern
- Initiated ongoing capture of network traffic
- Entered PS3 HOME and nssal invites jhuisi to participate
- N and J meet in HOME’s Central Plaza and chat about exchange of items
- Rough transcript of the communication in Home
- J: My friend "Atchoo" tells me you have an interesting collection
- N: I have not heard from "Atchoo" in a long time! Didn't know he was still into Mardi Gras.
- J: He is my neighbor. He had to cut back on MG contact because his family became suspicious but I am looking for some good videos and images.
- N: You have anything to barter?
- J: Um, I have a unique collection of family recipes guaranteed to improve your health and extend your life.
- N: I have been worried about getting older but I would need a sample.
- J: You can also bottle and sell this stuff. Make a bit of cash on the side.
- N: I will show you a sample if you show me a sample.
- J: Okay - the recipes are on my Linux side.
- J and N then decide to chat outside HOME on the PS3, exchange login credentials and samples, and arrange to reboot their PS3s into Linux.

Sample image exchanged between N and J using PS3 chat
- SSH credentials for N to login to J’s PS3 @ ps3.isi.jhu.edu with goatboy and password G04tB0y!
- N connects to J’s PS3 and copies recipes
- J compiles backdoor from C source on J’s PS3, uploads to N’s PS3, guesses nssal password, and installs backdoor for future access, deleting executable from N’s PS3
- Linux memory dump from N’s PS3 is taken
- File system image of Linux on each PS3 N’s file system dump contains MG images and videos
- J’s file system dump contains recipes and a folder showing customers and records of past sales of bottled snake oil
