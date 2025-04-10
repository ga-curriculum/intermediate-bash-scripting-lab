<h1>
  <span class="headline">Intermediate Bash Scripting Lab</span>
  <span class="subhead">Instructor Guide</span>
</h1>

tktk Information to help instructors deliver this content should be added here. This file should not be removed, even if there is no content to place here immediately, and the following content should be retained regardless of how much content is in this file.

---

🏗️ **Under Construction**

We are constantly working to improve our resources for instructors and students.

**Have something to contribute to this Instructor Guide?** [Let us know](https://pages.git.generalassemb.ly/modular-curriculum-all-courses/universal-resources-internal/module-feedback.html).

## Solution for Microlesson 1: Basic Menu Script

``` bash
#!/bin/bash

# System Information Tool

echo "==============================="
echo "    SYSTEM INFORMATION TOOL    "
echo "==============================="
echo ""
echo "Menu Options:"
echo "1. Show System Info"
echo "2. Show Disk Usage"
echo "3. Show Current Users"
echo "4. Exit"
echo ""
echo "Enter your choice (1-4):"

read choice

if [ "$choice" = "1" ]; then
    echo "You selected Option 1: Show System Info"
elif [ "$choice" = "2" ]; then
    echo "You selected Option 2: Show Disk Usage"
elif [ "$choice" = "3" ]; then
    echo "You selected Option 3: Show Current Users"
elif [ "$choice" = "4" ]; then
    echo "Exiting..."
    exit 0
else
    echo "Invalid option. Please try again."
fi
```

## Solution for Microlesson 2: System Information Commands

``` bash
#!/bin/bash

# System Information Tool

# Function to display menu
show_menu() {
    clear
    echo "==============================="
    echo "    SYSTEM INFORMATION TOOL    "
    echo "==============================="
    echo ""
    echo "Menu Options:"
    echo "1. Show System Info"
    echo "2. Show Disk Usage"
    echo "3. Show Current Users"
    echo "4. Exit"
    echo ""
    echo "Enter your choice (1-4):"
}

# Main program loop
while true; do
    show_menu
    read choice
    
    case $choice in
        1)
            echo ""
            echo "System Information:"
            echo "-------------------"
            echo "OS:" $(cat /etc/os-release | grep PRETTY_NAME | cut -d'"' -f2)
            echo "Hostname:" $(hostname)
            echo "Kernel:" $(uname -r)
            echo "Uptime:" $(uptime -p)
            echo ""
            read -p "Press Enter to continue..."
            ;;
        2)
            echo ""
            echo "Disk Usage:"
            echo "-----------"
            df -h
            echo ""
            read -p "Press Enter to continue..."
            ;;
        3)
            echo ""
            echo "Current Users:"
            echo "--------------"
            who
            echo ""
            read -p "Press Enter to continue..."
            ;;
        4)
            echo "Exiting..."
            exit 0
            ;;
        *)
            echo "Invalid option. Please try again."
            sleep 2
            ;;
    esac
done
```

## Solution for Microlesson 3: Enhanced Script

``` bash
#!/bin/bash

# System Information Tool

# Check for help argument
if [ "$1" = "-h" ] || [ "$1" = "--help" ]; then
    echo "System Information Tool"
    echo "Usage: $0 [-h|--help]"
    echo ""
    echo "A simple menu-driven script to display system information"
    echo "Options:"
    echo "  -h, --help    Display this help message and exit"
    exit 0
fi

# Function to display menu
show_menu() {
    clear
    echo "==============================="
    echo "    SYSTEM INFORMATION TOOL    "
    echo "==============================="
    echo "  Generated: $(date '+%Y-%m-%d %H:%M:%S')"
    echo "==============================="
    echo ""
    echo "Menu Options:"
    echo "1. Show System Info"
    echo "2. Show Disk Usage"
    echo "3. Show Current Users"
    echo "4. Show Top Processes"
    echo "5. Exit"
    echo ""
    echo "Enter your choice (1-5):"
}

# Main program loop
while true; do
    show_menu
    read choice
    
    case $choice in
        1)
            echo ""
            echo "+-------------------+"
            echo "| System Information |"
            echo "+-------------------+"
            echo ""
            echo "OS:" $(cat /etc/os-release | grep PRETTY_NAME | cut -d'"' -f2)
            echo "Hostname:" $(hostname)
            echo "Kernel:" $(uname -r)
            echo "Uptime:" $(uptime -p)
            echo ""
            read -p "Press Enter to continue..."
            ;;
        2)
            echo ""
            echo "+-----------+"
            echo "| Disk Usage |"
            echo "+-----------+"
            echo ""
            df -h
            echo ""
            read -p "Press Enter to continue..."
            ;;
        3)
            echo ""
            echo "+--------------+"
            echo "| Current Users |"
            echo "+--------------+"
            echo ""
            who
            echo ""
            read -p "Press Enter to continue..."
            ;;
        4)
            echo ""
            echo "+----------------+"
            echo "| Top 5 Processes |"
            echo "+----------------+"
            echo ""
            ps aux --sort=-%cpu | head -6
            echo ""
            read -p "Press Enter to continue..."
            ;;
        5)
            echo "Exiting..."
            exit 0
            ;;
        *)
            echo "Invalid option. Please try again."
            sleep 2
            ;;
    esac
done
```

## Common Issues

1. Permission denied when running the script: Make sure to run `chmod +x sysinfo.sh` to make the script executable.

2. Syntax errors: Watch for missing quotes, incorrect if/then/else syntax, or case statement errors.

3. Command not found errors: Some commands might not be available on all systems. Alternatives:

   - If `cat /etc/os-release` doesn't work, try `lsb_release -a`
   - If `ps aux` doesn't work, try `top -bn1`

4. Loop not working: The main while loop is essential for returning to the menu. Make sure it's properly structured.

5. Script exits unexpectedly: Check for exit commands that might be triggered incorrectly.
