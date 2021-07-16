# Usage instructiuons
* **Prerequisite**</br>
  * Platform: Lilee STS-1000 series with a working disk drive in SATA 0
  * LileeOS version: LileeOS 4.7+
  * Do the following if the application framework is currently in app-engine mode
  <pre>
  localhost.localdomain > show application framework 
  App-Engine
  localhost.localdomain > update application framework container
  ...
  localhost.localdomain > reboot
  </pre>

* **Enabling X.Org service**</br>
<pre>
localhost.localdomain > create application name xorg
localhost.localdomain > update application name xorg profile package https://github.com/lileesystems-com/sts-1000/raw/master/profiles/xorg.zip
localhost.localdomain > config application name xorg enable
localhost.localdomain > save configuration
localhost.localdomain > show application all
Name       | State   | Started At                    
-----------------------------------------------------
xorg         running   2021-02-16T19:33:53.693904601Z
</pre>

* **Enabling PulseAudio service**</br>
<pre>
localhost.localdomain > update application storage volume create name paconfig sata 0
localhost.localdomain > create application name pulseaudio
localhost.localdomain > update application name pulseaudio profile package https://github.com/lileesystems-com/sts-1000/raw/master/profiles/pulseaudio.zip
localhost.localdomain > config application name pulseaudio enable
localhost.localdomain > save configuration
localhost.localdomain > show application all
Name       | State   | Started At                    
-------------------------------------
pulseaudio   running   2021-02-16T19:34:53.796957782Z
xorg         running   2021-02-16T19:33:53.693904601Z
</pre>

* **Enabling Firefox service**</br>
<pre>
localhost.localdomain > create application name firefox
localhost.localdomain > update application name firefox profile package https://github.com/lileesystems-com/sts-1000/raw/master/profiles/firefox.zip
localhost.localdomain > config application name firefox enable
localhost.localdomain > save configuration
localhost.localdomain > show application all
Name       | State   | Started At                    
-----------------------------------------------------
firefox      running   2021-02-16T19:35:49.485047854Z
pulseaudio   running   2021-02-16T19:34:53.796957782Z
xorg         running   2021-02-16T19:33:53.693904601Z
</pre>
