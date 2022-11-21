# Pi-PrintScheduler

## Stop clogged inkjet printer issues
### Inkjet printers need to print often to keep from getting clogged up and wasting ink using the cleaning cycles.
### This will also save on the wasted ink going into the waste absorbing sponge.



### Install Cups
### Setup printer in the https://[CUPS ip address]:631 web interface
Username and password is the linux user and password


#### Create print file in ~/
   `touch print.sh`
#### Make it executable
   `chmod 777 print.sh`
#### Edit print file
   `nano print.sh`
#### Test file
   `lp /usr/share/cups/data/default-testpage.pdf`

#### Set default primter
   `lpoptions -d [printername]`

#### Setup schedule
   `crontab -e`

#### Examples
   `https://crontab.guru/#30_8_*_*_6`

#### Test with every Minute
   `*/1 * * * * /root/print.sh`

#### Every Mon - Wed - Friday @ 8:30 AM
   `30 8 * * 1,3,5 /root/print.sh`
