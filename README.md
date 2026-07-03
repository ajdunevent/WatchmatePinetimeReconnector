# Watchmate-Pinetime Reconnector

## Announcement:
My personal PineTime has been mostly retired and this project never quite reached the functionality I was aiming for.  If you still need a reliable way to connect a PineTime to a Linux Mobile, check out these interesting projects: 
* https://git.antisocialparadise.net/jeff/pinetime-furios
* https://github.com/nico359/pinepal


### Purpose:
* To keep the Watchmate Flatpak connected to your PineTime running InfiniTime


### Done:
* Discovers your paired PineTime device
* Monitors for PineTime device disconnection
* Attempts for ~5 minutes to rapidly reconnect while queueing missed notifications
* If connection occurs during this time, sends the queued notifications
* If connection doesn't occur in that time, clears the queued notifications and only attempts reconnection once every two minutes to save battery


### To Do:
* Make a less manual installation method


### How to install:
* Move the contents of dot-local_bin to ~/.local/bin/ and edit to your liking
* Move the contents of dot-config_systemd_user to ~/.config/systemd/user/
* Run: ```systemctl --user daemon-reload && systemctl --user enable --now pinetime-reconnection.service```


### How to uninstall
* Run: ```systemctl --user disable --now pinetime-reconnection.service```
* Remove the files you added to the directories above


### Shout out
* [FuriLabs](https://furilabs.com/) for making the [FLX1s](https://furilabs.com/shop/flx1s/), the first mobile Linux phone I've ever been able to comfortably (enjoyably even!) daily drive.
* [azymohliad](https://github.com/azymohliad) for [Watchmate](https://github.com/azymohliad/watchmate)
* [Pine64](https://pine64.org) for the [PineTime](https://pine64.org/devices/pinetime/)
* [JF002](https://github.com/JF002) (and contributors!) for [InifiniTime](https://github.com/InfiniTimeOrg/InfiniTime)
* [sorry-i-am-late](https://github.com/sorry-i-am-late) for [this comment](https://github.com/azymohliad/watchmate/pull/61#issuecomment-2323510023) which inspired me
