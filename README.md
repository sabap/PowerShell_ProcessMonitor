# PowerShell_ProcessMonitor
This script will monitor any running process in your task manager.</br>
If the process is closed, it will automatically try to re-launch the process.</br>
While the script is running, time-stamped host output will be written to the terminal.  Color-coded text will describe the status and process re-start events (if triggered).</br>
To stop the script, execute the Ctrl+C command in the terminal window.</br>
</br>
<b>-- SETUP</b></br>
The following variables need to set to suit your application.
```
$ProcessName = "HueSync" # Process name as it appears in Task manager
$ProcessExacutableLocation = "C:\Program Files\Hue Sync\HueSync.exe" # Path to the executable
$ProcessCheckInterval = "30" # Number in minutes to wait between process checks. Needs to be at least 1
```
<b>$ProcessName</b> is the name of the process as it appears in the task manager.</br>
<i>&nbsp;&nbsp;&nbsp;Note: This generally does NOT include the extension on the end of the name</i></br>
</br>
<b>$ProcessExacutableLocation</b> is the path of the executable.</br>
</br>
<b>$ProcessCheckInterval</b> is the amount of time <b>in minutes</b> that the script is to wait between checks.</br>
<i>&nbsp;&nbsp;&nbsp;Note: This needs to be set to a value no less than 1.</i></br>
<hr>
04/25/2022 - Revised the code and placed the function declarations at the top of the script, to ensure compatability with Task Manager.