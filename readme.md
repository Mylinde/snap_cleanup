# Snap Remover Script

This script removes disabled snaps from your system.

## Purpose

This script is designed to automatically remove snaps that are marked as disabled. This can be useful for cleaning up your system and removing unnecessary packages.

## Usage

To use this script, simply save it to a file (e.g. `remove_disabled_snaps.sh`) and make it executable with the command `chmod +x remove_disabled_snaps.sh`. Then, run the script with the command `./remove_disabled_snaps.sh`.

## How it works

The script sets temporarily LANG to C to ensure that the output of snap list --all is in English. It then uses the `snap list --all` command to get a list of all snaps on your system, including their status. The `awk` command is used to filter the list and only print the names and revisions of disabled snaps. Finally, the script uses a `while` loop to remove each disabled snap using the `sudo snap remove` command.

## Notes

* This script requires root privileges to run, as it uses `sudo` to remove snaps.
* Be careful when running this script, as it permanently removes disabled snaps without prompting for confirmation.