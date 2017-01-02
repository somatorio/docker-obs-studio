# OBS Studio
Open Broadcaster Software

# How to use?
```
docker run --rm \
            --device /dev/video0 \
            --device /dev/snd/ \
            --name obs \
            --net pulseaudio \
            -e DISPLAY \
            -e PULSE_SERVER=pulseaudio \
            -v /tmp/.X11-unix/:/tmp/.X11-unix/ \
            -v $HOME:/root/$(whoami) \
            -v $HOME/.obs:/root/.config/obs-studio \
            somatorio/obs-studio
```
