---
title: "Hardware & Network Troubleshooting"
date: 2026-01-19T12:00:00-06:00
draft: false
unsafe: true
#layout: single
---

## General Information
  - When hardware and networks work well, it’s a beautiful thing
  - But we know this is not always the case and, as an IT support professional, you will be depended upon to fix whatever goes wrong
  - Any device or network issue will fall within your domain
  - This is why hardware and network troubleshooting is the most emphasized area on the CompTIA A+ 1101 test, with 29% (nearly one-third) of the questions pertaining to it
  - It is important to note that *all* the questions about hardware and network troubleshooting will begin with a scenario
## Best Practice Methodology
  - Best practice methodology refers to the use of basic structured principles that should be followed when approaching a troubleshooting situation
  - While individuals may approach troubleshooting differently, certain **basic principles remain constant**: create a backup, prioritize tasks, and document the process
  - *Note:* Questions regarding this section of the exam will come in the form of scenarios
### Corporate Policies, Procedures, and Impacts 
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
## a
  - Every corporate enterprise has differing policies and procedures
  - Always consider corporate policies, procedures, and potential impacts before you begin troubleshooting
  - 1. Identify the Problem
  - The first step when troubleshooting an issue is to identify the problem
  - Technical problems with computer systems generally occur in one (or more) of **four areas**: hardware, the operating system, software, and the user
  - It is vital to accurately identify the problem **before taking action**
  - Gather information
  - To properly identify a problem, begin by gathering information **from the user and the computer system** in question
  - When gathering information from the user, ask questions to clarify the problem
  - Clarifying the issue will give you a starting point for further investigation
  - After questioning the user, examine the device to determine what is working and what is not
  - Check for common issues such as power problems or issues resolved upon reboot
  - Look into systems logs or application logs for information
  - Is the issue a hardware problem or a software problem?
  - Inquire about changes
  - Consider all the changes that could affect the user (e.g., network, computer, power issues, external connection, user account) and how those changes can be involved in the problem
  - As an example, let’s say the network team worked over the weekend performing an upgrade to the infrastructure (switch replacement) and neglected to plug all the cabling back into the switch (as simple as a cable falling behind the wiring channel and being missed)
  - The user might have been the one missed and now they cannot authenticate to the network, access their files, print to the network printer, and, therefore, cannot perform common functions
  - These things happen daily and other teams can be conducting changes without regard to the effect on employees
  - 2. Create a Theory of Probable Cause
  - Keep it **simple**
  - Always question the obvious and don’t assume something isn’t relevant
  - You might think it is common sense to be plugged into the network, but the user might not know this
  - Using your questioning ability, develop a theory (or two) regarding what the problem might be
  - When developing a theory, remember to **eliminate possible theories** as well if they do not fit the scenario
  - External or internal research
  - Utilize research resources, which can include internal and external resources
  - Check previous service **documentation** within the company, refer back to the **device manual**, and check for potential theories using **online** forums and search engines
  - The internet, when utilized properly, can be extremely helpful for troubleshooting problems
  - 3. Test the Theory/Determine the Cause
  - When you have your theory developed, you need to test it
  - On a time-sensitive issue, or if you know 100% that the theory is valid, you can implement it based upon corporate policies and/or procedures
  - In a perfect world, you would be able to replicate the issue within a testing (or laboratory) environment for verification
  - This isn’t always the case and you should be ready to test your theory at a moment’s notice
  - When testing a theory, **begin with the most obvious** and simple theories first, such as checking the power supply or ensuring cables are properly seated, before moving onto more complicated theories
  - If theory is confirmed, determine next steps
  - Only **test one possible solution at a time** and only **make one change at a time**
  - Sounds like a lengthy process? It is, but if you implement multiple changes in one process, how do you know which one worked and which one didn’t? Remember, keep it simple
  - If your theory is confirmed, then you can skip to the plan of action to implement your theory
  - If not, then it’s back to testing again
  - No worries, proper troubleshooting is an art
  - If theory is not confirmed, establish new theory or escalate
  - You’ve tested your theory and the problem still exists
  - Step back and take a look at your theory to see what other avenues are available and develop a working theory regarding the next possible solution
  - If you have exhausted all your potential theories, it may be time to escalate the problem
  - 4. Create a Plan of Action
  - Always remember: Your **company’s policies and procedures take precedence** and should be in the forefront prior to acting on any plan
  - The conclusion that you make might affect the whole company, but that might also be needed depending on the breath of the issue
  - Does correcting the issue require downtime for the company or just a single computer? Can that be scheduled around the users’ workday? Does it need to happen immediately? These are all questions that should be included in your plan of action
  - Vendor instructions
  - When creating a plan of action, remember to take into account vendor instructions
  - Vendors often provide **documented fixes** to identified issues, which should be considered
  - 5. Verify System Functionality
  - Once the issues have been resolved or appear to be resolved, verify full functionality of the problem system
  - Remember to verify **full system functionality** and do not focus strictly on the problem system
  - A fix to one system or component may cause issues with another system or component
  - 6. Document Findings, Actions, and Outcomes
  - Documentation! We can’t express how important it is for issues to be fully documented
  - **Everything that you have done** from the moment the user contacted you to the moment the user was back online, such as indications, findings, actions, outcomes, scenarios, etc., must be documented
  - Your **company should have a repository** to keep this information safe
  - It should also be possible to share among your peers in the event the same type of issue arises in the future
