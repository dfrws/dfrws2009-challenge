# dfrws2009-challenge
The DFRWS 2009 Challenge focused on the development of tools and techniques for analyzing Playstation 3’s (PS3s). The Playstation 3 is a powerful, Cell processor-based system that can run both its native OS (which has significant DRM features that also thwart forensic investigation) and modern versions of Linux. This challenge focused on the Linux and network aspects of PS3s, and did not touch the DRM protected data. The challenge scenario required analysis of a physical memory dump, filesystem images, and network traces involving 2 PS3’s and a Playstation Portable (PSP).

## The Winners
The winning submission for the DFRWS2009 Forensic Challenge was from **Wouter van Dongen and Alain van Hoof** at University of Amsterdam System & Network Engineering (PDF Report).

This submission provided a thorough analysis of the file system and network traffic, with some information extracted from the physical memory dump. The careful correlation of information from multiple data sources was a major strength of this submission. The results were presented in a very clear manner, and there is a particularly impressive timeline diagram.

## The Scenario
In early 2009 it came to the attention of investigators that an individual with the nickname “nssal” was using a Sony Playstation3 (PS3) to make illicit images (specifically, certain images depicting Mardi Gras activities) available to other PS3 users.  Investigators determined that “nssal” was connecting from an IP address in New Orleans, and they began capturing network traffic with the goal of catching “nssal” red-handed. Based on their initial surveillance, it appeared that “nssal” had advanced knowledge of Linux and digital forensics. 

On March 11, 2009 investigators observed “nssal” communicating with another PS3 user and exchanging unknown data. With proper legal authorization, the investigators entered the suspect’s premises and found him in front of a PS3 that was running Linux. They interviewed the suspect and determined that he was a digital forensics researcher who was developing memory acquisition and analysis tools for Linux on the PS3. He denied having exchanged any information with other PS3 users.

Investigators captured physical memory of the Linux system on the PS3 using tools found on the system.  This physical memory dump is present in the file nssal-physicalmem.dd.bz2.  Investigators also acquired a forensic duplicate of the Linux partition on the PS3 (present in file nssal-linux-side-fs.dd-bz2) and the suspect’s thumbdrive (present in file nssal-thumb-fs.dd-bz2). Several network traces are also available.  The first network trace is based on early surveillance of the suspect; this network trace is named nssal-capture-1.pcap.bz2. A second trace, nssal-capture-2.pcap.bz2, contains communication between “nssal” and another machine located at Johns Hopkins University.  The network administrator in the lab at Johns Hopkins identified the machine as another PS3.  This administrator regularly monitors communication and was able to provide a third network trace, jhuisi-capture-1.pcap.bz2, which contains traffic transmitted between the “nssal” PS3 and the PS3 in the Johns Hopkins lab.   The system administrator also obtained a filesystem image of the PS3 at Johns Hopkins (present in jhuisi-linux-side-fs.dd-bz2) but was unable to obtain a physical memory dump.

You have been asked to assist investigators with the following questions:

- What relevant user activity can be reconstructed from the available forensic data and what does it show?
- Is there evidence of inappropriate or suspicious activity on the system?
- Is there evidence of collaboration with an outside party? If so, what can be determined about the identity of the outside party? How was any collaboration conducted?
- Is there evidence that illicit data (specifically, Mardi Gras images) was exchanged? If so, what can be determined about that data and the manner of transfer?
- What data (if any) was provided by the Johns Hopkins PS3?
- The suspect claims that he was not responsible for any transfer of data.  What evidence do you have to show that remote, unauthorized access to the system might have occurred, and does this evidence exonerate the suspect?

## Challenge Data
The data set for this challenge includes:

- 3 network traces in pcap format
- 1 PS3 physical memory dump
- 2 filesystem images

The files are available for download [from this directory](https://www.dropbox.com/sh/abbpdpo7vqfidyp/AAA3ouunoR5rXhAqv99p0BCya?dl=0).  Some files that are too big for Github are stored on Dropbox.

| File Name | MD5 |
| --- | --- |
| [jhuisi-capture-1.pcap.bz2](https://www.dropbox.com/s/7y34kulkazm20ko/jhuisi-capture-1.pcap.bz2?dl=0) | c1253c1e025876a7e72f513fd7f72181 | 
| [jhuisi-linux-side-fs.dd.bz2](https://www.dropbox.com/s/ao0h0ptdi1xfz31/jhuisi-linux-side-fs.dd.bz2?dl=0) | 18ead4e2e923f163bc95912d7362c874 |
| [nssal-capture-1.pcap.bz2](nssal-capture-1.pcap.bz2) | 594cd393f2dfa2ea11022e72a7ed9331 | 
| [nssal-capture-2.pcap.bz2](nssal-capture-2.pcap.bz2) | d895973c216aea504c7b90b6785fe158 | 
| [nssal-linux-side-fs.dd.bz2](https://www.dropbox.com/s/s7v9w0n4c1htge3/nssal-linux-side-fs.dd.bz2?dl=0) | cca65ecabcc911d44de083fb9a950910 | 
| [nssal-physicalmem.dd.bz2](https://www.dropbox.com/s/q4yv6omhaypigi9/nssal-physicalmem.dd.bz2?dl=0) | 218a2f9fe8ccc31df1551eda75b179ba | 
| [nssal-thumb-fs.dd.bz2](nssal-thumb-fs.dd.bz2) | d31e38fb66a562dd357db41d1687a50b | 

## Submission Requirements

Submissions should include a detailed analysis in report format that answers the questions posed above and discusses in detail how the answers were determined. The report should also include any other conclusions that appear germane to the case and must outline novel techniques employed in sufficient detail that the results can be reproduced. Reports must be submitted in PDF, ASCII or HTML format.

The submission should also include data that supports the findings and the source code for any analysis tools that were developed for the challenge. The source code can be released under any restrictions and licenses that you choose. The report and supporting files should be bundled into a single compressed archive. All submitted data, with the exception of compiled executables, will be published on the DFRWS website.

Submissions were due by July 12, 2009.

## Submission Method

Please submit your report together with any accompanying files in a single compressed archive (zip or gzip, for example) via anonymous FTP to a FTP server that no longer exists. Use "ftp" (without quotes) as a username and supply your e-mail address as the password. Upload your submission to the "upload/" directory. A confirmation e-mail of your upload will be sent to the address given as a password.

## Criteria

Submissions will be judged primarily for the completeness and accuracy of findings, as well as the soundness of the supporting analysis.

The goal of this and past challenges is to spur advances in the state of the art in research and tools. Therefore, we expect that you document your techniques as much as possible. Extra weight will be given for the creation of novel analysis tools that are applicable to broader forensic challenges.
