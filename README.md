# my-pihole-lists

Alcoa Pi

  # Weekly Update 
  0 4 * * 1 sudo apt update  -y
  #
  # Weekly Upgrade
  0 5 * * 1 sudo apt upgrade -y
  #
  #Pi-Hole Daily Software Update
  30 12 * * * sudo pihole -up
  #
  #Push Master Pi-hole Lists from remote Git repo
  0 00,06,12,18 * * * sudo /usr/local/bin/pihole-cloudsync/pihole-cloudsync --push
  #
  #Pi-Hole Daily Gravity Updates
  05 00,06,12,18 * * * sudo pihole -g
  
Philadelphia Pi

  #Pull Master Pi-hole Lists from remote Git repo
  10 00,06,12,18 * * * sudo /usr/local/bin/pihole-cloudsync/pihole-cloudsync --pull

  #Pi-Hole Daily Gravity Updates
  30 00,06,12,18 * * * sudo pihole -g
