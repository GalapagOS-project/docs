##  Init system
Systemd is the most compatible and best for beginners, but OpenRC and other alternatives can be leaner.
OpenRC boots slower on multi-core CPUs. This makes systemd preferable for boot time.
OpenRC only uses 40MB-70MB less RAM on idle. This matters much less than choice of desktop environment or window manager.
Systemd is more well documented and much closer to arch, it will be basically artix if we use OpenRC
I will use systemd to begin with, if during testing the system does not meet targeted hardware requirements, an OpenRC rework may be required.