## Problems with Motherboards, RAM, CPU, and Power
  - There are many different situations that can arise when various types of hardware components start failing
  - You must be able to troubleshoot common problems through a scenario
### Common MOBO Symptoms
  - The **motherboard**, **RAM**, **CPU**, and **power supply** are the most critical components to a computer system
  - Problems with these components may have the same or similar symptoms
  - The list below covers general troubleshooting guidelines and causes of common symptoms
  - Power-on Self-Test (POST) Beeps   - The power-on self-test (POST) is a built-in diagnostic program in the BIOS/UEFI
  - When an error in the POST occurs, the computer performs a series of beeps, called the **beep code**
  - To identify the issue, listen to the beep code and refer to the **vendor documentation** to match the beep code with the corresponding error
  - The cause of these beeps could be problems with BIOS configuration or hardware
  - Proprietary Crash Screens   - Proprietary crash screens are operating system-specific error messages that occur when there is a potentially fatal error in the system
  - The most common proprietary crash screens are the **Windows blue screen of death (BSOD)** and the **macOS rotating pinwheel**
  - Common causes of these crash screens are **memory issues**, which may cause application crashes or error messages
  - Black Screen   - A black screen is indicative of **no video output**
  - Common causes of a black screen include problems with the video card, cabling, or the screen itself
  - Remember that many motherboards have the video card built in, which may indicate an issue with the motherboard itself
  - In this case, you can attempt to connect an external video card that, once connected, in most cases will disable the onboard video card
  - No Power 
  - Power outlet 






  - or **power supply** issues are usually the cause of this
  - When troubleshooting, begin by testing and replacing the easiest and most obvious components first before removing and replacing the power supply
  - Sluggish Performance   - Sluggish performance is one of the more difficult problems to troubleshoot
  - Common causes include low memory, low hard drive space, failing primary components, bad applications, too many applications, or malware
  - A good place to start when troubleshooting on a Windows OS is to view memory usage in Task Manager, which provides real-time statistics on the CPU, RAM, hard drive, and network connection
  - Overheating   - Problems with the fan, heat sink, dust accumulation, or something blocking the **air circulation** can all cause a device to overheat
  - Examine the device for impediments to the cooling mechanisms, such as excess dust or improper placement for optimal ventilation
  - **Compressed air** is one way to clean excess dust accumulation, but ensure that you are blowing away from the internal components of the computer rather than further into the device
  - Burning Smell   - A burning smell coming from a computer system is never a good thing
  - If you detect a burning smell, **shut down the device immediately** and examine it for potential culprits
  - Look for melted plastic and burn marks on circuit boards
  - Replace affected components and monitor the new component for failure
  - A component that fails too quickly may be an indicator of a power supply issue
  - Intermittent Shutdown   - An intermittent shutdown is typically a result of **components overheating and failing**
  - Intermittent shutdowns may also be caused by a bad hardware installation or improper motherboard connection
  - Application Crashes   - Application crashes are often an indicator of **memory**-related issues, such as failing memory or not enough memory available to run the application properly
  - Grinding Noise   - Grinding noises can only originate from **moving components** within the computer, such as the HDDs, fans, and optical drives
  - This fact eliminates all non-moving components within the device
  - Whirring sounds tend to originate from fans, while clicking or squealing sounds often come from the HDD
  - Optical drive noises are the simplest to diagnose
  - Capacitor Swelling   - Capacitors **store electricity** on the motherboard
  - When a capacitor fails, they tend to swell and produce a brownish-red residue that may seep
  - This phenomenon is referred to as a **distended capacitor** or **capacitor swelling**
  - Two options to resolve this issue include replacing the motherboard or replacing the capacitor, which requires specialized training
  - Inaccurate System Date/Time   - Inaccurate system date/time is most likely an indication of a **bad CMOS battery**
  - The CMOS battery is responsible for retaining the computer’s settings when it is powered off and is located on the motherboard
  - When the CMOS battery fails, the computer will be unable to retain its BIOS settings
