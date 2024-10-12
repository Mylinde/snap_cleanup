# Snap Remover Script

This script removes disabled snaps from your system.

## Purpose

This script is designed to automatically remove snaps that are marked as disabled. This can be useful for cleaning up your system and removing unnecessary packages.

## Usage

To use this script, simply save it to a file (e.g. `remove_disabled_snaps.sh`) and make it executable with the command `chmod +x remove_disabled_snaps.sh`. Then, run the script with the command `./remove_disabled_snaps.sh`.

## How it works

The script uses the `locale` command to determine the language of your system and sets the word for "disabled" accordingly. It then uses the `snap list --all` command to get a list of all snaps on your system, including their status. The `awk` command is used to filter the list and only print the names and revisions of disabled snaps. Finally, the script uses a `while` loop to remove each disabled snap using the `sudo snap remove` command.

## Notes

* This script requires root privileges to run, as it uses `sudo` to remove snaps.
* Be careful when running this script, as it permanently removes disabled snaps without prompting for confirmation.
* If you want to modify the script to remove snaps in a different language, you can simply add more cases to the `case` statement to handle different languages.
