<h1>
  <span class="headline">Intermediate Bash Scripting Lab</span>
  <span class="subhead">Create Your First Menu</span>
</h1>

**Learning objective**: By the end of this exercise, students will be able to create a menu-driven Bash script.

## Exercise

In this activity, you'll create a basic menu system that will serve as the foundation for your system information tool.

1. Create a new file called `sysinfo.sh`
2. Add a shebang line at the top of your file to specify that this is a Bash script.
3. Add a title for your script using echo commands.
4. Create a menu that displays at least 4 options:

   - Option 1: Show System Info
   - Option 2: Show Disk Usage
   - Option 3: Show Current Users
   - Option 4: Exit

5. Use the read command to capture the user's choice.

6. Create an `if`/`elif`/`else` structure to handle the different menu options.

   - For each option, just add an echo statement as a placeholder (for example, "You selected Option 1").
   - For the exit option, make sure the script actually exits.

7. Make your script executable with the `chmod` command.

8. Test your script to make sure the menu displays and responds to selections.

## Think about

- How can you make your menu visually clear and easy to read?
- What happens if the user enters an invalid option?
- How would you handle returning to the menu after completing an action?

## Common issues

1. Permission denied when running the script: Make sure to run `chmod +x sysinfo.sh` to make the script executable.

2. Syntax errors: Watch for missing quotes, incorrect if/then/else syntax, or case statement errors.

3. Command not found errors: Some commands might not be available on all systems. Alternatives:

   - If `cat /etc/os-release` doesn't work, try `lsb_release -a`
   - If `ps aux` doesn't work, try `top -bn1`

4. Loop not working: The main while loop is essential for returning to the menu. Make sure it's properly structured.

5. Script exits unexpectedly: Check for exit commands that might be triggered incorrectly.
