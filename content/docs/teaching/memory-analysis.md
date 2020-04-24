
# In-Memory Malware Analysis

This page contains some information and links for In-Memory Malware Analysis course.

In case of any questions, don't hesitate to contact me at
	**`vaclav.lorenc-at-gmail.com`** or [**`@valorcz`**](https://twitter.com/valorcz) on Twitter.

## Course Texts

 *  [In-Memory Analysis (text)](https://dior.ics.muni.cz/~valor/pv204/files/in-memory-analysis-text.pdf)
    --- A brief introduction to reverse engineering and memory forensics (English). 
 * [In-Memory Analysis (slides)](https://dior.ics.muni.cz/~valor/pv204/files/in-memory-analysis-slides.pdf)
   --- Handouts for this course (English). 

## Tools and Templates

 * [In-Memory Analysis (tools)](https://dior.ics.muni.cz/~valor/pv204/files/in-memory-analysis-2018.zip)
   --- A bootstrap folder structure with Volatility Framework and other tools.
   Unzip the file (if you know how, edit your `%PATH%` variable to contain the
   `\bin` folder). 

## Memory Images

Most of the memory images here can be found and downloaded from 
[Volatility Framework](https://code.google.com/p/volatility/wiki/SampleMemoryImages) page.
Download the file into your `\images` folder (it's in the unzipped folder
structure from the previous step).

| URL | Description  |
| --- | ------------ |
| [Infected WinXP](https://dior.ics.muni.cz/~valor/pv204/images/xp-infected.vmem) | A very basic Windows XP system, easy to analyze. |
| [Clean Win7, x64](https://dior.ics.muni.cz/~valor/pv204/images/win7_x64.vmem.bz2) | A clean image of Win7 Home memory, x64 platform (packed with bzip2). |
| [Zeus (older version)](https://dior.ics.muni.cz/~valor/pv204/images/zeus.vmem) | Windows XP infected with Zeus. |
| [Zeus (newer version)](https://dior.ics.muni.cz/~valor/pv204/images/zeus2x4.vmem) | Windows XP infected with never version of Zeus. |
| [Cridex (trojan, backdoor)](https://dior.ics.muni.cz/~valor/pv204/images/cridex.vmem) | A host infected with Cridex. |
| [SpyEye (keylogger)](https://dior.ics.muni.cz/~valor/pv204/images/spyeye.vmem) | A host infected with SpyEye. |
| [DarkComet (keylogger)](https://dior.ics.muni.cz/~valor/pv204/images/darkcomet-sample.zip) | A memory image of a host infected with DarkComet. Due to its size, this memory image si zipped. |
| [IE history analysis](https://dior.ics.muni.cz/~valor/pv204/images/exemplar17_1.vmem) | A memory image with a browser history to be analyzed. |
| [Bob! Detailed Forensics](https://dior.ics.muni.cz/~valor/pv204/images/bob.vmem) | Memory image to test your forensic skills (`foremost` can help you, be careful with dumped files). |

## Links

| URL | Description  |
| --- | ------------ |
| [Volatily Framework](http://www.volatilityfoundation.org/) | Powerful open source tool for memory analysis with command-line interface. Python powered. |
| [Rekall Memory Forensic Framework](http://www.rekall-forensic.com/) | Completely open collection of tools for the collection and extraction of digital artifacts from memory. Python powered. |
| [FireEye Redline](https://www.fireeye.com/services/freeware/redline.html) | Free (not open source) memory forensic tool, with nice GUI and decent forensic capabilities. For Windows only, requires latest .NET Framework. |
| [Reverse Engineering for Beginners](http://beginners.re/) | Excellent and free material for everyone who wants to dive into reverse engineering. Incredible stuff! |
| [SANS DFIR Memory Forensics Poster](http://digital-forensics.sans.org/media/Poster-2015-Memory-Forensics.pdf) | A poster with overview of memory forensics tools, workflows, commands and internals. |
| [Windows VMs](https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/mac/) | When you need a fully functional Windows VM with a browser (IE or Edge). |

## Homework

Your homework is as easy as forensic analysis. Ok, way easier :) 

{{<hint danger>}}
Analyse the image below, write a report and summarize your findings in such a way that I can possibly reproduce the process of your analysis. Use all the tools we used in the class, but only if you can work in a **safe environment** (VMWare, VirtualBox or Unix-based OS). If not, you don't have to dump any files from the memory image, especially if you don't trust your AV. Stay safe and keep your computer clean. If you want to perform more detailed analysis, you are cordially invited.
{{</hint>}}

You are expected to write a report with your analysis -- what volatility commands you used, what was the result, what did you find interesting and important. Preferebly, if you can put together a full story of what happened, that could bring you some extra points.

In case you need an inspiration in the report writing,
here's one: [a sample report](https://dior.ics.muni.cz/~valor/pv204/bob-vmem-analysis.pdf). Your report doesn't have to be that detailed, yet try to be as descriptive as possible.

 * [Your Homework](https://dior.ics.muni.cz/~valor/pv204/images/homework-2019.vmem.bz2) --- Memory image to test your skills (big warning here --be careful with dumped files!). 

Material prepared and created for **Laboratory of Applied Security and Cryptography**