## Problems with Storage Drives and RAID Displays
  - Storage devices include persistent storage such as storage drives and RAID storage
  - The most common causes of storage device problems are **bad adapters**, a **bad or failing drive**, or **improper connection**
  - You must be able to troubleshoot and diagnose problems with these systems based on a given scenario
### Common Storage Symptoms
  - While a bad adapter and an improper connection are relatively simple to detect and test, symptoms of a bad or failing drive are more complicated
  - Below is a list of common symptoms of a bad or failing drive or RAID
  - LED Status Indicators 
  - Light-emitting diode (LED) status indicators are typically visible on storage devices
  - A blinking light typically indicates a busy drive, while a light that does not come on at all or stays solid may be an indicator of a problem
  - However, you need to look at the **vendor-specific specifications** for indicator lights since the indicator lights on one product may not have the same meaning as lights on another product, such as a RAID display with a light that only comes on when a problem is detected in the array
  - Grinding Noises   - A grinding noise originating from a storage device is a significant **indicator of imminent failure** in a motor or spindle within the device
  - This grinding sound can also be heard as squealing sounds or nails on a chalkboard
  - It is important to **back up** the affected drive immediately and **replace** the drive
  - Clicking Sounds   - A rhythmic clicking or ticking sound is an indicator of a drive that is **in the process of failing**
  - Once again, back up and replace the drive immediately
  - Bootable Device Not Found   - Upon bootup, a storage device is first detected by the **BIOS/UEFI**, and then the OS
  - The “Bootable Device Not Found” error can be an indicator of a complete failure to boot or a failure of the OS to be found
  - Check **connection points and cables** between the motherboard and the drive if BIOS/UEFI autodetection fails
  - If a proper connection does not resolve the issue, it may be a bad drive
  - If the BIOS/UEFI is able to detect the drive but is unable to detect the OS, the issue may lie in the **master boot record (MBR)**
  - Data Loss/Corruption   - Data loss or corruption can be caused by a **failing or full drive**
  - To remedy the issue, first attempt to **remove unneeded files** or applications or **defragment** the drive
  - If this does not remedy the issue, you may attempt to **format** the drive and **reinstall** the OS
  - If the issue persists, the drive is most likely failing
  - RAID Failure   - Troubleshooting a RAID failure is similar to troubleshooting a single storage drive
  - First determine if the problem originates with a single drive or the system as a whole and proceed from there
  - Check the **indicator lights** on the RAID system for insight
  - Remember that the problem could originate from the type of RAID that is being employed
  - S.M.A.R.T Failure   - Self-monitoring, analysis, and reporting technology (S.M.A.R.T.) is software installed on drives that monitors hard drive reliability and performance
  - S.M.A.R.T
  - metrics, while in theory useful for diagnosing and predicting drive failure, tend to be overly complicated and difficult to parse
  - One **useful component** of S.M.A.R.T
  - is the **ability to create performance benchmarks** that may prove valuable in diagnosing potential drive failures
  - Extended Read/Write Times   - Extended read/write times, like data loss/corruption, can be indicators of a **failing or full drive**
  - Troubleshoot this issue as you would data loss/corruption
  - Input/Output Operations Per Second (IOPS) 
  - Input/output operations per second (IOPS) refers to how many reads and writes a storage device can perform in a second and is listed on storage devices, such as NAS and RAID systems
  - A **steadily declining IOPS** may be an **indicator of drive failure**
  - Missing Drives in OS   - Missing drives in the OS may be indications of a connection issue or an improperly set up storage device
  - Troubleshoot missing drives by checking connections, checking the **BIOS/UEFI** for the enabled drive, finding the drive in disk management or disk utility, making sure the drive is prepared and partitioned properly, updating drive drivers, and checking for bad sectors, which may cause the OS to show the drive as unreadable
