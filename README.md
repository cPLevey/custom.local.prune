# Scenario
Sometimes people want to keep less local backup copies (store 2 local) and more on the remote (store 10 remote). 

There is currently not a way to do this officially but a custom post backup script could be created to run after backups. For example, this script will search the backup dir for cPanel style backups and remove ones to maintain the number set by retain_local. 

The script prints what it would remove, but you could comment the final print line and uncomment the system rm line to have it delete once verifying that it works as intended. Using the bellow script with settings to retain 10 backups, the script will remove all the local backups except the 2 newest ones after backups finish. 

# Caveats
It does not check if the backups transported successfully which would be a notable caveat. 

# Links
[Feature Request](https://features.cpanel.net/topic/seperate-options-to-retain-backups-on-different-locations)

[Registering Hook](https://forums.cpanel.net/threads/rsync-after-backup-ends.488801/#post-1961371)
