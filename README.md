# my-pihole-lists

Alcoa Pi

  #Pi-Hole Daily Software Update
  0 1230 * * * sudo pihole -up

  #Pi External IP Address
  #0 0558,1158,1758,2358 * * * sudo curl ipecho.net > /home/pi/ipaddress.txt

  #Copy IP Address to Pi-hole lists
  #0 0559,1159,1759,2359 * * * sudo python /home/pi/projects/ipalcoa.py > /home/pi/projects/ipalcoa-log.txt

  #Push Master Pi-hole Lists from remote Git repo
  0 00,06,12,18 * * * sudo /usr/local/bin/pihole-cloudsync/pihole-cloudsync --push

  #Pi-Hole Daily Gravity Updates
  0 0005,0605,1205,1805 * * * sudo pihole -g

  #Pull Master Pi-hole lists from remote Git repo (to sync machines)
  #0 0025,1225 * * * sudo /usr/local/bin/pihole-cloudsync/pihole-cloudsync --pull

Philadelphia Pi

  #Pull Master Pi-hole Lists from remote Git repo
  0 0010,0610,1210,1810 * * * sudo /usr/local/bin/pihole-cloudsync/pihole-cloudsync --pull

  #Pi-Hole Daily Gravity Updates
  0 0015,0615,1215,1815 * * * sudo pihole -g

  #Pi External IP Address
  0 0018,1218 * * * sudo curl ipecho.net > /home/pi/ipaddress.txt

  #Copy IP Address to Pi-hole lists
  0 0019,1219 * * * sudo python /home/pi/projects/ipphiladelphia.py > /home/pi/projects/ipphiladelphia-log.txt

  #Push Master Pi-hole List to Git repo (for purpose of updating IP Philadelphia Address)
  0 0020,1220 * * * sudo /usr/local/bin/pihole-cloudsync/pihole-cloudsync --push





