<h1>
  <span class="headline">Intermediate Bash Scripting Lab</span>
  <span class="subhead">Rubric</span>
</h1>

## Lab requirements

The following requirements describe the functionality that should be present in the lab, and the points awarded out of 100 for each piece of functionality.

| Criteria                                                                                                                                                                      | Points |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ |
| The <code class="filepath">sysinfo.sh</code> script exists.                                                                                                                   | 2      |
| The <code class="filepath">sysinfo.sh</code> script is executable when cloned from GitHub.                                                                                    | 4      |
| The <code class="filepath">sysinfo.sh</code> script contains the correct shebang line.                                                                                        | 4      |
| The <code class="filepath">sysinfo.sh</code> script displays the title of the script when the script starts.                                                                  | 4      |
| When executed, the <code class="filepath">sysinfo.sh</code> script prints the title of the script.                                                                            | 4      |
| When executed, the <code class="filepath">sysinfo.sh</code> script displays the menu with 5 options to the user and prompts them to make a selection.                         | 8      |
| When executed with the `-h` or `--help` option, the <code class="filepath">sysinfo.sh</code> script displays a help message explaining what the script does and exits.        | 8      |
| When the first menu option is selected, the script should display the user's OS, hostname, kernel version, and how long the system has been running.                          | 10     |
| When the second menu option is selected, the script should display the available disk space on all mounted filesystems in a human readable format.                            | 10     |
| When the third menu option is selected, the script should display the users currently logged-in and the applications they have running.                                       | 10     |
| When the fourth menu option is selected, the script should display the 5 most CPU-intensive processes with at least the following columns: PID, user, CPU%, and command name. | 10     |
| When the fifth menu option is selected, the script should exit.                                                                                                               | 10     |
| When each menu option is selected, it should show a header and a timestamp for when the information was generated.                                                            | 8      |
| After selecting a menu option, the menu should be displayed again so the user can select another menu option.                                                                 | 8      |
| **Total possible points**                                                                                                                                                     | 100    |
