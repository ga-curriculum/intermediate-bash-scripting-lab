<h1>
  <span class="headline">Intermediate Bash Scripting Lab</span>
  <span class="subhead">Creating Your First Menu</span>
</h1>

In this activity, you'll create a basic menu system that will serve as the foundation for your system information tool.

1. Open a terminal window.
2. Create a new file called `sysinfo.sh`:

```bash
nano sysinfo.sh
```

3. Add a shebang line at the top of your file to specify that this is a Bash script.
4. Add a title for your script using echo commands.
5. Create a simple menu that displays at least 4 options:

   - Option 1: Show System Info
   - Option 2: Show Disk Usage
   - Option 3: Show Current Users
   - Option 4: Exit

6. Use the read command to capture the user's choice.

7. Create a simple if/elif/else structure to handle the different menu options.

   - For each option, just add an echo statement as a placeholder (e.g., "You selected Option 1").
   - For the exit option, make sure the script actually exits.

8. Make your script executable with the chmod command.

9. Test your script to make sure the menu displays and responds to selections.

**Think About:**

- How can you make your menu visually clear and easy to read?
- What happens if the user enters an invalid option?
- How would you handle returning to the menu after completing an action?
