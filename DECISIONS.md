##  Init system
Systemd is the most compatible and best for beginners, but OpenRC and other alternatives can be leaner.
OpenRC boots slower on multi-core CPUs. This makes systemd preferable for boot time.
OpenRC only uses 40MB-70MB less RAM on idle. This matters much less than choice of desktop environment or window manager.
Systemd is more well documented and much closer to arch, it will be basically artix if we use OpenRC
I will use systemd to begin with, if during testing the system does not meet targeted hardware requirements, an OpenRC rework may be required.


## Default browser
Firefox is efficient, fast, optimised and widely used and documented. For these reasons I had selected it as my first candidate. The second candidate I selected was falkon, as it is considered to be the most compatible "lightweight" alternative. However, during benchmarks i compared the two browsers. During light browsing loads like google search etc, falkon used less memory but was significantly less responsive and just overall a worse experience than firefox. There was around a 200 MB difference in RAM usage at times during light browsing. However, during video playback, firefox shines. I played a video at 720p on youtube, the same video for each browser, falkon used 200 MB more RAM, and was significantly choppier. It is clear to me that firefox is more compatible with modern day workloads, and falkon is only suitable for light browsing. The default browser needs to better as an all round browser, not just for one thing. For these reasons I chose firefox.


## Display server
The default display server will be X11. This decision is based primarily on compatibility. While Wayland is the future of the Linux desktop and offers a number of architectural improvements, X11 remains the more mature and widely supported option for the older 64-bit hardware GalapagOS is intended to target.

Users remain free to install and use Wayland after installation if their hardware and preferred desktop environment support it.

This decision is not considered permanent. As Wayland support for older hardware continues to mature, it will be periodically re-evaluated. If testing demonstrates that Wayland can provide comparable compatibility while improving performance, efficiency, or overall user experience on the project's target hardware, the default display server may change in a future release.


## Firefox Content Process Count

### Decision

GalapagOS will reduce Firefox's content process count from the upstream default to **4**.

### Rationale

Testing on the GalapagOS reference system showed approximately 200 MB lower memory usage during general web browsing while maintaining comparable responsiveness and media playback performance.

The change aligns with GalapagOS's goal of improving practical usability on memory-constrained systems.

### Review Criteria

This setting should be periodically re-evaluated as Firefox evolves. If future versions change process management or testing no longer demonstrates a measurable benefit, the default should be reconsidered.


## Boot Splash

### Decision

GalapagOS will not install Plymouth by default.

### Rationale

Plymouth primarily provides cosmetic improvements during boot. It does not improve usability or system performance and introduces an additional component into the boot process.

GalapagOS prioritises reliability, compatibility, and ease of troubleshooting over cosmetic boot animations. Boot messages remain visible, making it easier to diagnose startup problems, particularly on older hardware.

Users who prefer a graphical boot experience remain free to install Plymouth manually.
