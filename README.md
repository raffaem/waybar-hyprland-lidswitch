# waybar-hyprland-lidswitch

Waybar module to manage lidswitch from hyprland (i.e., at the compositor-level).

Copy `lidswitch` into `$HOME/.config/waybar/scripts`.

Put the following in waybar's config file:

```
"custom/lidswitch": {
    "exec": "$HOME/.config/waybar/scripts/lidswitch status",
    "interval": "once",
    "signal": 3,
    "format": "{}",
    "return-type": "json",
    "on-click": "$HOME/.config/waybar/scripts/lidswitch toggle"
},
```

Enable lidswitch management at start-up by putting the following in hyprland config file:

```
/home/USERNAME/.config/waybar/waybar-hyprland-lidswitch/lidswitch on
```
