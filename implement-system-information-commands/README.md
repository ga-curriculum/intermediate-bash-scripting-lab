<h1>
  <span class="headline">Intermediate Bash Scripting Lab</span>
  <span class="subhead">Implement System Information Commands</span>
</h1>

**Learning objective**: By the end of this exercise, students will be able to implement system information commands in a Bash script.

## Exercise

In this activity, you'll enhance your menu script by replacing the placeholder text with actual system commands that display useful information.

Now that you have a working menu, let's replace the placeholder text with real commands that display system information.

1. For option 1 (**Show System Info**), modify your script to display:

   - The operating system name and version
   - The hostname
   - The kernel version
   - How long the system has been running (uptime)

   You'll need to do some research to find the appropriate commands for this information.

2. For option 2 (**Show Disk Usage**), make your script display the available disk space on all mounted filesystems. Ensure that this is in a human-readable format. You'll need to research how to display disk usage and how to format it correctly.

3. For option 3 (**Show Current Users**), modify your script to:

   - Show all users currently logged into the system.
   - Show what apps each user has running.

   You'll need to research the appropriate command to use to show the currently logged-in users and the applications they have running.

4. Modify your script to return to the menu after completing each action, instead of exiting. Think about how to implement this using a loop.

Test each option to make sure it displays the correct information.