## Problems with Video, Projectors, and Displays
  - Consider this situation:
  - A call comes in to the help desk: The Chief Financial Officer has started a meeting with the “C” level officers (including the Chief Executive Officer) in your company, and the projector won’t power on
  - This has happened before and will happen again
  - What’s the next step?
  - Below are some of the more common symptoms to look for
  - Watch out, those projector bulbs can be hot!
### Common Display Symptoms
  - When troubleshooting issues with video, projectors, and displays, there are some common symptoms that should be considered prior to escalation
  - Remember to **always check the basics** first
  - Incorrect Data Source   - An incorrect data source means that the input source for the viewing device and the input source selected for the computer are not the same
  - Viewing devices, such as monitors and projectors, can have multiple data ports on them, including **HDMI**, **DisplayPort**, or **VGA**
  - Physical Cabling Issues   - Physical cabling can cause a wide variety of issues, such as no image being produced or an image that appears and then disappears
  - **Visually inspect** cabling for imperfections and **switch out cables** with known working cables to diagnose or rule out cabling issues
  - Burned-Out Bulb   - Burned-out bulbs are specific to projectors
  - Projector bulbs have a limited life
  - Replace the bulb to solve this issue
  - Fuzzy Image   - Fuzzy images can be caused by different problems depending on the display device
  - With a **projector**, check the focus mechanism
  - With an **LCD screen**, fuzzy images can be caused by external interference, cabling issues, or resolution settings
  - Display Burn-In   - Burn-in is when an image or image outline is still visible on the display
  - This is caused when images remain on the screen and become permanent parts of the display.The only solution is to **replace the display**
  - Dead Pixels   - Dead pixels are the result of pixels that do not fire
  - This issue is typically related to the hardware or the monitor itself
  - **Replacement** of the display is usually necessary to correct it
  - Flashing Screen   - Often, a malfunctioning screen will either flash or flicker
  - A flickering screen is most likely caused by a **failing backlight**
  - Replace the backlight
  - With a flashing screen or a screen that turns on and off, the most likely cause is a **bad connection cable**
  - Incorrect Color Display   - With an LCD monitor, an incorrect color display is most likely caused by a **failing controller board**, which is responsible for color mapping
  - Another cause of an incorrect color display may be the **connection cable** or the **pins** on the display device itself
  - Audio Issues 
  - Many display devices today have built-in audio
  - To troubleshoot any audio issues, first check that the audio is **not muted** and the audio **volume is up**
  - On the computer itself, make sure that the appropriate audio output is selected
  - Dim Image   - Dim images can be caused by either an issue with the display device itself, generally caused by a **failing backlight**, or the computer being set to a **low brightness setting**
  - Intermittent Projector Shutdown   - Intermittent projector shutdowns are most commonly caused by **overheating**
  - Check to ensure proper airflow and unimpeded fans and filters
