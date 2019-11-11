Change Lid Close Action in Ubuntu 19.10
=======================================
In Ubuntu 19.10 Gnome desktop, there’s no option in Settings utility for configuring laptop lid close actions. And Gnome Tweaks only offer a switch to enable / disable ‘Suspend when laptop lid is closed’.

For those who want it automatic shutdown, hibernate, or do nothing when laptop lid is closed, here’s how to do it by hacking on the configuration file.

<ol>
<li> Open terminal by pressing Ctrl+Alt+T or searching for “Terminal” from start menu. When it opens, run command:

    sudo gedit /etc/systemd/logind.conf
 </li>

<li> When the files opens, uncomment the line #HandleLidSwitch=suspend by removing # in the beginning, and change the value to:

    HandleLidSwitch=poweroff, shutdown / power off when lid is closed.
    HandleLidSwitch=hibernate, hibernate when lid is closed (need to test if hibernate works).
    HandleLidSwitch=ignore, do nothing.
    HandleLidSwitch=suspend, suspend laptop when lid is closed.
</li>


</ol>

In addition:
-------------

<ol>
<li> Previous steps do not add shutdown or hibernate options in the Power settings utility, but directly do the action when you close the laptop lid.
</li>

<li> For some laptops, the hibernate function might not work. Run test command:

    sudo apt install pm-utils && sudo pm-hibernate

</li>
