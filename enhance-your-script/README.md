<h1>
  <span class="headline">Intermediate Bash Scripting Lab</span>
  <span class="subhead">Enhance Your Script</span>
</h1>

**Learning objective**: By the end of this exercise, students will be able to enhance a Bash script with command-line arguments, help options, and improved formatting.

## Exercise

In this activity, you'll improve your script by adding command-line arguments, a help option, and better formatting for displayed information.

Let's make your script more user-friendly and powerful with some additional features.

1. Add a new menu option:

   The new menu should look like the following - notice that a new option (`Show Top Processes`) has been added, and the order of the options has changed:

   ```plaintext
   Welcome, select one of the following options using the number keys:
   1: Show System Info
   2: Show Disk Usage
   3: Show Current Users
   4: Show Top Processes
   5: Exit
   ```

2. Implement the "Show Top Processes" option to display:

   - The 5 most CPU-intensive processes.
   - Format the output to show at least: PID, user, CPU%, and command name, similar to the following:

     ```plaintext
     +------+-------+--------+-------------+
     | PID  | User  | CPU%   | Command     |
     +------+-------+--------+-------------+
     | 1234 | root  | 75.2%  | firefox     |
     | 5678 | userA | 50.1%  | chrome      |
     | 9101 | userA | 33.6%  | python      |
     | 1213 | userA | 25.9%  | java        |
     | 1415 | userA | 15.3%  | node        |
     +------+-------+--------+-------------+
     ```

3. Add a simple help feature:

   - If the script is called with `-h` or `--help` as a command line argument (as shown below), display a brief help message explaining what the script does.

     ```bash
     ./sysinfo.sh -h
     ```

   - Make sure the script exits after displaying help.

4. Improve the formatting for all information displays:

   - Add clear headers for each section.
   - Consider using simple ASCII borders or dividers between sections.

5. Add a timestamp to show when the information was generated.
6. Test all your new features to make sure they work correctly.

## Think about

- How can you check for command-line arguments in a Bash script?
- What command will show you the most CPU-intensive processes?
- How can you limit the output to just show the top 5 processes?