## Problems with Mobile Devices
  - Mobile devices are here to stay
  - For the purposes of the CompTIA A+ exam, the term refers to laptops and smaller devices
  - The only difference is they are smaller—much smaller—than other devices
  - Compact and portable, mobile devices can be much **tougher to troubleshoot** than conventional devices
  - Your company policy will dictate the level of repair you will be required to perform on these
  - If the device is personally owned, you might not be required to work on it
  - Keep in mind that the questions about this area will begin with a scenario
### Common Mobile Device Symptoms
  - Below are some fairly common symptoms and corresponding questions you should ask with regard to mobile devices
  - Ensure you have a **very clean workspace** and **sufficient lighting** prior to undertaking a major repair
  - Poor Battery Health 
  - Poor battery health can be evident by checking to see if a device works when physically plugged into a power source or if a fully charged battery drains very quickly with normal usage; within 30 minutes, for example
  - For a battery that will not hold a charge at all, replace the battery
  - With a laptop that holds a poor charge, you can attempt to perform a **battery calibration** before resorting to a battery replacement
  - With a smartphone, you can **drain** the battery completely and **recharge** before replacing the battery
  - Swollen Battery   - A swollen battery is a battery that is visibly distended
  - The image below shows how this might appear
  - **Turn off the device immediately** and **replace** the battery
  - Broken Screen   - A broken screen will have to be **replaced** if the break is severe enough to affect functionality
  - Improper Charging   - Most mobile devices have a charging indicator light or icon of some sort
  - While it is rare for the indicator to fail, it may happen
  - To check for this issue, plug the device in with a known working charger and see if the indicator is on
  - Improper charging is typically caused, however, by a connection issue, such as a **damaged cable** or the use of an **aftermarket cable** that is not fully compatible with the device
  - Poor/No Connectivity   - When troubleshooting poor/no connectivity, begin by checking to make sure the appropriate connectivity method is on, such as Bluetooth® or wireless
  - If the **connection method is enabled**, check the **signal strength** of the connection
  - Poor connectivity can be caused by too much distance between the sending and receiving devices
  - Liquid Damage   - Liquid damage can cause significant issues with a mobile device
  - If liquid damage is suspected, **turn off the device immediately** and let the device **air dry**
  - A laptop with significant liquid damage may be disassembled and cleaned using demineralized water and a lint-free cloth
  - Overheating   - Overheating can cause a device to shut down or not function properly
  - If overheating is suspected, **shut down the device immediately** and allow it to **cool**
  - To reduce the likelihood of overheating, ensure that the device is allowed proper **airflow** and keep all flow components clean and clear of dust and debris
  - Digitizer Issues   - To address digitizer issues on a laptop, you may go into the settings of the device and attempt to **recalibrate** the digitizer
  - If the digitizer cannot be calibrated or fixed, you may be able to work around the issue by **using a mouse and keyboard** for input
  - With a **mobile phone**, the only method for fixing the digitizer is to **fully power off** the device and **power it back on**
  - If this does not fix the issue, the screen will need to be replaced
  - Physically Damaged Ports   - With a physically damaged port, the only solution is to **replace** the port
  - Malware 
  - Malware is any malicious software designed to disrupt the usage of, cause damage to, or gain unauthorized access to an infected device
  - If malware is suspected, **antivirus and antimalware software** can identify, isolate, and remove most malware as well as defend against incoming malware
  - A **firewall** can also be used to help prevent infection
  - Cursor Drift/Touch Calibration   - Cursor drift is most commonly caused by a faulty pointing stick
  - You may **move** the input device around in an attempt to resolve the issue, or you can also attempt to **recalibrate** it
  - Recalibration can also be used to remedy faulty calibrations on touch screens
