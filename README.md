Damn you Lenovo
===============

Crappy touchpad is crappy.

(╯°□°）╯︵ ┻━┻

Installation
------------
```bash
sudo mkdir /etc/X11/xorg.conf.d
sudo cp 99-synaptics-t440s.conf /etc/X11/xorg.conf.d/

sudo mkdir /etc/X11/Xsession.d
sudo cp 98x11-syndaemon /etc/X11/Xsession.d/98x11-syndaemon
```

You will get
------------

Gesture          | Description
---------------- | -----------
One finger tap   | Left mouse button
Two finger tap   | Right mouse button
Three finger tap | Middle mouse button
Two finger swipe | Horizontal/Vertical scrolling
Everything else  | Disabled (no button areas, no edge scrolling, no tap and drag, etc.)

You will also get ```syndaemon``` with a sane configuration:

```bash
syndaemon -d -t -k -i 1 -m 100
```

Option | Description
------ | -----------
-d     | Start as a daemon, ie in the background.
-t     | Only disable tapping and scrolling, not mouse movements, in response to keyboard activity.
-k     | Ignore modifier keys when monitoring keyboard activity.
-i 1   | How many seconds to wait after the last key press before enabling the touchpad.
-m 100 | How  many  milliseconds  to wait between two polling intervals.



\o/
