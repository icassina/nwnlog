# NWNLog

## Abstract

nwnlog is a small shell script that filters NWN1 logs and show them in a colorful format, by using multitail.

## Requirements

A POSIX operating system (sh, tail, sed, stdbuf) and multitail (https://www.vanheusden.com/multitail/)

## Installation

Install multitail and make sure it's available in your PATH environnment variable.

Edit the script (nwnlog) and point the variable "nwn_log_file" to the location of your nwn1 log file.

## Usage

Just run ./nwnlog and play nwn1.

Read the multitail online help by pressing 'h' when focusing the multitail terminal.

'/' for searching the log
'b' to scroll the log (page-up / page-down 'q' to exit scrollback window)
'q' to exit multitail

## Bugs

Since the script basically pipes `tail -f` output to `sed` and then to
`multitail`, when exiting multitail, the first command will continue to run
regardeless. You have to terminate it quite forcefully (ctrl-c)

Enjoy!