## Printer Issues
  - Given a scenario, you’ll need to be able to troubleshoot printers
  - Although a lot of information is being passed digitally, printers still have their uses in offices and IT professionals need to know their way around troubleshooting and maintaining them
  - **Inkjet** and **laser** are the most common printer types in offices
  - Other less common printer types are **impact** and **thermal**
  - Printers can be either directly connected to a computer for local use or shared over a network
### Common Printer Symptoms
  - Below are some fairly common symptoms, corresponding troubleshooting steps, and questions you should ask with regard to printers and printing issues
  - Lines Down the Printed Pages   - Lines on the printed page are usually caused by **ink residue**
  - Follow the printer’s **cleaning procedure**
  - This may include physically cleaning the internal parts of a printer, or a cleaning process that can be triggered by the printer’s software
  - Try printing a **test page**—are there streaks too? Sometimes streaks may be caused by **the scanning part** of a copier, and therefore they aren’t a printing problem
  - Garbled Print   - A garbled print may mean a software or connection issue
  - Are **correct drivers** installed? Is the printer connected firmly with a good **cable**? Is there **enough RAM** free on the printer?
  - Toner Not Fusing to Paper 
  - Toner not fusing (or sticking) to the paper will only happen on laser printers, and it is due to a fuser problem
  - Try **replacing the fusing roller or the fuser lamp**
  - Paper Jams   - There are many reasons for frequent or sporadic paper jams
  - The reasons can be categorized as related to the **paper** or to the **printer hardware**
  - Ensure that the paper size and weight used are as recommended by the printer’s manufacturer
  - Try using a new, dry pack of good-quality paper
  - Don’t load too much paper at once
  - Bend the stack of paper to separate sheets before loading
  - If the problem is not with the paper, then the printer hardware needs to be checked
  - Check to see if the printer has been **maintained** per the manufacturer’s recommendations
  - Some printers have a page counter and recommendations on replacing specific internal parts to prevent paper jams
  - If the jams are very frequent, check for **broken parts** in the feeding path
  - Faded Print   - Check **toner or ink levels** if the print is faded
  - Try replacing the cartridges with new ones of known good quality
  - Check **printing settings**
  - Are there any **ink-saving settings** enabled that may reduce the amount of ink or toner used?
  - Incorrect Paper Size   - If a printer is loaded with the incorrect paper size, it may jam or misprint
  - Check the printer’s **settings** to ensure the correct **paper size and orientation** is selected to match the desired outcome
  - Paper Not Feeding   - If the paper is not feeding, follow the same troubleshooting steps as for a *paper jam*
  - Multipage Misfeed   - Multiple page misfeeds can be caused by **separation pad** issues or **sticky/damp paper**
  - Multiple Prints Pending in Queue   - Are there specific errors on these pending jobs that can direct to the troubleshooting steps, such as issues with toner, paper, or access?
  - A backed-up queue may also be due to **spooler issues**
  - **Restart** the spooler service
  - Try **disabling the spooler** and printing directly to the printer with no queueing
  - Speckling on Printed Pages   - Speckling, small marks, or defects on printed pages are common with frequently used or older laser printers
  - This is often caused by spilled toner or a crack or chip in the EP drum
  - To fix, **clean or replace the roller**
  - Speckling with an inkjet printer is often caused by dust or residue in the printer
  - **Clean the printer** with compressed air
  - If the problem persists, it may be a leaking cartridge
  - **Replace the cartridge.**
  - Double/Echo Images on the Print   - Echo images may happen on laser printers due to a **broken cleaning blade** or **bad erasure lamps**
  - Try replacing the toner cartridge or the erasure lamps
  - Incorrect Color Settings   - Incorrect color production on an inkjet printer, referred to as the **chroma display**, could be caused by incorrect **cartridge placement**, ink bleeding from a **leaking cartridge**, or the incorrect **paper type**
  - If the paper is correct, try cleaning the print cartridges with the installed software and reprint a test page
  - Grinding Noise   - Impact printers can produce grinding noises with a damaged stepper motor
  - Replace the motor
  - Finishing Issues 
  - Many laser printers have finishing options, such as collation, stapling, and hole punching
  - Issues with the finisher are typically resolved with thorough cleaning
  - Staple jams 






  - Problems with the stapling process are typically caused by malfunctions in the finisher
  - Check to ensure there are staples in the mechanism and that it does not have any jams
  - Hole punch 






  - Problems with the hole punch process require the same process as the stapler
  - Ensure there are no blockages to the hole punch mechanism
  - Incorrect Page Orientation   - Incorrect page orientation is most likely caused by the settings within the printer or software
  - Ensure that the printer is set to print the correct orientation
