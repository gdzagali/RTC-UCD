#Integration between RTC  Rational Team Concept(RTC) and UrbanCode Deploy(UCD) 
Task 1 - Investigation on UCD and RTC
1. https://www.youtube.com/playlist?list=PLZGO0qYNSD4XWxKTk2zP7qhSdUokhMxA8
2. Start with the essentials videos (very important, provides in dept tutorials on UrbanCode Deploy features) 
3. Investigate the features in RTC for better understanding on what to work on. (RTC Projects)

Task 2 - helloWorld Tutorial in UCD
a.This tutorial will demonstrate all necessary features in UCD.
b.https://www.ibm.com/support/knowledgecenter/en/SS4GSP_6.2.0/com.ibm.udeploy.tutorial.doc/topics/quickstart_abstract.html
c. For installation of an agent on a windows device use Task 3.

Task 3 - Install Agent on PC
Agent Installation
	Installation of UrbanCode Deploy Agent on Windows Terminal Server

Use this link for reference: https://www.ibm.com/support/knowledgecenter/en/SS4GSP_6.2.4/com.ibm.udeploy.install.doc/topics/agentInstall.html

1) Begin by ensuring that you have an account specifically dedicated to the UCD Agent 
	eg: ucagent1
2) Also ensure that all system requirements are followed:
	* Java at a minimum of version 7
	* Ensure that you have administrator access
3) Download the agent zip file from the tools menu under the UrbanCode Deploy server menu
4) Extract the file to any easily accessible location; the location doesn't matter as the install is unrelated to it.
5) Navigate to the extracted folder, likely named "ibm-ucd-agent-install"
6) Run "install-agent.bat" as an administrator
7) Press enter to accept the default directory to install into
	* Input y to create the directory as it likely does not exist yet
8) Next, it reads the path for the location of the java installation; you can just press enter again
9) Follow the default, as we do not use agent relays; just press enter
10) Input the stem of the URL for the server that this agent is connecting to
	*i.e. if your server URL when you access the portal is https://abc123.qrs.ibm.com:8443, you would input abc123.qrs.ibm.com
11) Just accept the default agent communication port; press enter
12) No setup for a failover server connection, simply press enter
13) Press enter and follow the default for the ssl two-way authentication, which is no
14) Follow the default and do not disable end-to-end encryption for server/agent JMS communication
15) Follow the default for enabling the agent to verify server https certificate; press enter
16) Provide the full URL in this step to verify that the agent can successfully connect to the server
	*i.e. this time it would be, following from the previous example, https://abc123.qrs.ibm.com:8443
Ideally it will return that "Server URL is valid"

17) Enter a name suiting your application for the agent; press enter
18) It is unnecessary to do anything with the next step, as it can be done later in the server interface; simply press enter
19) After a short wait, you are faced with the following option: 
	"Do you want to install the Agent as a Windows service?"
Type y and press enter if you would like the agent to start on boot of the server; otherwise simply type n and press enter, and your installation is finished

20) If you opted in to installing it as a service, the next option will ask you to pick a name; the default is good if you only have one agent on the server;  press enter
21) Enter the user account you wish to set it up under, which is the user you created for the agent, along with the password
22) If you wish for it to run on startup, press y; otherwise press enter as no is the default

The primary installation process ends here

If you did not set it up as a service, then to start the agent you should follow the instructions on this page:
https://www.ibm.com/support/knowledgecenter/en/SS4GSP_6.1.1/com.ibm.udeploy.install.doc/topics/run_agent.html

Task 4 - Download RTC Plugin in UCD
a. After urbancode tutorials and rtc tutorials, explore te features in both tools
b. Download RTC work item plugin on UCD server. https://developer.ibm.com/urbancode/plugindoc/ibmucd/ibm-rational-team-concert-work-items/2-455564/steps/

Task 5 - Create a sample work item story in RTC
a. Within the specific project create a work item.
Task 6 - Use RTC plugin steps within UCD to deploy a story.
a. "Check work item status" 
b. "Change work item"
c. "Add comments" 
Use these steps to deploy and change the status and add comments in rtc.
Task 7 - Acessing multiple work items
a. Create a query within RTC to add specific work items that need to be accessed
b. Use rtcwi command line tool to access all work items that are in a "Ready For Production" state
c. https://w3-connections.ibm.com/wikis/home?lang=en-us#!/wiki/Wc81535b497b4_4f3a_8250_45c558f66d91/page/rtcwicli
Task 8 - Scripting 
a. Scripting is used to trigger RTC to UCD, it is necessary if you want to deploy multiple work items and add some more functionality that is not avaiable within UCD

Here are a few links that will provide some information on IBM UrbanCode Deploy and Rational Team Concert
1. https://www.youtube.com/playlist?list=PLZGO0qYNSD4XWxKTk2zP7qhSdUokhMxA8
2. https://developer.ibm.com/urbancode/plugindoc/ibmucd/ibm-rational-team-concert-work-items/2-455564/steps/
3. https://www.ibm.com/support/knowledgecenter/en/SS4GSP_6.2.4/com.ibm.udeploy.install.doc/topics/agentInstall.html
4. https://www.ibm.com/support/knowledgecenter/en/SS4GSP_6.1.1/com.ibm.udeploy.install.doc/topics/run_agent.html
5. https://jazz.net/                                                            





