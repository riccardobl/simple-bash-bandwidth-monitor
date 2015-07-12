# Simple Bash Bandwidth Monitor
Simple bash script, with optional PHP frontend, for monitoring speed and traffic on linux.

## Requirements
`numfmt awk`

Optional: `exec` enabled in `php.ini` in order to use the php frontend

## Available Actions
`up` = current upload speed

`down` = current download speed

`total-up` = upload traffic since the latest reboot

`total-down` = download traffic since the latest reboot


## Available Formats
`GB` = Show values in GigaBytes

`MB` = Show values in MegaBytes

`KB` = Show values in KiloBytes

`B` = Show values in Bytes

`HUMAN` = Show values in Human readable format


## Installation
1. Install the dependencies (see Requirements)
2. Clone the repo where you want
3. Run `./status.sh ACTION INTERFACE FORMAT` (see Available Actions & Available Formats)
4. END


## Installation on webserver
1. Install the dependencies and enable exec inside the php.ini (See Requirements)
2. Clone the repo inside the webserver
3. Open status.php
4. Edit `$interface="eth0";` with the interface you want to monitor
5. Open the url `http://XXXXXXXXX/status.php?t=ACTION&f=FORMAT` (see Available Actions & Available Formats)
6. END
 

## Conky
See conkyrc-snippet for the code
