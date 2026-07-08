##  Init system
Systemd is the most compatible and best for beginners, but OpenRC and other alternatives can be leaner.
OpenRC boots slower on multi-core CPUs. This makes systemd preferable for boot time.
OpenRC only uses 40MB-70MB less RAM on idle. This matters much less than choice of desktop environment or window manager.
Systemd is more well documented and much closer to arch, it will be basically artix if we use OpenRC
I will use systemd to begin with, if during testing the system does not meet targeted hardware requirements, an OpenRC rework may be required.

## Default browser
Firefox is effecient, fast, optimised and widely used and documented. For these reasons I had selected it as my first candidate. The second candidate I selected was falkon, as it is considered to be the most compatible "lightweight" alternative. However, during benchmarks i compared the two browsers. During light browsing loads like google search etc, falkon used less memory but was significantly less responsive and just overall a worse experience than firefox. There was around a 200 MB difference in RAM usage at times during light browsing. However, during video playback, firefox shines. I played a video at 720p on youtube, the same video for each browser, falkon used 200 MB more RAM, and was significantly choppier. It is clear to me that firefox is more compatible with modern day workloads, and falkon is only suitable for light browsing. The default browser needs to better as an all round browser, not just for one thing. For these reasons I chose firefox.
