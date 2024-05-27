# Hard-Disk-Sentinel

![2024-05-27_13-51](https://github.com/sofijacom/Hard-Disk-Sentinel/assets/107557749/9e1fc425-7c91-442e-a113-5dcefef6215a)


Usage of Hard Disk Sentinel Linux version
After downloading the file below, please follow these steps to use it:
double click to open and decompress it to any folder
open a terminal window and navigate to the folder
change file permissions to make it executable by using chmod 755 HDSentinel
launch it by entering sudo ./HDSentinel [options]
sudo is not required if you logged in as "root".

##

Command line switches
The switches are NOT case sensitive. Upper and lower case can be used to specify them.

- -h - displays help and usage information
- -r [report file] - automatically save report to filename (default: report.txt)
- -html - use with -r to save HTML format report (-html -r report.html)
- -mht - use with -r to save MHT format report (-mht -r report.mht)
- -autosd - detect industrial SD card type and save flag file (see How to: monitor (micro) SD card health and status for more details)
- -dev /dev/sdX - detect and report only the specified device without accessing others
- -devs d1,d2 - detect (comma separated) devices in addition to default ones eg. /dev/sda,/dev/sdb,/dev/sdc
- -onlydevs d1,d2 - detect (comma separated) devices only eg. /dev/sda,/dev/sdb,/dev/sdc
- -nodevs d1,d2 - exclude detection of (comma separated) devices eg. /dev/sda,/dev/sdb,/dev/sdc
- -dump - dump report to stdout (can be used with -xml to dump XML output instead of text)
- -xml - create and save XML report instead of TXT
- -solid - solid output (drive, tempC, health%, power on hours, model, S/N, size)
- -verbose - detailed detection information and save temporary files (only for debug purposes)
- -aam - display acoustic management settings (current and recommended level)
- -setaam drive_num|ALL level(hex)80-FE|QUIET|LOUD - set acoustic level on drive 0..n (or all)
80 or QUIET is the lowest (most silent) setting, FE or LOUD is the highest (fastest) setting
For example: hdsentinel -setaam 0 loud - Configures drive 0 to fastest (loud) setting. Same as hdsentinel -setaam 0 FE
