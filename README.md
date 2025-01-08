# Install software in a Linux distribution
<h2>Activity Overview</h2>

In this lab activity, you’ll use the Advanced Package Tool (APT) and sudo to install and uninstall applications in a Linux Bash shell.

<h2>Scenario</h2>

Your role as a security analyst requires that you have the Suricata and tcpdump network security applications installed on your system.

In this scenario, you have to install, uninstall, and reinstall these applications on your Linux Bash shell. You also need to confirm that you’ve installed them correctly.


<h2>Task 1. Ensure that APT is installed</h2>

First, you’ll check that the APT application is installed so that you can use it to manage applications. The simplest way to do this is to run the apt command in the Bash shell and check the response.

The Bash shell is the command-line interpreter currently open on the left side of the screen. You’ll use the Bash shell by typing commands after the prompt. The prompt is represented by a dollar sign ($) followed by the input cursor.

- Confirm that the APT package manager is installed in your Linux environment. To do this, type apt after the command-line prompt and press ENTER.

When installed, apt displays basic usage information when you run it. This includes the version information and a description of the tool:

![image](https://github.com/user-attachments/assets/c39112d8-e2dc-4533-8574-17427be2d32b)
APT is already installed by default in the Linux Bash shell in this lab because this is a Debian-based system. APT is also the recommended package manager for Debian. If you’re using another distribution, a different package manager, such as YUM, may be available instead.

<h2>Task 2. Install and uninstall the Suricata application</h2>

In this task, you must install Suricata, a network analysis tool used for intrusion detection, and verify that it installed correctly. Then, you’ll uninstall the application.

1.Use the APT package manager to install the Suricata application.

Type sudo apt install suricata after the command-line prompt and press ENTER.
When you install an application with APT, the output displays details of all the software to be installed. This may include additional applications that depend on the new software. These additional applications are called the dependencies of the software to be installed.
![image](https://github.com/user-attachments/assets/bb840bad-ec39-46e1-afd5-b95ba773f8ca)

When prompted to continue, press the ENTER key to respond with the default response. (In this case, the default response is Yes.)

2.Verify that Suricata is installed by running the newly installed application.
Type suricata after the command-line prompt and press ENTER.

When Suricata is installed, version and usage information is listed:
![image](https://github.com/user-attachments/assets/180af3e8-7d7a-4c15-b91f-8a809af6108c)

3.Use the APT package manager to uninstall Suricata.

Type sudo apt remove suricata after the command-line prompt and press ENTER. Press ENTER (Yes) when prompted to continue.

When prompted to continue, press the ENTER key to respond with the default response. (In this case, the default response is Yes.)

![image](https://github.com/user-attachments/assets/1a822b89-a5dd-47ff-a197-a170cdbd8fc8)

4.Verify that Suricata has been uninstalled by running the application command again.

Type suricata after the command-line prompt and press ENTER.

If you have uninstalled Suricata, the output is an error message:

![image](https://github.com/user-attachments/assets/22fb10cd-f2f9-4632-84a6-f4890993820c)

<h2>Task 3. Install the tcpdump application</h2>
In this task, you must install the tcpdump application. This is a command-line tool that can be used to capture network traffic in a Linux Bash shell.

 - Use the APT package manager to install tcpdump.

Type sudo apt install tcpdump after the command-line prompt and press ENTER.
![image](https://github.com/user-attachments/assets/4919ba91-e440-422d-aaa5-c585937f3051)

<h2>Task 4. List the installed applications</h2>
Next, you need to confirm that you’ve installed the required applications. It's important to be able to validate that the correct applications are installed. Often you may want to check that the correct versions are installed as well.

1. Use the APT package manager to list all installed applications.

Type apt list --installed after the command-line prompt and press ENTER.
![image](https://github.com/user-attachments/assets/4840f122-07a6-4a8b-883a-2e47ca648be5)

This produces a long list of applications because Linux has a lot of software installed by default.

2.Search through the list to find the tcpdump application you installed.
![image](https://github.com/user-attachments/assets/c9f19f56-9b1d-4e77-b32f-ab0381886f60)

The Suricata application is not listed because you installed and then uninstalled that application:

<h2>Task 5. Reinstall the Suricata application</h2>

In this task, you must reinstall the Suricata application and verify that it has installed correctly.

1. Run the command to install the Suricata application.

Type sudo apt install suricata after the command-line prompt and press ENTER.
![image](https://github.com/user-attachments/assets/5516fcbd-52f2-4d58-9ba3-75e91f9639fb)

When prompted to continue, press the ENTER key to respond with the default response. (In this case, the default response is Yes.)

2. Use the APT package manager to list the installed applications.
Type apt list --installed after the command-line prompt and press ENTER.
![image](https://github.com/user-attachments/assets/84221b87-0f18-4b4c-87dc-6d8999f1c115)

3. Search through the list to confirm that the Suricata application has been installed.

   ![image](https://github.com/user-attachments/assets/b51f5e7c-1da7-4080-a6af-2c6be207e90b)
