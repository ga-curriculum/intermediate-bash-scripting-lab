<h1>
  <span class="headline">Intermediate Bash Scripting Lab</span>
  <span class="subhead">Creating Your First Menu</span>
</h1>

In this activity, you'll Improve your script by adding command-line arguments, a help option, and better formatting for displayed information.

Let's make your script more user-friendly and powerful with some additional features.

1. Add a new menu option:

   - Option 4: Show Top Processes
   - Option 5: Exit (moved from 4 to 5)

2. Implement the "Show Top Processes" option to display:

   - The 5 most CPU-intensive processes
   - Format the output to show at least: PID, user, CPU%, and command name

3. Add a simple help feature:

   - If the script is called with `-h` or `--help` as a command line argument, display a brief help message explaining what the script does
   - Make sure the script exits after displaying help

4. Improve the formatting for all information displays:

   - Add clear headers for each section
   - Consider using simple ASCII borders or dividers between sections

5. Add a timestamp to show when the information was generated.
6. Test all your new features to make sure they work correctly.

**Think About:**

- How can you check for command-line arguments in a Bash script?
- What command will show you the most CPU-intensive processes?
- How can you limit the output to just show the top 5 processes?
