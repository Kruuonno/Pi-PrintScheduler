# Pi-PrintScheduler

#### Create print file
   `touch print.sh`
#### make it executable
   `chmod 777 print.sh`
#### Edit print file
   `nano print.sh`
#### Test file
   `lp /usr/share/cups/data/default-testpage.pdf`

#### set default primter
   `lpoptions -d [printername]`

#### Setup schedule
   `crontab -e`

#### Test with every Minute
   `*/1 * * * * /root/print.sh`

#### examples
   `https://crontab.guru/#30_8_*_*_6`

#### Every Mon - Wed - Friday @ 8:30 AM
   `30 8 * * 1,3,5`
