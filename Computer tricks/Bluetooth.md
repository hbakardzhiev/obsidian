1) Connect using `Bluejay` with device
2) `pactl list sinks | grep bluetooth`
3) find `bluez_output.XX__XX__XX_XX_XX_X.X`
4) pactl set-default-sink `bluez_output.XX__XX__XX_XX_XX_X.X`