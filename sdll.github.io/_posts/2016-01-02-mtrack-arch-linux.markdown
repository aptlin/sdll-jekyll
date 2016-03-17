---
layout: post
title: mtrack & Arch Linux
date: 2016-01-02 19:10:41.000000000 +00:00
type: post
published: true
status: publish
categories:
- sysadmin
---
<p>The <a href="https://github.com/BlueDragonX/xf86-input-mtrack">mtrack driver</a> provides multifacetous configurability and gestures support for multitouch touchpads.</p>
<p>In Arch, the driver can be installed from the AUR with yaourt:</p>
<p id="850b" class="graf--pre graf-after--p"><strong>yaourt -S xf86-input-mtrack-git</strong></p>
<p>Then set up your configuration file:</p>
<p id="d6d9" class="graf--pre graf-after--p"><strong>sudo nano /etc/X11/xorg.conf.d/10-mtrack.conf</strong></p>
<p class="graf--pre graf-after--p">The configuration I recommend is the following:</p>
<pre>
<code class="bash">
Section "InputClass"
        Identifier "touchpad"
        MatchIsTouchpad "on"
        Driver          "mtrack”
        MatchDevicePath "/dev/input/event*”
        Option          "Sensitivity” “0.85”
        Option          "FingerHigh” “3”
        Option          "FingerLow” “3”
        Option          "IgnoreThumb” “false”
        Option          "IgnorePalm” “true”
        Option          "TapButton1” “0”
        Option          "TapButton2” “3”
        Option          "TapButton3” “2”
        Option          "TapButton4” “0”
        Option          "ClickFinger1” “1”
        Option          "ClickFinger2” “2”
        Option          "ClickFinger3” “3”
        Option          "ClickFinger4” “0”
        Option          "ButtonMoveEmulate” “false”
        Option          "ButtonIntegrated” “true”
        Option          "ClickTime” “0”
        Option          "BottomEdge” “0”
        Option          "SwipeLeftButton” “8”
        Option          "SwipeRightButton” “9”
        Option          "SwipeUpButton” “0”
        Option          "SwipeDownButton” “0”
        Option          "ScrollDistance” “75”
        Option          "ScrollUpButton” “4”
        Option          "ScrollDownButton” “5”
EndSection
</code>
</pre>
<p class="graf--pre graf-after--p">Change places of <strong>ScrollUpButton</strong> and <strong>ScrollDownButton </strong>to enable natural scrolling.</p>
<p class="graf--pre graf-after--p">Next, add the user of your choice to the <strong>input</strong> group to give the permissions required for setting the input methods up:</p>
<p id="9007" class="graf--pre graf-after--p"><strong>sudo gpasswd -a <em>$USERNAME</em> input</strong></p>
<p class="graf--pre graf-after--p">Restart the X server and enjoy!</p>