## Wired and Wireless Network Problems
  - Given a scenario, you will need to troubleshoot common wired and wireless network problems
  - Networks are at the heart of today’s computing
  - A failure in network access has a good chance of preventing users from doing their work or information from being accessed
  - It needs to be addressed effectively
### Common Network Symptoms
  - Below are some fairly common symptoms and corresponding troubleshooting steps and questions you should ask with regard to networking and connectivity issues
  - Some basic **troubleshooting tactics remain constant:** check physical cables, connection, and speed or duplex mismatch first
  - Intermittent Wireless Connectivity   - Intermittent connectivity occurs when wireless connectivity appears and disappears
  - Intermittent connectivity is the most difficult to troubleshoot
  - When troubleshooting intermittent connectivity, try to narrow down the issue by addressing **latency**, **jitter**, **port flapping**, and **slow network speeds**
  - Slow Network Speeds   - Slow network speeds on a wired connection are mostly due to overload of the network
  - Solutions include adding a switch or creating **VLANs** with switches
  - A wireless connection with slow speed can also be caused by overload to the **wireless access point (WAP)** or wireless router
  - Distance from the WAP can also cause slow network speeds
  - Limited Connectivity   - Limited connectivity is a state in which a device is connected to the network but can’t reach outside of the local network
  - Even some local resources may be unreachable
  - For **Wi-Fi** networks, this is frequently caused by an **incorrect password**
  - Try reconfiguring the Wi-Fi connection with the correct password
  - For **wired ethernet networks**, the issue is usually due to the device not getting an **IP address** from the DHCP server, or it’s due to having a static IP address that doesn’t match the router network configuration
  - Does the device have the IP address configured manually? Is the default gateway configured correctly and does it match the IP address of the router on the network? For dynamic IP addresses, does the device get an IP address assigned? Is it in valid range on the same network as the router on the network?
  - Jitter   - Jitter is **variable latency**
  - Jitter can be caused by overloaded networks, both wired and wireless, or, with a wired device, a poor cable connection
  - Poor VoIP Quality   - Intermittent network connectivity or a slow network can cause poor Voice over Internet Protocol (VoIP) quality
  - Most managed systems running VoIP have a **priority setting** for different streams of networks
  - To increase VoIP quality, rank the VoIP connection as a high priority
  - Port Flapping   - Port flapping causes intermittent connectivity when a switch opens and closes a port very quickly
  - To troubleshoot port flapping, check cables, the connection, and the duplex
  - Another place to check for port flapping is the error logs on the switch for which layer the error occurs at
  - Also, reseat the **small form-factor pluggable (SFP)** connector
  - If this does not remedy the issue, switch to a known working SFP
  - High Latency 
  - High latency may cause the connection to appear intermittent
  - Troubleshoot high latency as you would intermittent connections
  - External Wireless Interference   - External interference is caused when an external device interferes with the wireless signal of a WAP or wireless router
  - External devices that may cause interference include radio signals, physical barriers, microwaves, motors, or fluorescent lights
  - If external interference is suspected, **change the positioning of the WAP or the external device** if possible