
- List installed versions in your system:
    ```bash
    $ snap list intellij-idea-ultimate  --all
    
    Name                    Version   Rev  Tracking       Publisher   Notes
    intellij-idea-ultimate  2019.3.4  212  latest/stable  jetbrains✓  disabled,classic
    intellij-idea-ultimate  2020.1    216  latest/stable  jetbrains✓  classic
    
    ```
	
- Revert to a previous one:
    ```
    sudo snap revert intellij-idea-ultimate
    ```
    
- Revert to a specific revision:
    ```
    sudo snap revert intellij-idea-ultimate --revision 212
    ```


***
# [How can I disable automatic update for a single snap in Ubuntu?](https://askubuntu.com/questions/1131182/how-can-i-disable-automatic-update-for-a-single-snap-in-ubuntu)

with the latest version of snap (so far on edge channel) you can disable snap updates

The new hold feature allows system administrators and end users to stop or postpone their snap updates for as long as necessary. The hold can be applied to individual snaps or the entire set of installed snaps, for a limited period of time, or – if necessary – indefinitely.

For instance, to pause snap updates for VLC for 3 days, you would run the following command:

```
snap refresh --hold=72h vlc
```

General refreshes of "vlc" held until 2022-11-17T12:04:59Z

Similarly, to pause snap refreshes for all snaps for a period of 48 hours:

```
snap refresh --hold=48h
```

Auto-refresh of all snaps held until 2022-11-16T12:27:25Z

To stop the automatic refresh completely, and without a timer:

```
snap refresh --hold
```

Auto-refresh of all snaps held indefinitely.

Source: [https://snapcraft.io/blog/hold-your-horses-i-mean-snaps-new-feature-lets-you-stop-snap-updates-for-as-long-as-you-need](https://snapcraft.io/blog/hold-your-horses-i-mean-snaps-new-feature-lets-you-stop-snap-updates-for-as-long-as-you-need)