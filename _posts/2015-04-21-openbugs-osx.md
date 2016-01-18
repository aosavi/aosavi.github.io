---
layout: post
title: OpenBUGS on Mac OS X
---

Before going through the effort of installing OpenBUGS on a Mac, ask yourself whether you wouldn’t rather want to use [JAGS](http://mcmc-jags.sourceforge.net/), [Stan](http://mc-stan.org/), or the awesome [JASP](https://jasp-stats.org/). If you persist, this quick walk-through should help you out.

## WineBottler
[WineBottler](http://winebottler.kronenberg.org/) will help you run Windows applications on your Mac. Download the version of WineBottler that is compatible with your operating system (e.g., OS X Yosemite) and install it. If you are unsure about which OS you are running, hit the Apple sign in the top-left corner and choose ‘About This Mac’.

## OpenBUGS
You can now download the [OpenBUGS](http://openbugs.net/w/Downloads) ‘Microsoft Windows Download’. As soon as you try to open the executable (.exe), WineBottler will ask you what to do with it (this may take a while as Wine needs to be verified the first time). Choose ‘Convert to simple OS X Application bundle with WineBottler’ and hit ‘Go’.

You can leave the advanced settings that will pop-up to their defaults and hit ‘Install’. You will then be asked how and where to save the application. Saving it as ‘OpenBUGS’ in your Application folder is probably the most convenient.

After a while you will be directed to the OpenBUGS setup. Accept the license agreement, leave the subsequent options to their defaults, and hit ‘Install’ once more. As soon as the installation is finished you are asked to select the startfile, which should naturally be the OpenBUGS.exe.

You are now ready to use OpenBUGS on your Mac. You may either open it from within WineBottler (tab ‘On My Mac’) or directly from your Applications folder (as long as you don’t do both simultaneously). The first time you open OpenBUGS it needs to initialize, so you will have to be patient for a while.

Finally, be aware that you are now running OpenBUGS in a Windows-like environment, so you’ll for instance need ctrl-C/V rather than cmd-C/V to copy/paste.

### BIEMS
You can now also easily run [BIEMS](https://informativehypotheses.wordpress.com/software/biems/) on your Mac, for (in)equality constrained models. Obtain the version of BIEMS with a Windows user interface, open BIEMS.exe, and choose to run it directly (i.e., do not convert it to a simple OS X Application bundle).

## Uninstall
Want to get rid of OpenBUGS? Make sure to remove it through WineBottler (WineBottler > On My Mac > Remove).

## Troubleshooting
If OpenBUGS somehow fails to install or run, there are two options to consider. First check if you are running [Xcode](https://developer.apple.com/xcode/downloads/) (hit CMD-spacebar and search for it) and either download it from Apple’s App Store or make sure it is up-to-date (hit the Apple sign in the top-left and choose ‘App Store…’ and ‘Updates’). Second, if you still do not succeed you may try to install [MacPorts](https://www.macports.org/install.php). Be warned that installing MacPorts will take a few hours to complete!